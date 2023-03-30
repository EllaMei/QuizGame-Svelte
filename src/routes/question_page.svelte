<script>
    // Defining variables and allowing them to be filled by other components
    export let questions;
    export let correct_answers;
    export let incorrect_answers;
    export let i = 0
    
    //Importing component 
    import Answerblock from "./answerblock.svelte";
</script>

<style>
    /*Question style*/
h2 {
    text-align: center;
    font-size: 28px;
}
</style>

<!-- Question number and number of total questions -->
    <h2>Question {i+1}/{questions.length}</h2>
    <!-- Asking the question -->
    <h2>{questions[i]}</h2>
    
    <!-- Using component,
        passing on on:click event to another component
        Giving values for the different buttons to show
     -->
    <Answerblock on:click answer={ [
        correct_answers[i],
        incorrect_answers[i*3],
        incorrect_answers[(i*3+1)],
        incorrect_answers[(i*3+2)]
    ]}/> 