
<script>
import VueClock from "./components/VueClock.vue"
export default{
name: "App",
components: {
  VueClock
}
}

</script>

<template>
  <div class="container">
    <VueClock/>
  </div>

</template>

<style>
body{
    background-color: black;
}
.container {
  display:flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}

</style>

