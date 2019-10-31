
  <template>
  <div id="app">
    <!-- <Login /> -->
    <!-- <Task /> -->
    <SlotScopeTable :data="tableData" :table-header="tableColumns">
      <template slot-scope="{ row }">
        <!-- <td class="bold-row">{{ row.name }}</td>
        <td class="img-row">{{row.age}}</td>
        <td class="img-row">{{row.email}}</td>
        <td class="img-row">{{row.status}}</td> -->

        <td><input type="text" :value="row.name"></td>
        <td><input type="text" :value="row.age"></td>
        <td><input type="text" :value="row.email"></td>
        <td><input type="text" :value="row.status"></td>

        <td class="actions-row">
          <button @click="handleEdit(row)">Edit</button>
        </td>
      </template>
    </SlotScopeTable>
  </div>
</template>

<script>
import Login from './components/Login.vue'
import Task from './components/Task.vue'
import SlotScopeTable from './components/SlotScopeTable.vue'


export default {
  name: 'app',
  components: {
    /* eslint-disable */
    Login, 
    Task,
    SlotScopeTable
  },
  data() {
    return {
      tableData: [
        {
          name: "John",
          age: 22,
          status: true,
          email: "john@gmail.com"
        },
        {
          name: "Lan",
          age: 18,
          status: true,
          email: "lan@gmail.com"
        },
        {
          name: "Mia",
          age: 19,
          status: false,
          email: "mia@gmail.com"
        },
        {
          name: "Masha",
          age: 23,
          status: true,
          email: "masha@gmail.com"
        }
      ],
      tableColumns: ["Name", "Age", "Email", "Status", "Edit"]
    }
  },
  methods: {
     handleEdit: function (row) {
       this.$eventHub.emit('editRow',row.name);
       var found = this.tableData.filter( r => r.name === row.name );
       this.tableData[0].name = row.name;
      console.log( JSON.parse(JSON.stringify( found[0] )));
      
  }
  }
}
</script>

<style>

body {
  /* background-color: #FF6060; */
  
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>
