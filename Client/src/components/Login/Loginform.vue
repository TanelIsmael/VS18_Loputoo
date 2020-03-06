<template>
    <form action="/student">
        <input type="text" placeholder="email" v-model="email">
        <input type="text" placeholder="password" v-model="password">

        <input type="button" @click="login" value="Login">
    </form>
</template>

<script>
import AuthService from '@/services/AuthService.js';

export default {
  data() {
    return {
      email: '',
      password: ''
      
    };
  },
  methods: {
    async login() {
      try {
        const credentials = {
          email: this.email,
          password: this.password
        };
        const response = await AuthService.login(credentials);
        

        const token = response.token;
        const user = response.user;
        //const role = this.$store.getters.getUser.role;
        //const role = store.getters.user.role;
        //const role = store.state.user.role;

        this.$store.dispatch('login', { token, user });

        //this.role = this.$store.getters.getUser.role;
        /*if (role === 'student'){
          this.$router.push('/student');
        } else if (role === 'admin'){
          this.$router.push('/student');
        }*/
        this.$router.push('/student')
        
      } catch (error) {
        this.msg = error.response.data.msg;
      }
    }
  }
};
</script>


<style lang="scss" scoped>
    form {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        input {
            line-height: 20px;
        }

        input[type="text"], input[type="password"] {
            border: 1px solid #0099d8;
            border-radius: 50px;
            padding: 5px;
            color: #0099d8;
            outline: none;
            width: 250px;
            background: #efefef;
            margin-bottom: 20px;
        }

        input[type="submit"] {
            background:#0099d8;
            color: #ffffff;
            width: 250px;
            border: 1px solid #0099d8;
            border-radius: 50px;
            padding: 2px 8px;
            outline: none;
            font-size: 16px;
            line-height: 26px;
            transition: 150ms ease-in-out;
            cursor: pointer;


            &:hover {
                background:#00719e;
                border: 1px solid #00719e;
            }

        }
    }
</style>