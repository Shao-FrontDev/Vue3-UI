<template>
  <div>导航栏</div>
  <router-link to="/home">Home</router-link>
  <router-link to="/">About</router-link>
  <hr />
  <router-view></router-view>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>
