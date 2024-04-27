

<template>

    <div class="fitdata">
        <h2>{{fitness.Workout_performed}}</h2>
        <h4 class="h"> Sets Completed : {{fitness.Sets_completed}}</h4>
        <h4 class="h"> No. of Repitions : {{fitness.Repetitions}}</h4>
        <h4 class="h"> Intensity : {{fitness.Intensity}}</h4>
        <h4 class="h"> Weights Lifted : {{fitness.Weight_lifted}}</h4>
        <h4 class="h"> Calories Burned : {{fitness.Calories_burned}}</h4>

    </div>
</template>

<script>
export default{
    name: 'SingleFitness',
    props:{
        fitness: Object
    }
}
</script>

<style scoped>

.green{
    background-color: green;
}

.h{
    margin: 2px;
}


.fitdata{
    background-color: #139b59;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.red{
background-color: orangered !important;

}


</style>