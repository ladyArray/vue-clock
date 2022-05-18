<script>
export default
{name: "VueClock",
data (){
  return{
    hours: '--',
    minutes: '--',
    seconds: '--'
  }
},

  mounted(){
    setInterval(()=> this.updateClock(), 1000)
  },
  methods: {
    addLoadingZeros(num, totalLength){
      return String(num).padStart(totalLength, '0');
    },
    updateClock(){
      let date = new Date();
      this.hours = this.addLoadingZeros(date.getHours(), 2);
      this.minutes = this.addLoadingZeros(date.getMinutes(), 2);
      this.seconds = this.addLoadingZeros(date.getSeconds(), 2);

    }
  }
}
</script>

<template>
<div class="container">
  <div class="clock">
  <p>{{hours}} : {{minutes}} : {{seconds}}</p>
  </div>
</div>

</template>

<style>


.container{
  display: flex;
  color: white;
}

.clock{
  font-family: 'Orbitron', monospace;
  font-size: 75px;
  width: 500px;
  display: inline-block;
  text-shadow: 0px 0px 8px greenyellow;
}

</style>

