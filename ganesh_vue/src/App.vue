<template>
  <!--Step 3 use the component-->
  <FitnessList :fitnessData = fitnessData />
</template>

<script>
// Step: 1 Import the components

import FitnessList from "./components/FitnessList.vue";

export default{
name: 'App',
  // Step 2: Register the components
  components:{
    FitnessList
  },
  data(){
    return {
      fitnessData: []
    }
  },
  methods:{
    //promoises
    async fetchFitnessData(){
      const res = await fetch("https://fitness-27v4.onrender.com/api");
      const data = await res.json()
      console.log(data)
      return data[0].fitnessDetails;
    }
  },
  async created(){
      this.fitnessData = await this.fetchFitnessData();
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
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>
