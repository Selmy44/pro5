# pro5
this a pro 5
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }

        .calculator {
            width: 300px;
            margin: 50px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
        }

        .input {
            width: 100%;
            height: 40px;
            margin-bottom: 10px;
            font-size: 18px;
            text-align: right;
        }

        .button {
            width: 70px;
            height: 70px;
            font-size: 24px;
            margin: 5px;
            cursor: pointer;
        }

        .button.operator {
            background-color: #f0ad4e;
        }

        .button.equal {
            background-color: #5bc0de;
        }

        .button.clear {
            background-color: #d9534f;
        }
    </style>
</head>

<body>
    <div class="calculator">
        <input class="input" id="display" disabled>
        <br>
        <button class="button" onclick="appendToDisplay('1')">1</button>
        <button class="button" onclick="appendToDisplay('2')">2</button>
        <button class="button" onclick="appendToDisplay('3')">3</button>
        <button class="button operator" onclick="appendToDisplay('+')">+</button>
        <br>
        <button class="button" onclick="appendToDisplay('4')">4</button>
        <button class="button" onclick="appendToDisplay('5')">5</button>
        <button class="button" onclick="appendToDisplay('6')">6</button>
        <button class="button operator" onclick="appendToDisplay('-')">-</button>
        <br>
        <button class="button" onclick="appendToDisplay('7')">7</button>
        <button class="button" onclick="appendToDisplay('8')">8</button>
        <button class="button" onclick="appendToDisplay('9')">9</button>
        <button class="button operator" onclick="appendToDisplay('*')">*</button>
        <br>
        <button class="button clear" onclick="clearDisplay()">C</button>
        <button class="button" onclick="appendToDisplay('0')">0</button>
        <button class="button operator" onclick="calculate()">=</button>
        <button class="button operator" onclick="appendToDisplay('/')">/</button>
    </div>

    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            try {
                var result = eval(document.getElementById('display').value);
                document.getElementById('display').value = result;
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>
</body>

</html>
