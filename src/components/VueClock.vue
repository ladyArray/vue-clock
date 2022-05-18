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

  <div class="clock">
  <p>{{hours}}:{{minutes}}:{{seconds}}</p>
  </div>

</template>

<style>
@import url('http://fonts.cdnfonts.com/css/digital-7-mono');

.clock{
  font-family: 'Digital-7 Mono', monospace;
  font-size: 13vh;
  color:rgb(0, 0, 0);
  margin: 0 5% 30% 0;
  position: fixed;
}

.clock:hover{
  text-shadow: 0px 0px 8px rgb(255, 255, 255);
}

</style>
