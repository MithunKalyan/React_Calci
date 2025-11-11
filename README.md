# Ex04 Simple Calculator - React Project
## Name: Pagadala Mithun Kalyan
## Reg No: 212223040142
## Date: 17-09-2025

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
## App.js
```
import React, { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      setInput(eval(input).toString()); // Simple eval for demo (avoid in production)
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <h1>React Calculator</h1>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        <div>
          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("/")}>÷</button>
        </div>
        <div>
          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={() => handleClick("*")}>×</button>
        </div>
        <div>
          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("-")}>−</button>
        </div>
        <div>
          <button onClick={() => handleClick("0")}>0</button>
          <button onClick={handleClear}>C</button>
          <button onClick={handleCalculate}>=</button>
          <button onClick={() => handleClick("+")}>+</button>
        </div>
      </div>
    </div>
  );
}

export default App;
```

## App.css
```
body {
  font-family: Arial, sans-serif;
  background-color: #f3f4f6;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator {
  background: white;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  text-align: center;
  width: 260px;
}

input {
  width: 100%;
  height: 40px;
  font-size: 1.2rem;
  text-align: right;
  margin-bottom: 15px;
  padding: 5px;
  border: 1px solid #ddd;
  border-radius: 6px;
}

button {
  width: 50px;
  height: 50px;
  margin: 5px;
  font-size: 1.2rem;
  border: none;
  background: #2563eb;
  color: white;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.2s;
}

button:hover {
  background: #1d4ed8;
}

h1 {
  color: #2563eb;
  margin-bottom: 15px;
}
```

## OUTPUT
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/6f6093cf-33ca-4244-8d39-9fdcd6dc264d" />
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/7a2a787c-eedc-4645-a701-d7b725aa538c" />
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/c3b15580-1e7c-4d2a-a0aa-6a5d5acf8750" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
