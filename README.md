# Ex.08 Design of a Standard Calculator
## Date: 16.04.2024

## AIM: 
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

```
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
    #calculator {
      width: 20%;
      margin: 75px auto;
      border: 2px solid #330aa1;
      border-radius: 5px;
      padding: 10px;
      background-color: #0882b6fe;
    }
    #screen {
      height: 50px;
      font-size: 20px;
      text-align: right;
      padding: 5px;
      margin-bottom: 10px;
      background-color: #fff;
      border: 1px solid #ccc;
      border-radius: 3px;
    }
    .btn {
      width: 50px;
      height: 50px;
      margin: 5px;
      background-color: #ff9800;
      color: black;
      font-size: 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .btn:hover {
      background-color: moccasin;
    }
    .btn.operator {
      background-color: #ff9800;
      color: #fff;
    }
    .btn.operator:hover {
      background-color: #f57c00;
    }
    .equals{
        grid-column: span 4;
        width: 80%;
    }
  </style>
</head>
<body>

    <div id="calculator">
        <div style="font-family: arial black;">ESWANTH KUMAR K</div>
        <div style="font-family: arial black;">REGNO.212223040046</div> <br>
        <div id="screen">0</div>
        <button class="btn" onclick="appendToScreen('.')">.</button>
        <button class="btn" onclick="clearScreen()">C</button>
        <button class="btn" onclick="appendToScreen('/')">/</button>
        <button class="btn" onclick="appendToScreen('*')">*</button>
        <button class="btn" onclick="appendToScreen('7')">7</button>
        <button class="btn" onclick="appendToScreen('8')">8</button>
        <button class="btn" onclick="appendToScreen('9')">9</button>
        <button class="btn" onclick="appendToScreen('-')">-</button>
        <button class="btn" onclick="appendToScreen('4')">4</button>
        <button class="btn" onclick="appendToScreen('5')">5</button>
        <button class="btn" onclick="appendToScreen('6')">6</button>
        <button class="btn" onclick="appendToScreen('+')">+</button>
        <button class="btn" onclick="appendToScreen('1')">1</button>
        <button class="btn" onclick="appendToScreen('2')">2</button>
        <button class="btn" onclick="appendToScreen('3')">3</button>
        <button class="btn" onclick="appendToScreen('0')">0</button>
        <button class="btn equals"  onclick="calculate()" >=</button>
    </div>

<script>
  let screen = document.getElementById('screen');
  let currentValue = '';

  function appendToScreen(value) {
    if (value === '.') {
      if (!currentValue.includes('.')) {
        currentValue += value;
      }
    } else {
      currentValue += value;
    }
    screen.textContent = currentValue;
  }

  function clearScreen() {
    currentValue = '';
    screen.textContent = '0';
  }

  function calculate() {
    try {
      currentValue = eval(currentValue).toString();
      screen.textContent = currentValue;
    } catch (error) {
      screen.textContent = 'Error';
    }
  }
</script>

</body>
</html>
```

## OUTPUT:

![alt text](<Screenshot (20).png>)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
