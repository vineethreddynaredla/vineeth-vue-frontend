<template>
    <div>
        <h4> {{About}} </h4>
    </div>
    
</template>

<script>
export default {
    name: 'MyAbout',
    props:{
        About: String
    }
}
</script>

<style scoped>
div{
    text-align: center;
    border: 5px solid rgb(242, 234, 234);
    background-color: #61b2f4;
    padding: 10px;
}
</style>