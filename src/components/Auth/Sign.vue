<template>
  <div @submit.prevent="submit">
    <div class="mb-3">
      <label for="exampleFormControlInput1" class="form-label">Email address</label>
      <input v-model="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">
    </div>
    <div class="mb-3">
      <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
    </div>
    <div class="col-auto">
      <button type="submit" class="btn btn-primary mb-3" >Submit</button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { auth } from '@/plugins/firebase'

@Component({})
export default class AuthSign extends Vue {
  email=''

  submit () {
    var actionCodeSettings = {
      url: 'https://localhost:8080/finishSignUp',
      handleCodeInApp: true
    }
    auth.sendSignInLinkToEmail(this.email, actionCodeSettings)
      .then(() => {
        localStorage.setItem('emailForSignIn', this.email)
      })
      .catch((error) => {
        console.error(error.message)
      })
  }
}
</script>

<style scoped>

</style>
