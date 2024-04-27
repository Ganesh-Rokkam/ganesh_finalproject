<template>
<div><FitnessHead /></div>
    
    <div class="div-list" v-for="fitness of fitnessData" :key="fitness.Exercise_id" >
       <SingleFitness :fitness=fitness />
    </div>
</template>

<script>
import FitnessHead from './FitenessHead.vue'
import SingleFitness from './SingleFitness.vue'

export default {
    name: 'FitnessList',
    props:{
        fitnessData: Array
    },
    components:{
        FitnessHead,
        SingleFitness
    }
    
}
</script>
<style scoped>

</style>
