<script>
    // Importing components
    import Startbutton from "./startbutton.svelte";
    // Defining Title variable
    let Title = "Kangan Quiz";
</script>

<style>
    .buttons {
    /*Puts buttons in the center of screen horizontally*/
    display: flex;
    justify-content: center;
}
/* Styling the title of Quiz */
    h1 {
        text-align: center;
        font-size:40px;
}
</style>

<!-- Creating title -->
<h1>{Title}</h1>
<!-- Using imported component and passing on:click event on to another component -->
<div class=buttons>
    <Startbutton on:click/>
</div>