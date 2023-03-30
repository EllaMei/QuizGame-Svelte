<script>
    import Startbutton from "./startbutton.svelte";
    

    
</script>

<style>
    .buttons {
    /*Puts buttons in the center of screen horizontally*/
    display: flex;
    justify-content: center;
}
h1 {
    text-align: center;
    font-size:40px;
}
</style>

<h1>Kangan Quiz</h1>
<div class=buttons>
    <Startbutton on:click/>
</div>