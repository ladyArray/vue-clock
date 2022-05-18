
<script>
export default
{name: "VueClock",
data (){
  return{
    hours: new Date().getHours(),
    minutes: new Date().getMinutes(),
    seconds: new Date().getSeconds()
  }
},

}
</script>

<template>
<div>
  <span class="hours">{{hours}}:</span>
  <span class="minutes">{{minutes}}:</span>
  <span class="seconds">{{seconds}}</span>
</div>

</template>

<style>

</style>

