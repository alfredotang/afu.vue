<template>
  <div class="home">
    <img alt="Vue logo" src="@src/assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from '@src/components/HelloWorld.vue';

const Home = new Vue({
  components: {
    HelloWorld
  }
});

export default Home;
</script>
