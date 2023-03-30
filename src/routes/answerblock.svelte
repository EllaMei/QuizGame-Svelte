<script>
    import Answer_button from "./answerbutton.svelte";
    export let answer = ['answer','answer','answer','answer'];
    
</script>

<style>
    .buttons {
    /*Puts buttons in the center of screen horizontally*/
    display: flex;
    justify-content: center;
}

</style>
<div class="buttons">
    <Answer_button on:click answer = {answer[0]} />
    <Answer_button on:click answer = {answer[1]}/>
</div>
<div class="buttons">
    <Answer_button on:click answer = {answer[2]}/>
    <Answer_button on:click answer = {answer[3]}/>
</div>