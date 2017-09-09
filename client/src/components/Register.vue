<template>
  <div>
    <h1>Register</h1>
    <input type="email" name="email" placeholder="email" v-model="email">
    <br>
    <input type="password" name="password" placeholder="password" v-model="password">
    <br>
    <button @click="register">Register</button>
  </div>
</template>

<script>
import AutentificationService from '@/services/AuthentificationService'
export default {
  data () {
    return {
      email: 'abc',
      password: '1234'
    }
  },
  methods: {
    async register () {
      await AutentificationService.register({
        email: this.email,
        password: this.password
      })
    }
  }
}
</script>

<style scoped>

</style>
