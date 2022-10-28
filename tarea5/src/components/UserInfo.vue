<template>
  <li class="list-group-item">
    <h2>{{ user.name.title }} {{ user.name.first }} {{ user.name.last }}</h2>
    <h4>{{ user.gender }}</h4>
    <h4>{{ user.location.country }}</h4>
    <img :src="user.picture.medium" />
    <h4 v-if="user.dob.age > 18">+18</h4>
    <h4 v-else>-18</h4>

    <button
      v-if="user.gender === `female`"
      class="btn btn-danger"
      @click="isHidden = !isHidden"
    >
      More Info
    </button>
    <button
      v-if="user.gender === `male`"
      class="btn btn-primary"
      @click="isHidden = !isHidden"
    >
      More Info
    </button>
    <div v-if="!isHidden">
      <h4>{{ user.email }}</h4>
      <h4>{{ user.location.city }}</h4>
    </div>
  </li>
</template>

<script>
export default {
  name: "UserInfo",
  props: {
    user: Object,
  },
  data() {
    return {
      isHidden: true,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
