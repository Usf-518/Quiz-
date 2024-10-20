# Quiz<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Metallic & Non-metallic Property Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .quiz-container {
            max-width: 600px;
            margin: auto;
        }
        h1 {
            text-align: center;
        }
        .question {
            margin-bottom: 20px;
        }
        .result {
            display: none;
            font-size: 20px;
            font-weight: bold;
            color: green;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <h1>Metallic & Non-metallic Property Quiz</h1>
        <form id="quizForm">
            <div class="question">
                <p>1. Metals tend to have how many electrons in their outermost energy level?</p>
                <label><input type="radio" name="q1" value="A"> Less than 4</label><br>
                <label><input type="radio" name="q1" value="B"> More than 4</label><br>
                <label><input type="radio" name="q1" value="C"> Exactly 4</label>
            </div>
            <div class="question">
                <p>2. During a chemical reaction, non-metals tend to:</p>
                <label><input type="radio" name="q2" value="A"> Lose electrons and become positive ions</label><br>
                <label><input type="radio" name="q2" value="B"> Gain electrons and become negative ions</label><br>
                <label><input type="radio" name="q2" value="C"> Do nothing</label>
            </div>
            <div class="question">
                <p>3. Which elements do not usually enter into chemical reactions?</p>
                <label><input type="radio" name="q3" value="A"> Metals</label><br>
                <label><input type="radio" name="q3" value="B"> Non-metals</label><br>
                <label><input type="radio" name="q3" value="C"> Noble gases</label>
            </div>
            <div class="question">
                <p>4. Metalloids can have how many electrons in their outermost energy level?</p>
                <label><input type="radio" name="q4" value="A"> 3, 4, 5, or 6</label><br>
                <label><input type="radio" name="q4" value="B"> 1 or 2</label><br>
                <label><input type="radio" name="q4" value="C"> Always 6</label>
            </div>
            <button type="button" onclick="submitQuiz()">Submit</button>
        </form>
        <div class="result" id="result"></div>
    </div>

    <script>
        function submitQuiz() {
            const form = document.getElementById('quizForm');
            let score = 0;

            const answers = {
                q1: 'A',
                q2: 'B',
                q3: 'C',
                q4: 'A'
            };

            for (let i = 1; i <= 4; i++) {
                const userAnswer = form['q' + i].value;
                if (userAnswer === answers['q' + i]) {
                    score++;
                }
            }

            const resultDiv = document.getElementById('result');
            resultDiv.innerText = `You scored ${score} out of 4.`;
            resultDiv.style.display = 'block';
        }
    </script>
</body>
</html>
