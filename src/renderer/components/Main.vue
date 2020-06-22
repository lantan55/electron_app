<template>
  <div id="wrapper">
    <img id="logo" src="~@/assets/logo.png" alt="electron-vue">
    <main>
      <h1>Добро пожаловать!</h1>
      <MainMenu></MainMenu>
    </main>

    <Footer></Footer>
  </div>
</template>

<script>
  export default {
    name: 'landing-page',
    components: {
      Footer: () => import('./Footer.vue'),
      MainMenu: () => import('./MainMenu.vue')
    },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: 'Source Sans Pro', sans-serif;
    font-size: 16px;
  }

  #wrapper {
    position: relative;
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 30px 40px;
    width: 100vw;
  }

  #logo {
    height: auto;
    margin-bottom: 20px;
    width: 150px;
  }

  main {

  }

  h1{
    font-size: 2em;
  }
</style>
