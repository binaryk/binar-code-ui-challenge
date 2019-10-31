<template>
  <div class="notification">
      <div class="header">
      <h2 style="width:100%">
        <img class="done-icon" alt="touch logo" src="https://icon-library.net/images/done-icon/done-icon-16.jpg">
          Thank you
          <a class="close-icon" @click="close">            
              <img class="close-icon" alt="touch logo" src="https://icon-library.net/images/close-icon-png-transparent/close-icon-png-transparent-26.jpg">
          </a>
      </h2> 
      </div>
      
      <span>
          One of your team members will get back to you as soon as possible.
      </span>
  </div>
</template>

<script>
export default {
    name: 'notification',
    methods: {
        close() {
            this.$emit('submitted', false);
        }
    }
};
</script>

<style scoped>

.notification {
    font-family: 'Montserrat', sans-serif;
    position: fixed;
    right: 10px;
    top: 10px;
    width: 300px;
    height: 150px;
    background-color: white;
    border-radius: 15px;
    font-weight: bold;
}

.header {
    display: flex;
    flex-direction: row;
    justify-content: center;
}

.close-icon {
    height: 10px;
    margin-right: 10px;
    float:right;
}

.done-icon {
    height: 20px;
}

</style>