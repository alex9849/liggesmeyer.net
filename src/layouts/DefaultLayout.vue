<template>
  <div class="wrapper">
    <div class="wallpaper"></div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout"
}
</script>

<style scoped>
.wrapper {
  background-color: #00bcf1;
  background-image: linear-gradient(to bottom right, #00bcf1, #180CAC);
  font-family: "Work sans", sans-serif;
  color: #fff;
  font-size: 16px;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  line-height: 1.5;
  min-height: 100vh;
  min-width: 300px;
  overflow-x: hidden;
  text-shadow: 0 3px 5px rgba(0, 0, 0, 0.1);
}
.wallpaper {
  display: block;
  height: 100%;
  left: 0;
  top: 0;
  width: 100%;
  background-image: url('../assets/chicago.jpg');
  background-position: center;
  background-size: cover;
  opacity: 0.2;
  position: fixed;
}
</style>