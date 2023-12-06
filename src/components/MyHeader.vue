<template>
    <div>
        <h1> {{flightName}} </h1>
        <h1> {{airport}} </h1>
        <h4> {{yourName}} </h4>
        <h4>{{ airline }}</h4>
    </div>
    </template>
    
    <script>
    
    export default{ // Exporting Default Object
        name: 'MyHeader',
        props:{ 
    
            flightName:String,
            airport:String,
            yourName: String,
            airline:String
            
        
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
        color: rgb(255, 0, 0);
    }
    
    </style>