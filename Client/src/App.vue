<template>
  <div id="app">
    <router-view/>
  </div>
</template>


<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
  }

    // body {
    //   min-height: 100%;
    //   height: 100%;
    //   display: flex;
    //   flex-direction: column;
    //   background: #efefef;
    // }

  #app {
    // position: relative;
    // min-height: 100vh;
  }

  body {
    background: #efefef;
  }

  p, a {
    font-family: 'Open Sans', sans-serif;
  }
</style>
