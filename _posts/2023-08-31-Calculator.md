---
toc: true
comments: false
layout: post
title: Calculator
description: Example Blog!!!  This shows planning and notes from hacks.
type: hacks
courses: { compsci: {week: 2} }
---


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
    #calculator {
        width: 300px;
        margin: 0 auto;
        padding: 20px;
        border: 1px solid #ccc;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    input[type="text"] {
        width: 100%;
        margin-bottom: 10px;
        padding: 10px;
        font-size: 18px;
    }
    button {
        width: 50px;
        height: 50px;
        font-size: 18px;
        margin: 5px;
    }
</style>
</head>
<body>
<div id="calculator">
    <input type="text" id="display" readonly>
    <button onclick="appendNumber('7')">7</button>
    <button onclick="appendNumber('8')">8</button>
    <button onclick="appendNumber('9')">9</button>
    <button onclick="appendOperator('+')">+</button>
    <br>
    <button onclick="appendNumber('4')">4</button>
    <button onclick="appendNumber('5')">5</button>
    <button onclick="appendNumber('6')">6</button>
    <button onclick="appendOperator('-')">-</button>
    <br>
    <button onclick="appendNumber('1')">1</button>
    <button onclick="appendNumber('2')">2</button>
    <button onclick="appendNumber('3')">3</button>
    <button onclick="appendOperator('*')">*</button>
    <br>
    <button onclick="appendNumber('0')">0</button>
    <button onclick="clearDisplay()">C</button>
    <button onclick="calculate()">=</button>
    <button onclick="appendOperator('/')">/</button>
</div>

<script>
    let displayValue = '';

    function appendNumber(number) {
        displayValue += number;
        updateDisplay();
    }

    function appendOperator(operator) {
        displayValue += operator;
        updateDisplay();
    }

    function clearDisplay() {
        displayValue = '';
        updateDisplay();
    }

    function calculate() {
        try {
            displayValue = eval(displayValue);
            updateDisplay();
        } catch (error) {
            displayValue = 'Error';
            updateDisplay();
        }
    }

    function updateDisplay() {
        document.getElementById('display').value = displayValue;
    }
</script>
</body>
</html>



