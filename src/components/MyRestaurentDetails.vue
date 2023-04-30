<template>
    <div class="RestaurentDetails">
        <div v-for="restaurent in restaurents" :key="restaurent.id" >     
               <MyRestaurentList :restaurent="restaurent"/>
        </div>
    </div>

</template>

<script>
import MyRestaurentList from "./MyRestaurentList.vue"
export default {
    name: 'MyRestaurentDetails',
    components: {
        MyRestaurentList
    },
    props:{
        restaurents: Array

    }
}


</script>


<style>
.RestaurentDetails{

    background-color:#c6beb8;
    border: 5px solid rgb(89, 66, 66);
    padding: 1em;
    color: rgb(64, 64, 145);
}

</style>