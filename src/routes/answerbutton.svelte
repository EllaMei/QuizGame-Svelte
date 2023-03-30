<script>
    // Defining variable, giving default value and allowing value to be filled by other components
    export let answer = 'answer';
</script>

<style>
    .button {
    /*Button background color*/
    background-color: green;
    /*Button text color*/
    color: white;
    /*Button space around text*/
    padding: 15px 32px;
    /*Centering text inside button*/
    text-align: center;
    /*Button rounding*/
    border-radius: 8px;
    /*Button border*/
    border: 2px solid black;
    text-decoration:none;
    display: inline-block;
    /*Text size*/
    font-size: 20px;
    /*Width of the button*/
    width: 25%;
    /*How fast the color changes*/
    margin: 20px;
    height: 85px;
  }
</style>

<!-- Creating a button with a on:click event that will be used by a different component and a text that will be defined by another component with the default being 'answer' -->
<button class="button" on:click>{answer}</button>