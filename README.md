# Ex04 Simple Calculator - React Project
## Name: Tarun S
## Reg. NO.: 212223040226

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
### app.jsx
```
import { useState } from "react";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const calculate = () => {
    try {
      setInput(String(eval(input)));
    } catch {
      setInput("Error");
    }
  };

  const clearInput = () => setInput("");

  return (
    <div style={styles.container}>
      <div style={styles.display}>{input || "0"}</div>

      <div style={styles.grid}>
        {["7","8","9","/","4","5","6","*","1","2","3","-","0",".","=","+"].map((btn) => (
          <button 
            key={btn} 
            onClick={() => btn === "=" ? calculate() : handleClick(btn)}
            style={styles.button}
          >
            {btn}
          </button>
        ))}

        <button onClick={clearInput} style={styles.clear}>Clear</button>
      </div>
    </div>
  );
}

const styles = {
  container: {
    width: 260,
    margin: "50px auto",
    padding: 20,
    background: "white",
    borderRadius: 10,
    boxShadow: "0 0 10px rgba(0,0,0,0.2)",
  },
  display: {
    height: 50,
    fontSize: 24,
    background: "black",
    textAlign: "right",
    padding: 10,
    marginBottom: 10,
    borderRadius: 6,
  },
  grid: {
    display: "grid",
    gridTemplateColumns: "repeat(4, 1fr)",
    gap: 8,
  },
  button: {
    padding: 15,
    fontSize: 18,
    border: "none",
    borderRadius: 6,
    background: "black",
    cursor: "pointer",
  },
  clear: {
    gridColumn: "span 4",
    padding: 15,
    fontSize: 18,
    background: "red",
    color: "grey",
    borderRadius: 6,
    cursor: "pointer",
  }
};

export default App;

  ```

## OUTPUT
<img width="527" height="687" alt="Screenshot 2025-10-31 162225" src="https://github.com/user-attachments/assets/1fb9116d-91e8-4d0b-8755-ee0b98d5e28e" />



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
