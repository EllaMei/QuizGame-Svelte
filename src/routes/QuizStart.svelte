<script>
    // Importing components
    import Question_page from "./question_page.svelte";
    import Homepage from "./homepage.svelte";
    import Exitquiz from "./exitquiz.svelte";

    // Defining variables
    export let question_visibility = 0
    let i = 0 
    let questions = ['In which suburb is the Digital Traineeship Programme being run?','Which Train Station is the closest to the Cremorne Campus of Kangan Institute?','What is the capital city of Australia?']
    let correct_answers = ['Cremorne','Richmond','Canberra']
    let incorrect_answers = ['South Yarra','Bendigo','Dandenong','Frankston','Cranburne','Berwick','Beaconsfield','Adelaide','Brisbane','Perth','Paris','Melbourne','Sydney','Newcastle']

    // import questions from "./question_page.svelte";

    $: answers =[
        correct_answers[i],
        incorrect_answers[i*3],
        incorrect_answers[(i*3+1)],
        incorrect_answers[(i*3+2)]
    ]
    let answers2;

    function shuffle(a) {
    var y, x, z;
    for (z = a.length - 1; z > 0; z--) {
        y = Math.floor(Math.random() * (z + 1));
        x = a[z];
        a[z] = a[y];
        a[y] = x;
    }
    return a;
    }

    // Function to start quiz
    function handleStartClick() {
        question_visibility = 1
        answers2 = shuffle(answers)
    }

    // Function to leave quiz early
    function handleQuizExit() {
        question_visibility = 0
        i=0
    }

    //Function to move to next question and end quiz at end
    function handleClickAnswer() {
        i += 1
        if (i >= questions.length) {
            alert("Quiz Finished")
            i = 0
            question_visibility=0
        }
        answers =[
            correct_answers[i],
            incorrect_answers[i*3],
            incorrect_answers[(i*3+1)],
            incorrect_answers[(i*3+2)]
        ]
        answers2 = shuffle(answers)
    }
</script>

<style>
    /* Background color */
    :global(body) {
        background-color: lightblue;
    }
</style>

<!-- Shows Question page or Homepage -->
{#if (question_visibility===1)}
    <Question_page on:click={handleClickAnswer} questions={questions} answers={answers2} i={i}/>
    <Exitquiz on:click={handleQuizExit}/>
{:else}
    <Homepage on:click={handleStartClick}/>
{/if} 
