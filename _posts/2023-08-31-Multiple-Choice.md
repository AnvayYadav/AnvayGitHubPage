---
toc: true
comments: false
layout: hacks
title: Python Multiple Choice
description: Multiple choice quiz that tests your knowledge on python.
type: hacks
courses: { compsci: {week: 1} }
---

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anvay's Python Quiz</title>
<style>
  body {
    font-family: Arial, sans-serif;
  }
  .quiz-container {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  .question {
    font-weight: bold;
    margin-bottom: 10px;
  }
  .options label {
    display: block;
    margin-bottom: 5px;
    cursor: pointer;
  }
</style>
</head>
<body>
<div class="quiz-container">
  <h1>Anvay's Python Quiz</h1>
  <div class="question">1. How do I change my directory to home?</div>
  <div class="options">
    <label><input type="radio" name="q1" value="a"> a) cd home</label>
    <label><input type="radio" name="q1" value="b"> b) cd ~</label>
    <label><input type="radio" name="q1" value="c"> c) cd vscode</label>
    <label><input type="radio" name="q1" value="d"> d) cd_home</label>
  </div>
  
  <div class="question">2. Which python command creates a loop, which stops after a condition is met"?</div>
  <div class="options">
    <label><input type="radio" name="q2" value="a"> a) for</label>
    <label><input type="radio" name="q2" value="b"> b) while</label>
    <label><input type="radio" name="q2" value="c"> c) repeating</label>
    <label><input type="radio" name="q2" value="d"> d) check</label>
  </div>
  
  <div class="question">3. How to generate an input box for the user, in python?</div>
  <div class="options">
    <label><input type="radio" name="q3" value="a"> a) print("abcd")</label>
    <label><input type="radio" name="q3" value="b"> b) ask("abcd")</label>
    <label><input type="radio" name="q3" value="c"> c) input(“abcd”)</label>
    <label><input type="radio" name="q3" value="d"> d) prompt("abcd")</label>
  </div>
  
  <button id="submit-button">Submit</button>
  <div id="result"></div>
</div>

<script>
  const submitButton = document.getElementById("submit-button");
  const resultDiv = document.getElementById("result");

  submitButton.addEventListener("click", () => {
    const selectedAnswers = [];
    const questions = document.querySelectorAll(".options");

    questions.forEach((question, index) => {
      const selectedOption = question.querySelector("input[type=radio]:checked");
      if (selectedOption) {
        selectedAnswers.push(selectedOption.value);
      } else {
        selectedAnswers.push(null);
      }
    });

    const correctAnswers = ["b", "b", "c"]; // Replace with the correct answers
    let score = 0;

    selectedAnswers.forEach((answer, index) => {
      if (answer === correctAnswers[index]) {
        score++;
      }
    });

    const totalQuestions = correctAnswers.length;
    const resultText = `You scored ${score} out of ${totalQuestions}`;
    resultDiv.textContent = resultText;
  });
</script>
</body>
</html>

