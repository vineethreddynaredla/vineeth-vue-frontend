<template>

    <div :class="restaurent.popularDishAvailability ? 'true': 'false' ">
        <h2>{{restaurent.nameOfRestaurent}}</h2>
        <div class = "A">
            <p>
                <ul>
                    <li><b>CONTENTS</b></li>
                    &nbsp;&nbsp;<u>Established Date:</u> {{restaurent.establishedDate}}<br>
                    <!-- &nbsp;&nbsp;<u>Restaurent Info:</u> <a href="{{restaurent.restInfo}}">{{restaurent.restInfo}}</a><br> -->
                    &nbsp;&nbsp;<u>Restaurent Info:</u> <a href="{{restaurent.restInfo}}" target="_blank">{{restaurent.restInfo}}</a><br>
                    <!-- <a href="{{restaurent.restInfo}}" target="_blank">{{restaurent.restInfo}}</a> -->
                    <!-- <iframe src="{{restaurent.restInfo}}" width="100%" height="500px"></iframe> -->
                    <!-- <a href="{{restaurent.restInfo}}" target="_blank">{{restaurent.restInfo}}</a> -->
                    &nbsp;&nbsp;<u>Restaurent Rating:</u> {{restaurent.rating}}<br>
                    &nbsp;&nbsp;<u>availability:</u> {{restaurent.popularDishAvailability}}<br>
                </ul>
            </p>
        </div>
    </div>
</template>

<script>

export default{
    name: 'MyRestaurentList',
    props:{
        restaurent: Array
    }  
}
</script>

<style scoped>

a{
  color: rgb(137, 175, 68) 
}


h4{
    margin: 2px;
}

div{
    background-color: #96668e;
    color: rgb(14, 15, 15);
    padding: 1em;
}

.true{
    background-color: #25b5a4 !important;

}
.false{
    background-color: #c93030 !important;
}


</style>