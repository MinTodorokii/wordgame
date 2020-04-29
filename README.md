<html>
    <head>
        <meta charset="utf-8">
        <title>Project: Word game </title>
        <style>
            body {
                font-family: Arial, sans-serif;
            }
            form {
                font-size: 1.5em;
            }
            .scrambled, input, button {
                font-family: monospace;
                font-size: 2em;
            }
            
        </style>
    </head>
    <body>
    
    <h1>Word game!</h1>
    <form id="joke-form">
        <label>
            Unscramble these letters to form a word:<Br>
            <span class="scrambled">REYJUQ</span>
            <br>
            
            <input type="text" size="10">
            
        </label>
        <button type="submit">Check</button>
    </form>
    
    <div id="result"></div>
    

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
    <script>

        $("#joke-form").on("submit", function(event){
            event.preventDefault();
            var $answer =$("#joke-form");
            var answer =$answer.val();
            console.log(answer);

       
        if (answer === "JQUERY") {
  $("#result").text("YAYYYYYY U GOT ITTTT");
} else {
  $("#result").text("Oppssieeee, try again!");
}
        });
        // when the user submits the form,
        //   check that their answer is correct
        //   and show them appropriate message
    </script>
    </body>
</html>
