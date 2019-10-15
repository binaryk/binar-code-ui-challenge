<template>
  <div class="input-master">
    <!-- <div class="input-wrapper"> -->
      <input class="input-field" type="text" v-bind="$attrs" :value="value" v-on="listeners"> 
      <span v-if="error === true" class="error">
        {{message}}
      </span>
    <!-- </div> -->
    
      
  </div>
</template>

<script>
export default {
    name: 'input-area',
    props: {
        message: String,
        error: Boolean,
        value: String
    },
    computed: { 
      listeners() {
        return {
          ...this.$listeners,
          input: this.onInput
        }
      }
    },
    methods: {
      onInput(e) {
        this.$emit('input', e.target.value);
      }
    }
};
</script>


<style scoped>

.input-master {
  margin: 10px 0;
  
}

.input-field {
    font-family: 'Montserrat', sans-serif;
    background: transparent;
    border-width: 0 0 1px;
    outline: none;
    width: 380px;
    margin: 10px auto;
    padding: 7px;

}

::placeholder { 
  color: white;
  opacity: 0.7; 

}

.error {
  font-family: 'Montserrat', sans-serif;
  float: left;
  color: white;
  font-size: 12px;
}

</style>