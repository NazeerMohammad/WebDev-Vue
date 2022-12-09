<template>
    <div>
        <h2>{{titleName}}</h2>
    </div>
</template>
    
    <script>
    export default {
        name: 'MyHeader',
        props:{
            titleName: String,
        }   
    }
    </script>
    
    <style scoped>
    div{
        text-align: center;
        border: 5px solid black;
        padding: 2px;
        background-color: rgb(72, 52, 152);
    }
    h2{
        color: rgb(170, 103, 168);
    }
    
    </style>