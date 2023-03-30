<script>
    export let questions;
    export let correct_answers;
    export let incorrect_answers;
    
    import {createEventDispatcher} from "svelte";
    const dispatch = createEventDispatcher();

    import Answerblock from "./answerblock.svelte";
    export let i = 0

    

    

</script>

<style>
    /*Question style*/
h2 {
    text-align: center;
    font-size: 28px;
}
</style>

    <h2>Question {i+1}/{questions.length}</h2>
    <h2>{questions[i]}</h2>
    
    <Answerblock on:click answer={ [
        correct_answers[i],
        incorrect_answers[i*3],
        incorrect_answers[(i*3+1)],
        incorrect_answers[(i*3+2)]
    ]}/> 