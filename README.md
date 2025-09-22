# MWAD-EXP_04-Simple-caluculator
## Date:

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

Calculator.js
```
import React, { useState } from "react";
import "./Calculator.css";

export default function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      setInput(eval(input).toString()); 
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || "0"}</div>
      <div className="buttons">
        {/* Number buttons */}
        {[1, 2, 3, 4, 5, 6, 7, 8, 9, 0].map((num) => (
          <button key={num} onClick={() => handleClick(num.toString())}>
            {num}
          </button>
        ))}
        {/* Operators */}
        {["+", "-", "*", "/"].map((op) => (
          <button key={op} onClick={() => handleClick(op)}>
            {op}
          </button>
        ))}
        {/* Clear and Equal */}
        <button className="clear" onClick={handleClear}>C</button>
        <button className="equal" onClick={handleCalculate}>=</button>
      </div>
    </div>
  );
}


```

Calculator.css

```
.calculator {
  width: 250px;
  margin: 50px auto;
  padding: 10px;
  background: #222;
  border-radius: 10px;
  box-shadow: 0 0 10px #000;
}

.display {
  background: #000;
  color: #0f0;
  font-size: 2rem;
  padding: 10px;
  text-align: right;
  margin-bottom: 10px;
  border-radius: 5px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;
}

button {
  padding: 15px;
  font-size: 1.2rem;
  border: none;
  border-radius: 5px;
  background: #444;
  color: white;
  cursor: pointer;
}

button:hover {
  background: #666;
}

.clear {
  background: red;
}

.equal {
  background: green;
}

```

App.js
```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <div className="App">
      <h1 style={{ textAlign: "center" }}>Simple Calculator</h1>
      <Calculator />
    </div>
  );
}

export default App;

```


## OUTPUT
<img width="1897" height="915" alt="image" src="https://github.com/user-attachments/assets/548297f7-7aa8-4e38-9cdf-542dcfb3b710" />
<img width="1890" height="898" alt="image" src="https://github.com/user-attachments/assets/cf6cce12-7dc8-4191-bf89-ae0f4245f420" />



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
