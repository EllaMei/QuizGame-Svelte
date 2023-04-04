<script>
    import LoginPage from "./loginpage.svelte";
    import QuizStart from "./QuizStart.svelte";
    import Loginbutton from "./loginbutton.svelte";
    let admin_visibility = 0;
    let quiz_visibility = 0;
    let username;
    let password;

    function handleLogIn() {
        if (username === 'Admin' && password === 'password') {
            admin_visibility = 1
        }
        else if (password === "password") {
            quiz_visibility = 1
        }
        else {
            alert("Incorrect username or password")
        }
        
    }

    function handleLogOut() {
        admin_visibility = 0
        quiz_visibility = 0
        question_visibility = 0
    }
</script>


{#if admin_visibility === 1}
    <!-- Show Admin Page Here -->
    <Loginbutton on:click={handleLogOut} login="Log Out"/>
{:else if quiz_visibility === 1}
    <QuizStart/>
    <Loginbutton on:click={handleLogOut} login="Log Out"/>
{:else}
    <LoginPage on:click={handleLogIn} bind:username={username} bind:password={password} />
{/if}

