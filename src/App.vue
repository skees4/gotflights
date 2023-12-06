<template>

  
  <MyHeader flightName="AMERICAN AIRLINES"   yourName="List of flights" airline=" AIRPORT : JFK"/> 
  <FlightBox :flights=flights />
 
</template>

<script>

import MyHeader from './components/MyHeader.vue'
import FlightBox from './components/FlightBox.vue'


export default{
  name: 'App',

  
  components:{
    MyHeader,
    FlightBox
  },
  data(){
    return {
      flights: []
    }
  },
  methods:{
    //promoises
    async fetchflights(){
      const res = await fetch("https://saik.onrender.com/api");
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.flights = await this.fetchflights();
  }
}
</script>


<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid  RED;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>
