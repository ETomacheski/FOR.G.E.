<template>
<div>
  <Navbar />

  <div>

    <div class="container-login">
    <h1>
      Login
    </h1>
    <span class="Label">Email</span>
    <input class="input-login"
      type="text"
      v-model='email'
    />
    <span class="Label">Senha</span>
    <input class="input-login"
      type="password"
      v-model='password'
    />
    <button
      class="btn-primary"
      @click="logar()"
     >Entrar</button>
    </div>

  </div>

</div>

</template>
<script>
import Navbar from '../../components/navbar.vue'
import { mapMutations } from 'vuex'

export default {
  components: {
    Navbar
  },

  data () {
    return {
      email: '',
      password: ''
    }
  },

  methods: {
    ...mapMutations(['setToken']),
    async logar () {
      // const response = await axios({
      //   method: 'post',
      //   url: 'https://eifchar-api.herokuapp.com/login',
      //   params: {
      //     email: this.email, password: this.password
      //   },
      //   withCredentials: true
      // })
      // this.setToken(response.data.token)
      // return this.$router.push({ name: 'adminHome' })
    }
  },
  watch: {
  }
}
</script>

<style scoped>
  *{
    color: black;
  }
  .container-login{
    display: flex;
    flex-direction: column;
    width: 400px;
    margin: auto;
    margin-top: 100px;
  }
  .input-login{
    height: 40px;
    border: 3px solid #00FA9A;
  }
  .Label{
    font-size: 18px;
    font-family: 'Montserrat', sans-serif;
    font-weight: 500;
    padding: 10px 0;
  }
  .btn-primary{
    padding: 10px 0;
    border: 3px solid #00FA9A;
    color: #00FA9A;
    margin-top: 10px;
    background-color: transparent;
    width: 25%;
    text-transform: uppercase;
    transition: color 0.5;
    transition: border 0.5s;
    font-weight: bold;
    letter-spacing: 0.5px;
  }
  .btn-primary:hover{
    border: 3px solid black;
    color: black;
  }
</style>
