<!-- eslint-disable vuejs-accessibility/label-has-for -->
<template>
  <NaviComp />
  <!--Iteration 2b-->
  <div id="iteration-two">
    <label for="text">Something to do with {{ textInInput }} </label>
    <input v-model="textInInput" placeholder="Type here..."/>
  </div>
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
    const textInInput = ref('');
    return {
      textInInput,
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

input {
  display: block;
  margin: auto;
}

#iteration-two {
  margin-bottom: 100px;
}

</style>
