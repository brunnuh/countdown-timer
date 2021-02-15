<template>
  <div class="pattern-hills">
      <div class="rows-icons">
        <a href=""><img src="@/assets/icon-facebook.svg" alt="facebook-to"></a>
        <a href=""><img src="@/assets/icon-pinterest.svg" alt="pinterest-to"></a>
        <a href=""><img src="@/assets/icon-instagram.svg" alt="instagram-to"></a>
      </div>
  </div>
</template>



<style scoped>
    .pattern-hills{
        grid-area: MNT;
       
        background-image: url("../assets/pattern-hills.svg");
        background-repeat: no-repeat;
        background-size: cover;
     
    }

    .rows-icons{
      display: flex;
      justify-content: center;
      align-items: center;
    }
    a{
      height: 24px;
      margin: 0 20px;
      margin-top: 50px;
      
    }
  
    a > img:hover{
      filter: sepia(100);
    }

   
</style>