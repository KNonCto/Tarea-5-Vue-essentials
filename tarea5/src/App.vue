<template>
  <img alt="Vue logo" src="./assets/img/logo.png" />
  <UserInfo v-for="user in users" :user="user" :key="user.id.value" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import UserInfo from "./components/UserInfo.vue";
import Users from "./assets/json/users.json";

export default {
  name: "App",
  components: {
    HelloWorld,
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
