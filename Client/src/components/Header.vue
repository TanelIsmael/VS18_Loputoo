<template>
  <header>
    <div class="logo">
      <img src="../assets/Logo.svg">
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>
  header {
    background: #0054a6;
    height: 70px;
    display: flex;
    align-items: center;
    padding: 0 30px;

    .logo > img {
      height: 50px;
    }
  }
</style>