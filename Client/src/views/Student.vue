<template>
  <div class="student">
    <Header></Header>
    <main>
      
      <h1 class="headline">VS (noorem tarkvaraarendaja) õpilane</h1>
      <Tab></Tab>
    </main>
    <input type="button" value="Logout" @click="logout" />
    <Footer></Footer>
  </div>
</template>


<script>
// @ is an alias to /src
import Header from '@/components/Header';
import Tab from '@/components/Tab/Tab';
import Footer from '@/components/Footer';
import AuthService from '@/services/AuthService.js';

export default {
  name: 'momo',
  components: {
    Header,
    Tab,
    Footer
  },
  data() {
    return {
      email: '',
      initialTab: 'taotlusleht',
      tabs: ['taotlusleht', 'hinnanguleht', 'juhendid', 'dokumendid', 'abimaterjalid']
    };
  },
  async created() {
    if (!this.$store.getters.isLoggedIn) {
      this.$router.push('/');
    }

    this.email = this.$store.getters.getUser.email;

    this.secretMessage = await AuthService.getSecretContent();
  },
  methods: {
    logout() {
      this.$store.dispatch('logout');
      this.$router.push('/');
    }
  }
};
</script>



<style lang="scss" scoped>
  .student {
    // display: flex;
    // flex-direction: column;
    // justify-content: space-evenly;


    main {
      padding: 5rem 15rem;
      margin-bottom: 101px;
    }

    .headline {
      font-family: 'Source Sans Pro', sans-serif;
      font-weight: 700;
      font-size: 2.25rem;
      margin-bottom: 40px;
    }
  }
</style>