<script>
    // Defining variables and allowing them to be filled by other components
    export let questions = ['In which suburb is the Digital Traineeship Programme being run?','Which Train Station is the closest to the Cremorne Campus of Kangan Institute?','What is the capital city of Australia?'];
    export let i = 0
    export let answeredID;
    
    //Importing component 
    import Answerblock from "./answerblock.svelte";

    export let answers;
    export let answerID;

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
    <Answerblock answer = {answers} answerID = {answerID} bind:answeredID = {answeredID} on:click/> 
    