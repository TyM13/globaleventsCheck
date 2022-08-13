<template>
  <div>
    <user-list>
      <h1 ref="clicked" @user_clicked="show_username"></h1>
    </user-list>
  </div>
</template>

<script>
export default {
  methods: {
    show_username(user) {
      this.$refs[`clicked`] = user;
    },
  },

  mounted() {
    this.$root.$on(`user_clicked`, this.show_username);
  },
};
</script>

<style scoped>
</style>