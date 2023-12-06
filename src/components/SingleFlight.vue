<template>
    

    <div >

                        <h2>{{flight.flightName}}</h2>
                        <h4> {{flight.airline}}</h4>
                        <h4>{{ flight.price }}</h4>
                        <h4>{{ flight.departureTime }}</h4>
                
    </div>
</template>

<script>

export default{
    name: 'SingleFlight',
    props:{
        flight: Array
    }
}
</script>

<style scoped>

.green{
    background-color: green;
}

h4{
    margin: 2px;
}

div{
    background-color: #9effa6;
    color:BLUE;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.red{
background-color: orangered !important;

}


</style>