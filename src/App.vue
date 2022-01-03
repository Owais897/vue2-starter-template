<template>
  <div id="app">
    <div class="center">
      <el-menu
        :default-active="activeIndex"
        class="el-menu-demo"
        mode="horizontal"
      >
        <el-menu-item index="/"
          ><router-link to="/">Home</router-link></el-menu-item
        >

        <el-menu-item index="/about">
          <router-link to="/about">About</router-link></el-menu-item
        >
      </el-menu>
    </div>
    <div class="line"></div>
    <div class="square">
      <router-view />
    </div>
  </div>
</template>
<script>
export default {
  name: "App",
  mounted() {
    this.activeIndex = this.$route.path;
  },

  data() {
    return {
      activeIndex: "/",
    };
  },
};
</script>
<style>
body {
  margin: 0;
  padding: 0;
  background: #e6e6e6;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.center {
  display: flex;
  justify-content: center;
  width: 100% !important;
  background-color: white;
}
.square {
  margin-top: 70px;
}
</style>
