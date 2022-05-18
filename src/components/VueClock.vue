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
@import url('http://fonts.cdnfonts.com/css/led-digital-7');

.clock{
  font-family: 'LED Digital 7';
  font-size: 13vh;
  color:rgb(0, 0, 0);
  margin: 0 5% 30% 0;
}

.clock:hover{
  text-shadow: 0px 0px 8px rgb(255, 255, 255);
}

</style>
