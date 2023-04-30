<template>
    <div>
        <h1>{{titleName}}</h1>
        <h2>{{details}}</h2>
    </div>
    </template>
    
    <script>
    export default {
        name: 'MyHeader',
        props:{
            titleName: String,
            details:String
        }   
    }
    </script>
    
    <style scoped>
    div{
        text-align: center;
        border: 5px solid rgb(240, 234, 234);
        padding: 3px;
        background-color: #206648;
    }
    h1{
        color: rgb(238, 226, 226);
    }
    
    </style>