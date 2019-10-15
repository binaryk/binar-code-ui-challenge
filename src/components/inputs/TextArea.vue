<template>
  <div>
        <textarea name="help us" class="input-master" cols="10" rows="7" v-bind="$attrs" :value="value" v-on="listeners"></textarea>  
  </div>
</template>

<script>
export default {
    name: 'input-area',
    props: {
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
    font-family: 'Montserrat', sans-serif;
    background: transparent;
    border-width: 0 0 1px;
    outline: none;
    width: 380px;
    padding: 7px;
    border-color: white;
    margin: 10px 0;

}

::placeholder { 
  color: white;
  opacity: 0.7; 
}

</style>