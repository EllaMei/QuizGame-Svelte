<script>
    export let login;
</script>

<style>
    .login {
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
        font-size: 14px;
    }
</style>

<button class="login" on:click>{login}</button>