<template>
  <div class="info-container">
      <h1>WE´RE LAUNCHING SOON</h1>
      <div class="schedule">
          <box-number number="08" typeText="DAYS"/>
          <box-number number="23" typeText="HOURS"/>
          <box-number :number="minutes.toString()" typeText="MINUTES"/>
          <box-number :number="seconds.toString()" typeText="SECONDS"/>
      
      </div>
      
  </div>
</template>

<script>
import BoxNumber from './BoxNumber.vue'

export default {
    data() {
        return {
            data: new Date(),
            seconds: 0,
            minutes: 0,
            hours: 0,
            days: 0
        }
    },
    components:{
        BoxNumber
    },
    created() {
      var vm = this
      setInterval(function(){
        if(vm.seconds < 59){
            vm.seconds++
        }else{
            vm.seconds = 0
            if(vm.minutes < 59){
                vm.minutes ++
            }else{
                vm.minutes = 0
            }
        }
      }, 1000)
    }
}
</script>

<style scoped>
    .info-container{
        grid-area: INF;
        color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
        background-image: url("../assets/bg-stars.svg");
    }
    h1{
        margin-top: 100px;
        height: 30px;
        font-size: 20px;
        letter-spacing: 7px;
        font-weight: bolder;
    }
    .schedule{
        margin-top: 100px;
        display: flex;
        height: 200px;
        width: 680px;
        justify-content: space-between;
    }

</style>