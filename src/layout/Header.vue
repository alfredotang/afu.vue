<template>
  <div class="header-container">
    <header class="header">
      <router-link
        v-for="(route, index) in routes"
        :to="route.path"
        :key="route.name"
        active-class="actived"
        exact="route.exact"
      >
        <span class="hover:text-green-500 route-name">{{ route.name }}</span>
        <span v-show="index !== routes.length - 1" class="px-3"
          >|</span
        ></router-link
      >
    </header>
  </div>
</template>
<script>
import Vue from 'vue';
import { routes } from '@src/router';
const Header = Vue.component('Header', {
  data() {
    return {
      routes
    };
  }
});
export default Header;
</script>
<style lang="postcss" scoped>
.header-container {
  --header-height: 80px;

  /* header height + padding-top + padding-bottom  */
  height: calc(var(--header-height) + 8px + 8px);
}

.header {
  @apply z-10 w-full;
  @apply border-b border-solid border-gray-200;
  @apply box-border p-2;
  @apply bg-white text-gray-500 antialiased;
  @apply flex justify-center items-center;
  height: var(--header-height);
}

.actived .route-name {
  @apply text-green-500;
}
</style>
