<template>
  <ul class="list-group">
    <UserInfo v-for="user in users" :user="user" :key="user.id.value" />
  </ul>
</template>

<script>
import UserInfo from "./components/UserInfo.vue";
import Users from "./assets/json/users.json";

export default {
  name: "App",
  components: {
    UserInfo,
  },
  data() {
    return {
      users: Users,
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
  margin-top: 60px;
}
</style>
