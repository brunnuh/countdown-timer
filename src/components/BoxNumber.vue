<template>
   <div class="container">
        <div class="box-container">
            <h3 class="number">
                <p v-if="parseInt(number) < 10 && typeText == 'SECONDS' || typeText == 'MINUTES'">0{{number}}</p>
                <P v-else>{{number}}</P>
            </h3>
        </div>
        <div class="text">
            {{typeText}}
        </div>
   </div>
</template>

<script>
export default {
    props:{
        number: {
            type: String,
            default: 0
        },
        typeText: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>

    .container{
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 200px;
    }
    .box-container{
        width: 150px;
        height: 150px;
        background-color: #2C2C44;
        box-shadow: 3px 10px rgba(0, 0, 0, 0.2) ;
        display: flex;
        flex-direction: column;
        align-items: center;
        border-radius: 10px;
    }

    .number > p{
        font-size: 80px;
        display: flex;
        align-items: center;
        color:#bb497a;
        font-weight: bold;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }

    .text{
        margin-top: 30px;
        font-weight: bolder;
        letter-spacing: 7px;
    
        color: #666373;
    }
</style>