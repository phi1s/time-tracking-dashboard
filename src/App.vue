<template>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;500&display=swap"
    rel="stylesheet"
  />
  <TimeTrackingDashboard />
</template>

<script>
import TimeTrackingDashboard from "./components/TimeTrackingDashboard.vue";

export default {
  name: "App",
  components: {
    TimeTrackingDashboard,
  },
};
</script>

<style>
#app {
  font-family: "Rubik", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
  background-color: #0e1323;
  text-align: center;
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
