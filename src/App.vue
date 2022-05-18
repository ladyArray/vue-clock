
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
  background-image: url('/casio.jpg');
  background-position: 40%;
  background-size: 75vh;
    height: 100vh;
    background-repeat: no-repeat;
    justify-content: center;
    align-items: center;
    display:flex;
}

</style>

