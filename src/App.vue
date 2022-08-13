<template>
  <div id="app">
    <user-list> </user-list>
  </div>
</template>

<script>
import UserList from "@/components/UserList.vue";
export default {
  name: "App",
  components: {
    UserList,
  },
};
</script>

<style>
</style>
