# AfreenTech
<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
</head>
<body>
    <h2>Simple Calculator</h2>
    <form name="calculator">
        <input type="text" name="display" id="display" disabled>
        <br>
        <button type="button" onclick="clearDisplay()">C</button>
        <button type="button" onclick="appendToDisplay('7')">7</button>
        <button type="button" onclick="appendToDisplay('8')">8</button>
        <button type="button" onclick="appendToDisplay('9')">9</button>
        <button type="button" onclick="appendToDisplay('+')">+</button>
        <br>
        <button type="button" onclick="appendToDisplay('4')">4</button>
        <button type="button" onclick="appendToDisplay('5')">5</button>
        <button type="button" onclick="appendToDisplay('6')">6</button>
        <button type="button" onclick="appendToDisplay('-')">-</button>
        <br>
        <button type="button" onclick="appendToDisplay('1')">1</button>
        <button type="button" onclick="appendToDisplay('2')">2</button>
        <button type="button" onclick="appendToDisplay('3')">3</button>
        <button type="button" onclick="appendToDisplay('*')">*</button>
        <br>
        <button type="button" onclick="appendToDisplay('0')">0</button>
        <button type="button" onclick="appendToDisplay('.')">.</button>
        <button type="button" onclick="calculate()">=</button>
        <button type="button" onclick="appendToDisplay('/')">/</button>
    </form>

    <script>
        function appendToDisplay(value) {
            document.calculator.display.value += value;
        }

        function clearDisplay() {
            document.calculator.display.value = '';
        }

        function calculate() {
            try {
                document.calculator.display.value = eval(document.calculator.display.value);
            } catch (error) {
                document.calculator.display.value = 'Error';
            }
        }
    </script>
</body>
</html>

