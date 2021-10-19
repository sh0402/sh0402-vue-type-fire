<template>
  <div @submit.prevent="submit">
    <div class="mb-3">
      <label for="exampleFormControlInput1" class="form-label"
        >Email address</label
      >
      <input
        v-model="email"
        class="form-control"
        id="exampleFormControlInput1"
        placeholder="name@example.com"
      />
    </div>
    <div class="mb-3">
      <label for="exampleFormControlTextarea1" class="form-label"
        >Example textarea</label
      >
      <textarea
        class="form-control"
        id="exampleFormControlTextarea1"
        rows="3"
      ></textarea>
    </div>
    <div class="col-auto">
      <button type="submit" class="btn btn-primary mb-3" @click="submit">
        Submit
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { auth } from '@/plugins/firebase'

@Component<AuthSign>({
  created () {
    this.signIn()
  }
})

export default class AuthSign extends Vue {
  email = '';

  submit (): void {
    const actionCodeSettings = {
      url: 'http://localhost:8080/finishSignUp',
      handleCodeInApp: true
    }
    auth
      .sendSignInLinkToEmail(this.email, actionCodeSettings)
      .then(() => {
        localStorage.setItem('emailForSignIn', this.email)
      })
      .catch((error) => {
        console.error(error.message)
      })
  }

  signIn (): void {
    if (!auth.isSignInWithEmailLink(location.href)) return
    const email = localStorage.getItem('emailForSignIn')
    if (!email) return
    this.email = email
    auth
      .signInWithEmailLink(email, location.href)
      .then((result) => {
        console.log(result)
        localStorage.removeItem('emailForSignIn')
      })
      .catch((error) => {
        console.error(error.message)
      })
  }
}
</script>

<style scoped></style>
