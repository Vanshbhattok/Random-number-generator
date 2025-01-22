# This project is created by members of Team-9 (DevOPS & SCM).
## Looking to enhance the GUI and add functionalities.
## New features would be added like 7-UP,Tambola, etc.
## Follow along for newer updates as our team proceeds.
## ![225813708-98b745f2-7d22-48cf-9150-083f1b00d6c9](https://github.com/user-attachments/assets/d7c6b1de-658d-47d7-bbc9-63fbf4916b11)
<!DOCTYPE html>
<html>
<head>
  <style>
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
      background-color: #f2f2f2;
    }

    .container {
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      padding: 30px;
      text-align: center;
      width: 300px;
    }

    h1 {
      font-size: 24px;
      margin-bottom: 20px;
    }

    .input-section {
      margin-bottom: 20px;
    }

    input[type="number"] {
      padding: 8px;
      margin: 10px 5px;
      width: 80px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      padding: 10px 20px;
      margin-top: 10px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #45a049;
    }

    button:active {
      background-color: #3e8e41;
    }

    #randomNumber {
      font-size: 24px;
      font-weight: bold;
      margin: 20px 0;
      color: #333;
    }

    #reset {
      background-color: #f44336;
      margin-top: 10px;
    }

    #reset:hover {
      background-color: #e53935;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Random Number Generator</h1>
    <div class="input-section">
      <label for="min">Minimum:</label>
      <input type="number" id="min" value="1">
      <label for="max">Maximum:</label>
      <input type="number" id="max" value="100">
    </div>
    <button id="generate">Generate Random Number</button>
    <div class="result">
      <p id="randomNumber">Click the button to generate</p>
    </div>
    <button id="reset">Reset</button>
  </div>

  <script>
    document.getElementById('generate').addEventListener('click', function() {
      const min = parseInt(document.getElementById('min').value);
      const max = parseInt(document.getElementById('max').value);
      const randomNumber = Math.floor(Math.random() * (max - min + 1)) + min;
      document.getElementById('randomNumber').innerText = randomNumber;
    });

    document.getElementById('reset').addEventListener('click', function() {
      document.getElementById('randomNumber').innerText = 'Click the button to generate';
      document.getElementById('min').value = 1;
      document.getElementById('max').value = 100;
    });
  </script>
</body>
</html>
