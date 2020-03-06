<template>
  <div>
    <Header></Header>
    <main>
      <Login></Login>
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
import Login from '@/components/Login/Login'
import Header from '@/components/Header'
import Footer from '@/components/Footer'

export default {
  components: {
    Header,
    Login,
    Footer
  }
}
</script>
