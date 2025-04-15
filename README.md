<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Fancy Input Without Border</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      background: #121212;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: sans-serif;
      margin: 0;
    }

    .input-wrapper {
      position: relative;
      width: 300px;
      padding-top: 10px;
    }

    .input-container {
      position: relative;
      z-index: 2;
    }

    input {
      width: 100%;
      padding: 18px 12px 10px 12px;
      font-size: 16px;
      border-radius: 12px;
      background-color: #1e1e1e; /* Dark background for input */
      color: white;
      outline: none;
      position: relative;
      z-index: 2;
    }

    label {
      position: absolute;
      top: 18px;
      left: 16px;
      color: #aaa;
      font-size: 16px;
      background-color: #1e1e1e; /* Same as input to create the floating effect */
      padding: 0 4px;
      transition: all 0.3s ease;
      pointer-events: none;
      z-index: 2;
    }

    
    .input-wrapper:focus-within label {
      top: 4px;
      left: 12px;
      font-size: 12px;
      color: #00aaff; /* Change label color on focus */
    }




    /* Animate the top border when input is focused */
    .input-wrapper:focus-within .top-border::before {
      width: 100%;
    }
  </style>
</head>
<body>

  <div class="input-wrapper">
    <div class="input-container">
      <input type="text" id="customInput" placeholder=" " />
      <label for="customInput">Your Name</label>
    </div>
    <div class="top-border"></div>
  </div>

</body>
</html>
