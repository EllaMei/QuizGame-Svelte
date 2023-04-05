<script>
    // Importing component
    import Answer_button from "./answerbutton.svelte";
    // Defining variable, giving default values and allowing values to be filled by other components
    export let answer = ['answer','answer','answer','answer'];
    
</script>

<style>
    .buttons {
    /*Puts buttons in the center of screen horizontally*/
    display: flex;
    justify-content: space-around;
}
</style>

<!--Seperating buttons to make two different lines. 
    Passing on:click event on to next component
    Giving each button a different answer based on the answer array -->
    
<div class="buttons">
    <Answer_button on:click answer = {answer[0]} />
    <Answer_button on:click answer = {answer[1]}/>
</div>
<div class="buttons">
    <Answer_button on:click answer = {answer[2]}/>
    <Answer_button on:click answer = {answer[3]}/>
</div>