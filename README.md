# Ex04 Simple Calculator - React Project
## Date:14-03-2026
## Name : 
## Reg No :

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
JSX FILE 
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  const clearInput = () => {
    setInput("");
  };

  return (
    <div className="container">
      <div className="calculator">
        <h2>Simple Calculator</h2>

        <input
          type="text"
          value={input}
          readOnly
          className="display"
        />

        <div className="buttons">
          <button onClick={clearInput}>C</button>
          <button onClick={() => handleClick("/")}>/</button>
          <button onClick={() => handleClick("*")}>*</button>
          <button onClick={() => handleClick("-")}>-</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={calculate}>=</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("0")}>0</button>

          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>

      <footer>
        <p>Name: THARUN</p>
        <p>Register Number: YOUR_REGISTER_NUMBER</p>
      </footer>
    </div>
  );
}

export default Calculator;
```
CSS FILE
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

.container {
  min-height: 100vh;
  background: #f4f4f4;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.calculator {
  background: white;
  padding: 20px;
  border-radius: 10px;
  width: 320px;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
}

.calculator h2 {
  text-align: center;
  margin-bottom: 15px;
}

.display {
  width: 100%;
  padding: 10px;
  font-size: 20px;
  margin-bottom: 15px;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.buttons button {
  padding: 15px;
  font-size: 18px;
  border: none;
  background: #007bff;
  color: white;
  border-radius: 5px;
  cursor: pointer;
}

.buttons button:hover {
  background: #0056b3;
}

footer {
  margin-top: 20px;
  text-align: center;
}
```
APP.JSX
```
import Calculator from "./Calculator";

function App() {
  return <Calculator />;
}

export default App;
```

## OUTPUT

<img width="676" height="393" alt="image" src="https://github.com/user-attachments/assets/55131006-9ed1-4639-88c3-381c3700222c" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
