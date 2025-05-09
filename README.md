# Ex04 Simple Calculator - React Project
## Date:21.04.25

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
index.js
```
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```
app.css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(135deg, #9aa1a6, #232965);
}

.container {
  width: 300px;
}

.calculator {
  background-color: rgb(8, 8, 8);
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(255, 255, 255, 0.2);
}

.display input {
  width: 100%;
  height: 60px;
  font-size: 24px;
  text-align: right;
  margin-bottom: 10px;
  padding: 5px;
  border: none;
  border-radius: 5px;
  background-color: rgb(250, 250, 250);
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 60px;
  font-size: 20px;
  background-color: rgb(9, 66, 99);
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}

button:hover {
  background-color: rgb(255, 255, 255);
}

button:active {
  background-color: rgb(100, 100, 200);
}

button:nth-child(16) {
  background-color: rgb(112, 9, 51); /* Red for 'C' */
}

```
app.js
```

import React, { useState } from 'react';
import './App.css';

function App() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput('');
  };

  const calculateResult = () => {
    try {
      setInput(eval(input));
    } catch {
      setInput('Error');
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <form className="display">
          <input type="text" value={input} readOnly />
        </form>

        <div className="buttons">
          <button onClick={() => handleClick('1')}>1</button>
          <button onClick={() => handleClick('2')}>2</button>
          <button onClick={() => handleClick('3')}>3</button>
          <button onClick={() => handleClick('+')}>+</button>

          <button onClick={() => handleClick('4')}>4</button>
          <button onClick={() => handleClick('5')}>5</button>
          <button onClick={() => handleClick('6')}>6</button>
          <button onClick={() => handleClick('-')}>-</button>

          <button onClick={() => handleClick('7')}>7</button>
          <button onClick={() => handleClick('8')}>8</button>
          <button onClick={() => handleClick('9')}>9</button>
          <button onClick={() => handleClick('')}></button>

          <button onClick={() => handleClick('0')}>0</button>
          <button onClick={clearInput}>C</button>
          <button onClick={calculateResult}>=</button>
          <button onClick={() => handleClick('/')}>/</button>
        </div>
      </div>

      {/* Footer Section */}
      <footer className="footer">
        <p>Reg No: 212223220093 | Name: Sandhiya Sree</p>
      </footer>
    </div>
  );
}

export default App;
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(135deg, #3498db, #8e44ad);
}

.container {
  width: 300px;
}

.calculator {
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.display input {
  width: 100%;
  height: 60px;
  font-size: 24px;
  text-align: right;
  margin-bottom: 10px;
  padding: 5px;
  border: none;
  border-radius: 5px;
  background-color: rgb(240, 240, 240);
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 60px;
  font-size: 20px;
  background-color: rgb(91, 91, 151);
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}

button:hover {
  background-color: rgb(137, 22, 245);
}

button:active {
  background-color: rgb(100, 100, 200);
}

button:nth-child(16) {
  background-color: rgb(220, 53, 69); /* Red for 'C' */
}

.footer {
  margin-top: 20px;
  text-align: center;
  font-size: 14px;
  color: white;
}
```


## OUTPUT
![image](https://github.com/user-attachments/assets/6e989a09-2ed5-47cf-958b-ab0dbec2b407)





## RESULT
The program for developing a simple calculator in React.js is executed successfully.
