<template>
   
    <div class="Flight-Box">
    <div v-for="flight of flights.flights" :key="flight._id" >

     
       <SingleFlight :flight=flight />

    </div>
   </div>
</template>
<script>
import SingleFlight from './SingleFlight.vue'

export default {
    name: 'FlightBox',
    props:{
        flights: Array
    },
    components:{
        SingleFlight
    }
    
}
</script>
<style scoped>

</style>
