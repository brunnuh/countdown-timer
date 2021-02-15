<template>
  <div class="info-container">
      <h1>WE´RE LAUNCHING SOON</h1>
      <div class="schedule">
          <box-number :number="data.getDate().toString()" typeText="DAYS"/>
          <box-number :number="data.getHours().toString()" typeText="HOURS"/>
          <box-number :number="data.getMinutes().toString()" typeText="MINUTES"/>
          <box-number :number="data.getSeconds().toString()" typeText="SECONDS"/>
      
      </div>
      
  </div>
</template>

<script>
import BoxNumber from './BoxNumber.vue'

export default {
    data() {
        return {
           data: new Date()
        }
    },
    components:{
        BoxNumber
    },
    created() {
      var vm = this

      setInterval(function(){
        vm.data = new Date()
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
     
        background-size: cover;
    }
    h1{
        margin-top: 100px;
        width: 100%;
        height: 30px;
        font-size: 20px;
        justify-content: center;
        display: flex;
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

    /** responsive */

    @media (max-width: 765px) {
        .schedule{
            width: 350px;
        }
        
        h1{
            font-size: 13px;
        }

    }

</style>