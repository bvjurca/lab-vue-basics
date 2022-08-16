<template>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      <!--Iteration 2a-->
      <p> Showing arithmetics in a moustache syntax: {{ 2 + 2 * 2 }} </p>
      <!--Iteration 3-->
      <button @click="btnClick++">Click me</button>
      <div v-if="btnClick %2 == 1">
        <p>🎉 Iteration 3 complete 🎉</p>
      </div>
    </nav>
</template>

<script>
import { ref } from 'vue';

const btnClick = ref(false);
export default {
  data() {
    return {
      btnClick: 0,
    };
  },

};

</script>

<style scoped>

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

</style>
