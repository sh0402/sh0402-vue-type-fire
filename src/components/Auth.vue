<template>
  <div class="container">
    <AuthSign />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import AuthSign from '@/components/Auth/Sign.vue'
import firebase from 'firebase/app'

declare module 'vue/types/vue' {
  interface Vue {
    $firebase: typeof firebase;
  }
}

@Component({
  components: { AuthSign }
})
export default class extends Vue {
  async test (): Promise<void> {
    const ref = this.$firebase.firestore().collection('test').doc('aaaa')
    await ref.set({ a: 111 })
    const doc = await ref.get()
    console.log(doc.data())
  }
}
</script>

<style scoped>

</style>
