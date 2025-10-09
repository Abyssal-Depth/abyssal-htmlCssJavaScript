# Lesson 06 Tasks: Conditionals and Decision Making

---

## Task 1: GUIDED EXAMPLE - Grade Calculator

**Follow these steps to create a grade calculator using conditionals.**

### Step 1: Create the HTML File
Create a file called `grade-calculator.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Grade Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        input {
            width: 100%;
            padding: 12px;
            font-size: 16px;
            margin-bottom: 15px;
            border: 2px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 12px;
            font-size: 18px;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #result {
            margin-top: 20px;
            padding: 20px;
            border-radius: 5px;
            text-align: center;
            font-size: 24px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Grade Calculator</h1>
        <p>Enter your score (0-100):</p>
        <input type="number" id="scoreInput" placeholder="Enter score">
        <button id="calculateBtn">Calculate Grade</button>
        <div id="result"></div>
    </div>
    
    <script>
        let input = document.getElementById('scoreInput');
        let button = document.getElementById('calculateBtn');
        let result = document.getElementById('result');
        
        button.addEventListener('click', function() {
            // Convert input to a number
            let score = Number(input.value);
            
            // Validate input - check if score is in valid range
            if (score < 0 || score > 100) {
                result.textContent = 'Please enter a score between 0 and 100!';
                result.style.backgroundColor = '#ffcdd2';
                result.style.color = '#c62828';
            }
            // Check grade ranges - ORDER MATTERS! Start with highest
            else if (score >= 90) {
                result.textContent = 'Grade: A - Excellent! 🌟';
                result.style.backgroundColor = '#c8e6c9';
                result.style.color = '#2e7d32';
            }
            else if (score >= 80) {
                result.textContent = 'Grade: B - Good Job! 👍';
                result.style.backgroundColor = '#b3e5fc';
                result.style.color = '#01579b';
            }
            else if (score >= 70) {
                result.textContent = 'Grade: C - Not Bad! 📚';
                result.style.backgroundColor = '#fff9c4';
                result.style.color = '#f57f17';
            }
            else if (score >= 60) {
                result.textContent = 'Grade: D - Needs Improvement 📖';
                result.style.backgroundColor = '#ffe0b2';
                result.style.color = '#e65100';
            }
            else {
                result.textContent = 'Grade: F - Keep Trying! 💪';
                result.style.backgroundColor = '#ffcdd2';
                result.style.color = '#c62828';
            }
        });
    </script>
</body>
</html>
```

### Step 2: Test It
1. Open the file in your browser
2. Try different scores (95, 85, 75, 65, 55)
3. Try invalid scores (150, -10)
4. Verify the correct grade and color appear

**✅ Checkpoint:** Each score range should display the correct grade and color.

**Key Concepts in This Example:**
- **Validation first** - Always check for invalid input before processing
- **Order matters** - Start with highest value (90) and work down
- **else if chains** - Only one condition will run
- **=== operator** - Use for comparisons

---

## Task 2: Simple Number Checker

**Goal:** Practice basic if-else statements.

### Instructions:
1. Create a file called `number-checker.html`
2. Check if a number is positive, negative, or zero
3. Display the result with different colors

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Number Checker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f0f0f0;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        input {
            width: 100%;
            padding: 12px;
            font-size: 16px;
            margin-bottom: 15px;
            border: 2px solid #2196f3;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 12px;
            background-color: #2196f3;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
        }
        #result {
            margin-top: 20px;
            padding: 20px;
            border-radius: 5px;
            text-align: center;
            font-size: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Number Checker</h1>
        <p>Enter a number:</p>
        <input type="number" id="numberInput" placeholder="Enter any number">
        <button id="checkBtn">Check Number</button>
        <div id="result"></div>
    </div>
    
    <script>
        let input = document.getElementById('numberInput');
        let button = document.getElementById('checkBtn');
        let result = document.getElementById('result');
        
        button.addEventListener('click', function() {
            // Get and convert input to number
            let number = Number(input.value);
            
            // Check if number is positive
            if (number > 0) {
                result.textContent = 'The number is positive';
                result.style.backgroundColor = '#c8e6c9';
                result.style.color = '#2e7d32';
            }
            // Check if number is negative
            else if (number < 0) {
                // Add your code here for negative numbers
                // Use a red/pink background color
            }
            // If not positive or negative, must be zero
            else {
                // Add your code here for zero
                // Use a blue/gray background color
            }
        });
    </script>
</body>
</html>
```

### Expected Output:
- Input: 5 → "The number is positive" (green background)
- Input: -3 → "The number is negative" (red background)
- Input: 0 → "The number is zero" (blue/gray background)

**💡 Hint:** Follow the pattern from the positive check for the other two conditions!

---

## Task 3: Even or Odd

**Goal:** Use the modulo operator (%) with conditionals.

### Instructions:
1. Create a file called `even-odd.html`
2. Check if a number is even or odd using the modulo operator
3. Display the result with different styling

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Even or Odd</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            text-align: center;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        input {
            width: 80%;
            padding: 12px;
            font-size: 18px;
            margin: 15px 0;
            border: 2px solid #9c27b0;
            border-radius: 5px;
        }
        button {
            padding: 12px 30px;
            background-color: #9c27b0;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
        }
        #result {
            margin-top: 20px;
            padding: 20px;
            border-radius: 10px;
            font-size: 24px;
            font-weight: bold;
        }
        .even {
            background-color: #e1bee7;
            color: #4a148c;
        }
        .odd {
            background-color: #fff9c4;
            color: #f57f17;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Even or Odd Checker</h1>
        <p>Enter a number to check if it's even or odd:</p>
        <input type="number" id="numberInput" placeholder="Enter a number">
        <br>
        <button id="checkBtn">Check</button>
        <div id="result"></div>
    </div>
    
    <script>
        let input = document.getElementById('numberInput');
        let button = document.getElementById('checkBtn');
        let result = document.getElementById('result');
        
        button.addEventListener('click', function() {
            let number = Number(input.value);
            
            // Check if input is empty or not a valid number
            if (input.value === '' || isNaN(number)) {
                result.textContent = 'Please enter a valid number!';
                result.style.backgroundColor = '#ffcdd2';
                result.style.color = '#c62828';
                return; // Stop here if invalid
            }
            
            // Use modulo (%) to check if even or odd
            // If number % 2 equals 0, it's even
            if (number % 2 === 0) {
                result.textContent = `${number} is EVEN`;
                result.className = 'even';
            }
            else {
                // Add your code here for odd numbers
                // Display: "${number} is ODD"
                // Use className = 'odd'
            }
        });
    </script>
</body>
</html>
```

### How Modulo Works:
```javascript
// Modulo (%) gives the remainder when dividing
10 % 2 = 0  // Even (no remainder)
11 % 2 = 1  // Odd (remainder of 1)
8 % 2 = 0   // Even
7 % 2 = 1   // Odd
```

**💡 Key Concept:** Any number divisible by 2 with no remainder is even!

---

## Task 4: Voting Eligibility

**Goal:** Practice comparison operators and calculations.

### Instructions:
1. Create a file called `voting-check.html`
2. Check if someone can vote based on age
3. Calculate years remaining if too young

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Voting Eligibility</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        .container {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        input {
            width: 100%;
            padding: 15px;
            font-size: 18px;
            margin: 15px 0;
            border: 2px solid #667eea;
            border-radius: 8px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 15px;
            background-color: #667eea;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        button:hover {
            background-color: #5568d3;
        }
        #result {
            margin-top: 25px;
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            font-size: 20px;
            font-weight: bold;
        }
        .eligible {
            background-color: #c8e6c9;
            color: #2e7d32;
        }
        .not-eligible {
            background-color: #ffecb3;
            color: #e65100;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🗳️ Voting Eligibility Checker</h1>
        <p>Enter your age to check if you can vote:</p>
        <input type="number" id="ageInput" placeholder="Enter your age">
        <button id="checkBtn">Check Eligibility</button>
        <div id="result"></div>
    </div>
    
    <script>
        let input = document.getElementById('ageInput');
        let button = document.getElementById('checkBtn');
        let result = document.getElementById('result');
        
        button.addEventListener('click', function() {
            let age = Number(input.value);
            
            // Check if age is 18 or older
            if (age >= 18) {
                result.textContent = 'You can vote! 🗳️';
                result.className = 'eligible';
            }
            // If younger than 18
            else if (age > 0 && age < 18) {
                // Calculate years to wait
                let yearsToWait = 18 - age;
                result.textContent = `You cannot vote yet. Wait ${yearsToWait} more year(s).`;
                result.className = 'not-eligible';
            }
            // Handle invalid ages
            else {
                result.textContent = 'Please enter a valid age!';
                result.style.backgroundColor = '#ffcdd2';
                result.style.color = '#c62828';
            }
        });
    </script>
</body>
</html>
```

### Expected Output:
- Age 20 → "You can vote! 🗳️"
- Age 15 → "You cannot vote yet. Wait 3 more year(s)."
- Age -5 → "Please enter a valid age!"

**💡 Bonus:** Handle the singular vs plural ("1 year" vs "2 years") using another conditional!

---

## Task 5: Password Strength Checker

**Goal:** Practice multiple conditions with logical operators.

### Instructions:
1. Create a file called `password-checker.html`
2. Check password strength based on multiple criteria
3. Display strength rating with colors

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Password Strength Checker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        input {
            width: 100%;
            padding: 12px;
            font-size: 16px;
            margin: 15px 0;
            border: 2px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 12px;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
        }
        #result {
            margin-top: 20px;
            padding: 20px;
            border-radius: 5px;
            text-align: center;
            font-size: 20px;
            font-weight: bold;
        }
        .weak {
            background-color: #ffcdd2;
            color: #c62828;
        }
        .medium {
            background-color: #ffe0b2;
            color: #e65100;
        }
        .strong {
            background-color: #c8e6c9;
            color: #2e7d32;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🔒 Password Strength Checker</h1>
        <p>Enter a password to check its strength:</p>
        <input type="password" id="passwordInput" placeholder="Enter password">
        <button id="checkBtn">Check Strength</button>
        <div id="result"></div>
    </div>
    
    <script>
        let input = document.getElementById('passwordInput');
        let button = document.getElementById('checkBtn');
        let result = document.getElementById('result');
        
        button.addEventListener('click', function() {
            let password = input.value;
            let length = password.length;
            
            // Check password length and assign strength
            if (length < 6) {
                result.textContent = '❌ Weak - Password too short!';
                result.className = 'weak';
            }
            else if (length >= 6 && length <= 10) {
                result.textContent = '⚠️ Medium - Could be stronger';
                result.className = 'medium';
            }
            else {
                // Password is longer than 10 characters
                // Add your code here for strong passwords
                // Use textContent and className
            }
            
            console.log('Password length:', length);
        });
    </script>
</body>
</html>
```

### Bonus Challenge - Check for Numbers:
```javascript
// Check if password contains at least one number
let hasNumber = /\d/.test(password);

if (hasNumber) {
    // Password has numbers - better!
}
```

**💡 Hint:** Complete the strong password condition following the pattern!

---

## Task 6: Temperature Advisory

**Goal:** Use if-else if chains with multiple ranges.

### Instructions:
1. Create a file called `temp-advisory.html`
2. Give weather advice based on temperature
3. Change styling based on temperature

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Temperature Advisory</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            text-align: center;
            transition: background-color 0.5s;
        }
        .container {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        input {
            width: 200px;
            padding: 15px;
            font-size: 24px;
            text-align: center;
            border: 3px solid #2196f3;
            border-radius: 10px;
            margin: 20px 0;
        }
        button {
            padding: 15px 40px;
            background-color: #2196f3;
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        #advisory {
            margin-top: 30px;
            padding: 30px;
            border-radius: 15px;
            font-size: 22px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🌡️ Temperature Advisory</h1>
        <p>Enter temperature in Fahrenheit:</p>
        <input type="number" id="tempInput" placeholder="°F">
        <br>
        <button id="checkBtn">Get Advisory</button>
        <div id="advisory"></div>
    </div>
    
    <script>
        let input = document.getElementById('tempInput');
        let button = document.getElementById('checkBtn');
        let advisory = document.getElementById('advisory');
        
        button.addEventListener('click', function() {
            let temp = Number(input.value);
            
            // Freezing temperatures (below 32)
            if (temp < 32) {
                advisory.textContent = '❄️ Freezing! Stay inside!';
                advisory.style.backgroundColor = '#b3e5fc';
                advisory.style.color = '#01579b';
                document.body.style.backgroundColor = '#e1f5fe';
            }
            // Cold (32-50)
            else if (temp >= 32 && temp <= 50) {
                advisory.textContent = '🧥 Cold! Wear a jacket!';
                advisory.style.backgroundColor = '#c5cae9';
                advisory.style.color = '#283593';
                document.body.style.backgroundColor = '#e8eaf6';
            }
            // Nice weather (51-70)
            else if (temp >= 51 && temp <= 70) {
                // Add your code here for nice weather
                // Text: '🌤️ Nice weather!'
                // Use light green colors
            }
            // Warm (71-85)
            // Add your code here
            
            // Hot (above 85)
            // Add your code here
            // Text: '🔥 Hot! Stay hydrated!'
            // Use orange/red colors
        });
    </script>
</body>
</html>
```

### Temperature Ranges:
- Below 32°: Freezing ❄️ (blue)
- 32° - 50°: Cold 🧥 (light blue)
- 51° - 70°: Nice 🌤️ (green)
- 71° - 85°: Warm 🌞 (yellow)
- Above 85°: Hot 🔥 (red/orange)

**💡 Hint:** Follow the pattern for the first two ranges to complete the others!

---

## Task 7: Login Form

**Goal:** Practice combining conditions with AND operator.

### Instructions:
1. Create a file called `simple-login.html`
2. Check username AND password together
3. Give specific error messages

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        .login-box {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            width: 350px;
        }
        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
        }
        input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 12px;
            margin-top: 20px;
            background-color: #667eea;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        button:hover {
            background-color: #5568d3;
        }
        #message {
            margin-top: 20px;
            padding: 15px;
            border-radius: 5px;
            text-align: center;
            font-weight: bold;
            display: none;
        }
        .success {
            background-color: #c8e6c9;
            color: #2e7d32;
        }
        .error {
            background-color: #ffcdd2;
            color: #c62828;
        }
    </style>
</head>
<body>
    <div class="login-box">
        <h1>🔐 Login</h1>
        <input type="text" id="usernameInput" placeholder="Username">
        <input type="password" id="passwordInput" placeholder="Password">
        <button id="loginBtn">Login</button>
        <div id="message"></div>
    </div>
    
    <script>
        // Hardcoded correct credentials
        const CORRECT_USERNAME = 'student';
        const CORRECT_PASSWORD = 'learn123';
        
        let usernameInput = document.getElementById('usernameInput');
        let passwordInput = document.getElementById('passwordInput');
        let loginBtn = document.getElementById('loginBtn');
        let message = document.getElementById('message');
        
        loginBtn.addEventListener('click', function() {
            // Get input values
            let username = usernameInput.value;
            let password = passwordInput.value;
            
            // Show the message div
            message.style.display = 'block';
            
            // Check if both fields are empty
            if (username === '' && password === '') {
                message.textContent = 'Please fill in all fields';
                message.className = 'error';
            }
            // Check if username is empty
            else if (username === '') {
                message.textContent = 'Please enter a username';
                message.className = 'error';
            }
            // Check if password is empty
            else if (password === '') {
                message.textContent = 'Please enter a password';
                message.className = 'error';
            }
            // Check if BOTH username AND password are correct
            else if (username === CORRECT_USERNAME && password === CORRECT_PASSWORD) {
                message.textContent = '✅ Login successful!';
                message.className = 'success';
            }
            // If fields filled but credentials wrong
            else {
                // Add your code here for invalid credentials
                // Show error message
            }
            
            console.log('Username:', username);
            console.log('Password:', password);
        });
    </script>
</body>
</html>
```

### Correct Credentials:
- Username: `student`
- Password: `learn123`

### Expected Behavior:
- Empty fields → "Please fill in all fields"
- Correct credentials → "✅ Login successful!"
- Wrong credentials → "❌ Invalid credentials"

**💡 Key Concept:** The AND operator (`&&`) requires BOTH conditions to be true!

---

## Task 8: Discount Calculator

**Goal:** Practice nested conditionals and calculations.

### Instructions:
1. Create a file called `discount-calc.html`
2. Apply different discounts based on age and price
3. Calculate and display savings

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Discount Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .calculator {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 2px solid #4caf50;
            border-radius: 5px;
            font-size: 16px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 15px;
            margin-top: 15px;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        #results {
            margin-top: 30px;
            padding: 25px;
            background-color: #e8f5e9;
            border-radius: 8px;
            border-left: 5px solid #4caf50;
        }
        .result-line {
            margin: 10px 0;
            font-size: 18px;
        }
        .highlight {
            font-size: 24px;
            font-weight: bold;
            color: #2e7d32;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>💰 Discount Calculator</h1>
        <p>Enter product price and your age:</p>
        
        <input type="number" id="priceInput" placeholder="Product price ($)">
        <input type="number" id="ageInput" placeholder="Your age">
        
        <button id="calculateBtn">Calculate Final Price</button>
        
        <div id="results" style="display: none;"></div>
    </div>
    
    <script>
        let priceInput = document.getElementById('priceInput');
        let ageInput = document.getElementById('ageInput');
        let calculateBtn = document.getElementById('calculateBtn');
        let results = document.getElementById('results');
        
        calculateBtn.addEventListener('click', function() {
            let price = Number(priceInput.value);
            let age = Number(ageInput.value);
            
            let discountPercent = 0;
            let discountReason = '';
            
            // Check age for discounts
            if (age < 12) {
                discountPercent = 20;
                discountReason = 'Kids discount (20%)';
            }
            else if (age >= 65) {
                discountPercent = 15;
                discountReason = 'Senior discount (15%)';
            }
            
            // Additional discount for orders over $100
            if (price > 100) {
                discountPercent += 10;
                discountReason += ' + Large order (10%)';
            }
            
            // Calculate discount amount and final price
            let discountAmount = price * (discountPercent / 100);
            let finalPrice = price - discountAmount;
            
            // Display results
            results.style.display = 'block';
            results.innerHTML = `
                <div class="result-line">Original Price: $${price.toFixed(2)}</div>
                <div class="result-line">Discount: ${discountPercent}% ${discountReason}</div>
                <div class="result-line">You Save: $${discountAmount.toFixed(2)}</div>
                <div class="highlight">Final Price: $${finalPrice.toFixed(2)}</div>
            `;
            
            console.log(`Price: $${price}, Age: ${age}, Discount: ${discountPercent}%`);
        });
    </script>
</body>
</html>
```

### Discount Rules:
- Kids under 12: **20% off**
- Seniors 65+: **15% off**
- Everyone else: **No discount**
- Orders over $100: **Additional 10% off**

### Example:
- Price: $120, Age: 70
- Discount: 25% (Senior 15% + Large order 10%)
- Final: $90.00

**💡 Key Concept:** Discounts can stack! The code adds the extra 10% on top of age discounts.

---

## Task 9: Traffic Light Simulator

**Goal:** Practice multiple conditions and styling.

### Instructions:
1. Create a file called `traffic-light.html`
2. Create three colored circles (lights)
3. Turn lights on/off based on button clicks

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Traffic Light Simulator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #263238;
        }
        .traffic-light-box {
            background-color: #37474f;
            width: 200px;
            padding: 30px;
            margin: 0 auto;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }
        .light {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin: 20px auto;
            border: 5px solid #1c1c1c;
            transition: all 0.3s;
        }
        .red-light {
            background-color: #555;
        }
        .red-on {
            background-color: #f44336;
            box-shadow: 0 0 40px #f44336;
        }
        .yellow-light {
            background-color: #555;
        }
        .yellow-on {
            background-color: #ffeb3b;
            box-shadow: 0 0 40px #ffeb3b;
        }
        .green-light {
            background-color: #555;
        }
        .green-on {
            background-color: #4caf50;
            box-shadow: 0 0 40px #4caf50;
        }
        .controls {
            margin-top: 40px;
        }
        button {
            padding: 15px 30px;
            margin: 10px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            color: white;
        }
        #redBtn {
            background-color: #f44336;
        }
        #yellowBtn {
            background-color: #ffeb3b;
            color: #333;
        }
        #greenBtn {
            background-color: #4caf50;
        }
        #message {
            margin-top: 30px;
            font-size: 32px;
            font-weight: bold;
            color: white;
            min-height: 50px;
        }
    </style>
</head>
<body>
    <h1 style="color: white;">🚦 Traffic Light Simulator</h1>
    
    <div class="traffic-light-box">
        <div id="redLight" class="light red-light"></div>
        <div id="yellowLight" class="light yellow-light"></div>
        <div id="greenLight" class="light green-light"></div>
    </div>
    
    <div class="controls">
        <button id="redBtn">Red Light</button>
        <button id="yellowBtn">Yellow Light</button>
        <button id="greenBtn">Green Light</button>
    </div>
    
    <div id="message"></div>
    
    <script>
        // Select all light elements
        let redLight = document.getElementById('redLight');
        let yellowLight = document.getElementById('yellowLight');
        let greenLight = document.getElementById('greenLight');
        
        // Select all buttons
        let redBtn = document.getElementById('redBtn');
        let yellowBtn = document.getElementById('yellowBtn');
        let greenBtn = document.getElementById('greenBtn');
        
        // Select message display
        let message = document.getElementById('message');
        
        // Red button click
        redBtn.addEventListener('click', function() {
            // Turn on red light
            redLight.className = 'light red-light red-on';
            
            // Turn off other lights
            yellowLight.className = 'light yellow-light';
            greenLight.className = 'light green-light';
            
            // Display message
            message.textContent = '🛑 STOP';
            message.style.color = '#f44336';
        });
        
        // Yellow button click
        yellowBtn.addEventListener('click', function() {
            // Turn on yellow light
            // Turn off other lights
            // Display "⚠️ CAUTION"
            // Add your code here...
        });
        
        // Green button click
        // Add your event listener here...
        // Turn on green light
        // Turn off other lights
        // Display "✅ GO"
    </script>
</body>
</html>
```

### Expected Behavior:
- Click "Red Light" → Red glows, message shows "STOP"
- Click "Yellow Light" → Yellow glows, message shows "CAUTION"
- Click "Green Light" → Green glows, message shows "GO"
- Only one light on at a time

**💡 Hint:** Follow the pattern from the red button for the other two!

---

## Task 10: BMI Calculator

**Goal:** Practice calculations with multiple conditional ranges.

### Instructions:
1. Create a file called `bmi-calculator.html`
2. Calculate BMI from weight and height
3. Categorize BMI into health ranges

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>BMI Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        .calculator {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        label {
            display: block;
            margin-top: 15px;
            font-weight: bold;
            color: #555;
        }
        input {
            width: 100%;
            padding: 12px;
            margin-top: 5px;
            border: 2px solid #667eea;
            border-radius: 5px;
            font-size: 16px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 15px;
            margin-top: 25px;
            background-color: #667eea;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        #result {
            margin-top: 25px;
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            display: none;
        }
        .bmi-number {
            font-size: 48px;
            font-weight: bold;
            margin: 10px 0;
        }
        .bmi-category {
            font-size: 24px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>📊 BMI Calculator</h1>
        
        <label for="weightInput">Weight (pounds):</label>
        <input type="number" id="weightInput" placeholder="Enter weight">
        
        <label for="heightInput">Height (inches):</label>
        <input type="number" id="heightInput" placeholder="Enter height">
        
        <button id="calculateBtn">Calculate BMI</button>
        
        <div id="result"></div>
    </div>
    
    <script>
        let weightInput = document.getElementById('weightInput');
        let heightInput = document.getElementById('heightInput');
        let calculateBtn = document.getElementById('calculateBtn');
        let result = document.getElementById('result');
        
        calculateBtn.addEventListener('click', function() {
            let weight = Number(weightInput.value);
            let height = Number(heightInput.value);
            
            // Calculate BMI: (weight / (height * height)) * 703
            let bmi = (weight / (height * height)) * 703;
            
            // Round to 1 decimal place
            bmi = bmi.toFixed(1);
            
            let category = '';
            let color = '';
            
            // Determine BMI category
            if (bmi < 18.5) {
                category = 'Underweight';
                color = '#64b5f6';
            }
            else if (bmi >= 18.5 && bmi < 25) {
                category = 'Normal weight';
                color = '#81c784';
            }
            else if (bmi >= 25 && bmi < 30) {
                // Add category for Overweight
                // Use orange color (#ffb74d)
            }
            else {
                // Add category for Obese
                // Use red color (#e57373)
            }
            
            // Display result
            result.style.display = 'block';
            result.style.backgroundColor = color;
            result.innerHTML = `
                <div class="bmi-number">${bmi}</div>
                <div class="bmi-category">${category}</div>
            `;
            
            console.log(`BMI: ${bmi}, Category: ${category}`);
        });
    </script>
</body>
</html>
```

### BMI Categories:
- Below 18.5: **Underweight** (blue)
- 18.5 - 24.9: **Normal weight** (green)
- 25.0 - 29.9: **Overweight** (orange)
- 30.0 and above: **Obese** (red)

### Formula:
```
BMI = (weight ÷ height²) × 703
```

**💡 Hint:** Complete the two missing categories following the pattern!

---

## Challenge Task: Quiz Game

**Goal:** Create a multi-question quiz with scoring.

### Instructions:
1. Create a file called `quiz-game.html`
2. Track score across multiple questions
3. Show final results with conditional messages

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Quiz Game</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 700px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f0f4f8;
        }
        .quiz-container {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #2c3e50;
        }
        .question {
            background-color: #ecf0f1;
            padding: 20px;
            margin: 20px 0;
            border-radius: 10px;
            border-left: 5px solid #3498db;
        }
        .question h3 {
            margin-top: 0;
            color: #2c3e50;
        }
        .answer-btn {
            display: block;
            width: 100%;
            padding: 15px;
            margin: 10px 0;
            background-color: #ecf0f1;
            border: 2px solid #bdc3c7;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            text-align: left;
            transition: all 0.3s;
        }
        .answer-btn:hover {
            background-color: #d5dbdb;
            transform: translateX(5px);
        }
        .correct {
            background-color: #d4edda !important;
            border-color: #c3e6cb !important;
        }
        .incorrect {
            background-color: #f8d7da !important;
            border-color: #f5c6cb !important;
        }
        #scoreDisplay {
            text-align: center;
            font-size: 24px;
            font-weight: bold;
            margin: 30px 0;
            color: #2c3e50;
        }
        #submitBtn {
            display: block;
            width: 100%;
            padding: 15px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        #finalResults {
            margin-top: 30px;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            font-size: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <h1>🎯 JavaScript Quiz</h1>
        
        <!-- Question 1 -->
        <div class="question">
            <h3>Question 1: What is 5 + 3?</h3>
            <button class="answer-btn" data-question="1" data-correct="false">7</button>
            <button class="answer-btn" data-question="1" data-correct="true">8</button>
            <button class="answer-btn" data-question="1" data-correct="false">9</button>
        </div>
        
        <!-- Question 2 -->
        <div class="question">
            <h3>Question 2: What does CSS stand for?</h3>
            <button class="answer-btn" data-question="2" data-correct="true">Cascading Style Sheets</button>
            <button class="answer-btn" data-question="2" data-correct="false">Computer Style System</button>
            <button class="answer-btn" data-question="2" data-correct="false">Creative Style Sheets</button>
        </div>
        
        <!-- Question 3 -->
        <div class="question">
            <h3>Question 3: Which is a JavaScript data type?</h3>
            <button class="answer-btn" data-question="3" data-correct="false">text</button>
            <button class="answer-btn" data-question="3" data-correct="true">boolean</button>
            <button class="answer-btn" data-question="3" data-correct="false">decimal</button>
        </div>
        
        <div id="scoreDisplay">Score: 0 / 3</div>
        
        <button id="submitBtn">Show Final Results</button>
        
        <div id="finalResults"></div>
    </div>
    
    <script>
        let score = 0;
        let totalQuestions = 3;
        let answeredQuestions = [];
        
        let scoreDisplay = document.getElementById('scoreDisplay');
        let submitBtn = document.getElementById('submitBtn');
        let finalResults = document.getElementById('finalResults');
        
        // Get all answer buttons
        let answerButtons = document.querySelectorAll('.answer-btn');
        
        // Add click event to each answer button
        answerButtons.forEach(function(button) {
            button.addEventListener('click', function() {
                let questionNum = button.getAttribute('data-question');
                let isCorrect = button.getAttribute('data-correct') === 'true';
                
                // Check if this question was already answered
                if (answeredQuestions.includes(questionNum)) {
                    return; // Don't allow answering twice
                }
                
                // Mark question as answered
                answeredQuestions.push(questionNum);
                
                // Check if answer is correct
                if (isCorrect) {
                    score++;
                    button.classList.add('correct');
                } else {
                    button.classList.add('incorrect');
                    // Find and highlight the correct answer
                    answerButtons.forEach(function(btn) {
                        if (btn.getAttribute('data-question') === questionNum && 
                            btn.getAttribute('data-correct') === 'true') {
                            btn.classList.add('correct');
                        }
                    });
                }
                
                // Update score display
                scoreDisplay.textContent = `Score: ${score} / ${totalQuestions}`;
                
                // Disable all buttons for this question
                answerButtons.forEach(function(btn) {
                    if (btn.getAttribute('data-question') === questionNum) {
                        btn.style.cursor = 'not-allowed';
                        btn.style.opacity = '0.7';
                    }
                });
            });
        });
        
        // Show final results
        submitBtn.addEventListener('click', function() {
            let percentage = (score / totalQuestions) * 100;
            let message = '';
            let bgColor = '';
            
            if (percentage === 100) {
                message = '🏆 Perfect! You got all questions right!';
                bgColor = '#d4edda';
            }
            else if (percentage >= 70) {
                message = '🌟 Great job! You did well!';
                bgColor = '#d1ecf1';
            }
            else if (percentage >= 50) {
                message = '👍 Good try! Keep practicing!';
                bgColor = '#fff3cd';
            }
            else {
                message = '📚 Keep studying! You\'ll do better next time!';
                bgColor = '#f8d7da';
            }
            
            finalResults.style.display = 'block';
            finalResults.style.backgroundColor = bgColor;
            finalResults.innerHTML = `
                <h2>Final Results</h2>
                <p>You got ${score} out of ${totalQuestions} correct</p>
                <p>Percentage: ${percentage.toFixed(0)}%</p>
                <p>${message}</p>
            `;
        });
    </script>
</body>
</html>
```

### Features Included:
- Three questions with multiple choice
- Tracks score automatically
- Shows correct/incorrect answers
- Prevents answering same question twice
- Final results with conditional messages

### Bonus Ideas:
- Add more questions
- Add a timer
- Create a "Next Question" flow
- Store high score in browser

**💡 Try changing the questions and answers to create your own quiz!**

---

## Challenge Task 2: Shipping Calculator

**Goal:** Complex conditionals with multiple factors.

### Instructions:
1. Create a file called `shipping-calc.html`
2. Calculate shipping based on destination and speed
3. Apply free shipping thresholds

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Shipping Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .calculator {
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        label {
            display: block;
            margin-top: 15px;
            font-weight: bold;
            color: #333;
        }
        input, select {
            width: 100%;
            padding: 12px;
            margin-top: 5px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 15px;
            margin-top: 25px;
            background-color: #ff9800;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            cursor: pointer;
            font-weight: bold;
        }
        #results {
            margin-top: 30px;
            padding: 25px;
            background-color: #fff3e0;
            border-radius: 8px;
            border-left: 5px solid #ff9800;
            display: none;
        }
        .result-line {
            display: flex;
            justify-content: space-between;
            margin: 10px 0;
            font-size: 18px;
        }
        .total {
            font-size: 24px;
            font-weight: bold;
            color: #e65100;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 2px solid #ff9800;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>📦 Shipping Calculator</h1>
        
        <label for="orderTotal">Order Total ($):</label>
        <input type="number" id="orderTotal" placeholder="Enter order amount">
        
        <label for="destination">Shipping Destination:</label>
        <select id="destination">
            <option value="">Select destination</option>
            <option value="domestic">Domestic</option>
            <option value="international">International</option>
        </select>
        
        <label for="speed">Shipping Speed:</label>
        <select id="speed">
            <option value="">Select speed</option>
            <option value="standard">Standard</option>
            <option value="express">Express</option>
        </select>
        
        <button id="calculateBtn">Calculate Shipping</button>
        
        <div id="results"></div>
    </div>
    
    <script>
        let orderTotalInput = document.getElementById('orderTotal');
        let destinationSelect = document.getElementById('destination');
        let speedSelect = document.getElementById('speed');
        let calculateBtn = document.getElementById('calculateBtn');
        let results = document.getElementById('results');
        
        calculateBtn.addEventListener('click', function() {
            let orderTotal = Number(orderTotalInput.value);
            let destination = destinationSelect.value;
            let speed = speedSelect.value;
            
            let shippingCost = 0;
            let shippingMethod = '';
            
            // Domestic Standard: $5.99 (free if order > $50)
            if (destination === 'domestic' && speed === 'standard') {
                shippingMethod = 'Domestic Standard';
                if (orderTotal > 50) {
                    shippingCost = 0;
                } else {
                    shippingCost = 5.99;
                }
            }
            // Domestic Express: $12.99 (free if order > $100)
            else if (destination === 'domestic' && speed === 'express') {
                shippingMethod = 'Domestic Express';
                if (orderTotal > 100) {
                    shippingCost = 0;
                } else {
                    shippingCost = 12.99;
                }
            }
            // International Standard: $19.99 (free if order > $150)
            else if (destination === 'international' && speed === 'standard') {
                // Add your code here
            }
            // International Express: $39.99 (free if order > $200)
            else if (destination === 'international' && speed === 'express') {
                // Add your code here
            }
            
            // Calculate final total
            let finalTotal = orderTotal + shippingCost;
            
            // Display results
            results.style.display = 'block';
            results.innerHTML = `
                <div class="result-line">
                    <span>Subtotal:</span>
                    <span>$${orderTotal.toFixed(2)}</span>
                </div>
                <div class="result-line">
                    <span>Shipping (${shippingMethod}):</span>
                    <span>${shippingCost === 0 ? 'FREE' : '$' + shippingCost.toFixed(2)}</span>
                </div>
                <div class="result-line total">
                    <span>Total:</span>
                    <span>$${finalTotal.toFixed(2)}</span>
                </div>
            `;
        });
    </script>
</body>
</html>
```

### Shipping Rules:
| Destination | Speed | Cost | Free Threshold |
|------------|-------|------|----------------|
| Domestic | Standard | $5.99 | Over $50 |
| Domestic | Express | $12.99 | Over $100 |
| International | Standard | $19.99 | Over $150 |
| International | Express | $39.99 | Over $200 |

**💡 Hint:** Complete the two international shipping options following the same pattern!

---

## Tips for Success

1. **Test all paths** - Try every possible condition
   ```javascript
   // Test with: age = 10, age = 18, age = 65, age = 100
   ```

2. **Order matters in if-else chains** - Put most specific conditions first
   ```javascript
   // ✅ Correct order
   if (score >= 90) { }
   else if (score >= 80) { }
   else if (score >= 70) { }
   
   // ❌ Wrong order
   if (score >= 70) { }  // This catches 90 too!
   else if (score >= 90) { } // Never runs
   ```

3. **Use === not ==** - Avoid type conversion issues
   ```javascript
   if (age === 18)  // ✅ Correct
   if (age == 18)   // ⚠️ Works but not recommended
   if (age = 18)    // ❌ Wrong! This assigns, doesn't compare
   ```

4. **Always validate input**
   ```javascript
   if (age < 0 || age > 120) {
       alert('Invalid age!');
       return; // Stop execution
   }
   ```

5. **Console.log conditions** - Debug by logging true/false values
   ```javascript
   console.log('Is age 18?', age === 18);
   ```

## Common Mistakes to Avoid

❌ **Using = instead of ===**
```javascript
if (age = 18) // Wrong! This assigns 18 to age
```
✅ **Use === for comparison**
```javascript
if (age === 18) // Correct! This compares
```

❌ **Wrong order in else-if chains**
```javascript
if (score >= 60) { return 'D'; }
else if (score >= 90) { return 'A'; } // Never runs!
```
✅ **Start with highest/most specific**
```javascript
if (score >= 90) { return 'A'; }
else if (score >= 60) { return 'D'; } // Now works!
```

❌ **Forgetting to convert input to number**
```javascript
let age = input.value; // age is a string!
if (age > 18) // "20" > 18 works, but "5" > 18 is true!
```
✅ **Always convert**
```javascript
let age = Number(input.value); // Now it's a number
if (age > 18) // Correct comparison
```

❌ **Not handling edge cases**
```javascript
if (age >= 18) {
    // What about negative ages? Empty input?
}
```
✅ **Validate first**
```javascript
if (age < 0 || age > 120 || isNaN(age)) {
    alert('Invalid age!');
}
else if (age >= 18) {
    // Now it's safe
}
```

---

## Comparison Operators Quick Reference

```javascript
===  // Equal to (strict)
!==  // Not equal to
>    // Greater than
<    // Less than
>=   // Greater than or equal to
<=   // Less than or equal to
```

## Logical Operators

```javascript
&&   // AND - both must be true
||   // OR - at least one must be true
!    // NOT - reverses true/false

// Examples:
if (age >= 18 && hasID) { }  // Both conditions required
if (isWeekend || isHoliday) { }  // Either condition works
if (!isLoggedIn) { }  // If NOT logged in
```

## Conditional Structure Patterns

```javascript
// Simple if-else
if (condition) {
    // do this
} else {
    // do that
}

// Multiple conditions (else-if chain)
if (condition1) {
    // first option
} else if (condition2) {
    // second option
} else if (condition3) {
    // third option
} else {
    // default option
}

// Nested conditionals
if (condition1) {
    if (condition2) {
        // both true
    }
}
```