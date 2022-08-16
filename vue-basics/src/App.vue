<template>
  <NaviComp />

  <router-view/>
  <FooterComp />
</template>

<script>
import { ref } from 'vue';
import FooterComp from './components/FooterComp.vue';
import NaviComp from './components/NaviComp.vue';

export default {
  name: 'App',
  components: {
    FooterComp, NaviComp,
  },
  setup() {
    const name = ref(0);
    return {
      name,
    };
  },
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
