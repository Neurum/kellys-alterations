<template>
  <Navbar />
  <router-view />
  <Footer />
</template>

<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  font-size: 62.5%;
}

html,
body {
  overflow-x: hidden;
}

html {
  scroll-behavior: smooth;
  overflow-y: scroll;
}

body {
  font-family: 'Nunito', sans-serif;
  background: #fcecdd;

  &::-webkit-scrollbar {
    width: 1rem;

    &-track {
      background: #fcecdd;
    }

    &-thumb {
      background: #2f2f2f;
    }
  }
}
</style>
