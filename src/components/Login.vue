<template>
    <div>
      <form class="review-form" @submit.prevent="onSubmit">

      <div class="logo">
        <img alt="touch logo" src="https://www.binarcode.com/img/icons/design/svg/check-mail.svg">
          <h1 class="message">Get in touch</h1>
      </div>

      <div class="wrapper">
        <Input message="The name field is required" :placeholder="'Name'" :id="'name'" v-model="formData.name" :error="error.name" /> 
        <Input message="The email field must be a valid email" :placeholder="'Email Adress'" :id="'email'" v-model="formData.email" :error="error.email" />
        <Input message="Only numbers allowed" :placeholder="'Phone (optional)'" :id="'phone'" v-model="formData.phone" :error="error.phone" />
        <TextArea :placeholder="'How we can help'" :id="'text'" v-model="formData.text" />
        <Button />
      </div>
      </form>

      <Notification :submitted="submitted" @submitted="formSubmited"/>
      
    </div> 
</template>

<script>

import Input from './inputs/Input.vue'
import TextArea from './inputs/TextArea.vue'
import Button from './Button.vue'
import Notification from './Notification.vue'


export default {
  name: 'Login',
  
  components: {
    Input,
    TextArea,
    Button, 
    Notification
  },
  data() {
    return {
      formData: this.initFormData(),
      submitted: false,
      error: {
        name: false,
        email: false
      }
    }
  },
  methods: {
    onSubmit() {
      if (!this.validation()) {
        return 
      }
      this.submitted = true
      this.formData = this.initFormData()
    },
    formSubmited(state) {
      this.submitted = state
    },
    validation() {
      var re = /\S+@\S+\.\S+/;
      var nu = /^-?\d*\.?\d*$/;
      this.error = {
        name: false,
        email: false,
        phone: false
      }
      if (!this.formData.name) {
        this.error.name = true
        return false;
      } else if (!re.test(this.formData.email)) {
        this.error.email = true
        return false;
      }
      else if (!nu.test(this.formData.phone)) {
        this.error.phone = true
        return false;
      }
      return true;
    },
    initFormData() {
      return {
        name: '',
        email: '',
        text: '',
        phone: ''
      }
    }
  },
  watch: {
  formData: {
     handler(val){
       this.validation()
     },
     deep: true
  }
}
}
</script>

<style scoped>

.logo {
  margin-top: 100px;

}
h1 {
  color: white;
  font-family: 'Montserrat', sans-serif;
}

.wrapper {
  display:flex;
  width: 400px;
  flex-direction: column;
  justify-content: center;
  margin: auto;
}
</style>
