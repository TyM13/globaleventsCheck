<template>
  <div>
    <section v-for="user in users" :key="user">
      <h1 @click="highlight_username">{{ user }}</h1>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    highlight_username() {
      this.$root.$emit(`user_clicked`, this.users);
    },
  },

  data() {
    return {
      users: [`user one`, `user two`, `user three`],
    };
  },
};
</script>

<style scoped>
</style>