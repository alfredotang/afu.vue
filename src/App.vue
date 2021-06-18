<template>
  <div id="app">
    <Header />
    <router-view />
  </div>
</template>
<script>
import Header from '@src/layout/Header.vue';
export default {
  components: {
    Header
  }
};
</script>
