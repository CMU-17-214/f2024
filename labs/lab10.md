# Lab 10: Introduction to React.js

React is a declarative, efficient, and flexible JavaScript library for building interactive and dynamic user interfaces. 
It lets you compose complex UIs from small and isolated pieces of code - components. 
In this lab, you will learn the fundamentals of React.js and create an interactive quiz application.

## Deliverables
- [ ] Separate the core and GUI components.
- [ ] Enhance the UI to highlight the selected answer for a more user appealing experience.
- [ ] Extend the Quiz component to make the "Next Question" button functional. It should move to the next question and display the total score when all questions have been answered.

## Instructions

### Setup
Fork and clone the Quiz App repository from: [https://github.com/CMU-17-214/f24-lab10](https://github.com/CMU-17-214/f24-lab10) and run

```
npm install
npm start
```
![Local Image](https://github.com/CMU-17-214/f24-lab10/blob/main/src/image/starterPic.png)

This will start the front-end server. You will be able to see a simple quiz GUI from the link http://localhost:3000/. You can update the front-end code as the server is running in the development mode (i.e., `npm start`). It will automatically recompile and reload.

In this starter code, you are provided with a Quiz class component.
The initial state includes a sample question, answer options, and a `selectedAnswer` value.
The `handleOptionSelect` function allows selecting an answer option and updates the `selectedAnswer` in the component's state.
The component uses JSX to return HTML-like markup directly, displaying the question, answer options, and the selected answer within the component's return statement.
> JSX is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file.

---

### Task 1: Core-GUI Separation 
You will notice the `Quiz.tsx` file contains both the logic and the graphical user interface (GUI) of the quiz application. 
As the project grows, it's best practice to separate the application's core logic from its GUI components.

We've provided a core implementation at [src/core/QuizCore.ts](https://github.com/CMU-17-214/f24-lab10/blob/main/src/core/QuizCore.ts). This core module encapsulates critical quiz operations. It's designed to manage the quiz's functionality independently of the GUI. Your task is to integrate this core with the user interface `Quiz.tsx`. Ensure that your GUI component correctly reflects the data from the QuizCore. Update your component to display the questions and answer options provided by the core. Take care to observe and update the user's selected options and other state changes effectively.
<br><br>
### Task 2: Enhance User Experience
The starter code displays the user’s selection as text directly and your task is to improve the user experience by making it visually engaging. You have the creative freedom to design how the selected option is displayed.
> Hint: Change CSS to highlight or apply a border to the selected option.
<br><br>
### Task 3: Manage User Interaction and Scoring
In the initial implementation, the "Next Question" button remains inactive – it neither progresses to the next question nor displays the final score upon completing all the questions. Your task is to make the "Next Question" button functional and display the total score when all questions have been answered.

When a question is displayed, ensure that the "Next Question" button can take users to the following question. To achieve this, you should check if there is a next question available in the quiz. You can utilize the `hasNextQuestion()` method provided in the core logic.

When all questions have been answered, "Next Question" button should become "Submit" button, and upon clicking it, display the total score. For simplicity, each question in the quiz is worth a score of 1 if answered correctly. You can utilize the `getScore()` method provided in the core logic.
