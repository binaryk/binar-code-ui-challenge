
  <template>
  <div id="app">
    <Login />
  </div>
</template>

<script>
import Login from './components/Login.vue'

export default {
  name: 'app',
  components: {
    Login
  }
}
</script>

<style>

body {
  background-color: #FF6060;
  
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>
