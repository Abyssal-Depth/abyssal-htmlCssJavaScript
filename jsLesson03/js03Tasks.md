# Lesson 03 Tasks: Math Operations Practice

---

## Task 1: GUIDED EXAMPLE - Grade Calculator

**Follow these steps to create a grade calculator.**

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
        .result {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            margin-top: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        h1 {
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Grade Calculator</h1>
    <div class="result" id="output"></div>
    
    <script>
        // Test scores
        let test1 = 85;
        let test2 = 92;
        let test3 = 78;
        let test4 = 88;
        
        // Calculate total
        let total = test1 + test2 + test3 + test4;
        
        // Calculate average
        let average = total / 4;
        
        // Round to 1 decimal place
        let roundedAverage = average.toFixed(1);
        
        // Display results
        let output = `
            Test 1: ${test1}
            Test 2: ${test2}
            Test 3: ${test3}
            Test 4: ${test4}
            
            Total Points: ${total}
            Average: ${roundedAverage}
        `;
        
        document.getElementById('output').textContent = output;
        
        // Log to console
        console.log('Average grade:', roundedAverage);
    </script>
</body>
</html>
```

### Step 2: Test and Modify
1. Open the file in your browser
2. See the calculated results
3. Change the test scores to different values
4. Refresh and see the new calculation

**✅ Checkpoint:** The average should update correctly when you change the test scores.

---

## Task 2: Basic Calculator

**Goal:** Practice all basic math operations.

### Instructions:
1. Create a file called `calculator.html`
2. Create two variables: `num1` and `num2` (use any numbers)
3. Perform all five operations: `+`, `-`, `*`, `/`, `%`
4. Display each result on the page with a label
5. Also log each result to the console

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Basic Calculator</title>
</head>
<body>
    <h1>Math Operations Practice</h1>
    
    <!-- Create paragraph elements for each operation -->
    <p id="addition"></p>
    <p id="subtraction"></p>
    <p id="multiplication"></p>
    <p id="division"></p>
    <p id="remainder"></p>
    
    <script>
        // Your two numbers
        let num1 = 10;
        let num2 = 5;
        
        // Perform calculations
        let sum = num1 + num2;
        let difference = num1 - num2;
        let product = num1 * num2;
        // Add division here
        // Add remainder here
        
        // Display results using template literals
        document.getElementById('addition').textContent = `Addition: ${num1} + ${num2} = ${sum}`;
        document.getElementById('subtraction').textContent = `Subtraction: ${num1} - ${num2} = ${difference}`;
        // Add the rest of your displays here
        
        // Log to console
        console.log('Sum:', sum);
        console.log('Difference:', difference);
        // Add the rest of your console.log statements
    </script>
</body>
</html>
```

### Expected Output on Page:
```
Addition: 10 + 5 = 15
Subtraction: 10 - 5 = 5
Multiplication: 10 * 5 = 50
Division: 10 / 5 = 2
Remainder: 10 % 5 = 0
```

**💡 Hint:** The modulo operator `%` gives you the remainder. For example, `10 % 3 = 1` because 10 ÷ 3 = 3 remainder 1.

---

## Task 3: Shopping Cart Total

**Goal:** Calculate a shopping cart total with tax.

### Instructions:
1. Create a file called `shopping-cart.html`
2. Create variables for three items with their prices
3. Calculate the subtotal (sum of all prices)
4. Calculate tax (8% of subtotal)
5. Calculate the total (subtotal + tax)
6. Display all the information formatted nicely on the page

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Shopping Cart</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .receipt {
            background-color: white;
            padding: 20px;
            border: 2px dashed #333;
        }
        h2 {
            text-align: center;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="receipt">
        <h2>Shopping Cart Summary</h2>
        <p id="item1"></p>
        <p id="item2"></p>
        <p id="item3"></p>
        <hr>
        <p id="subtotal"></p>
        <p id="tax"></p>
        <hr>
        <p id="total"></p>
    </div>
    
    <script>
        // Item prices
        let item1Price = 29.99;
        let item2Price = 15.50;
        let item3Price = 42.00;
        let taxRate = 0.08;  // 8% tax
        
        // Calculate subtotal (add all three prices)
        let subtotal = item1Price + item2Price + item3Price;
        
        // Calculate tax (multiply subtotal by tax rate)
        let tax = subtotal * taxRate;
        
        // Calculate total (subtotal + tax)
        let total = subtotal + tax;
        
        // Display items
        document.getElementById('item1').textContent = `Item 1: $${item1Price.toFixed(2)}`;
        // Complete item2 and item3 displays
        
        // Display calculations (use .toFixed(2) to show 2 decimal places)
        document.getElementById('subtotal').textContent = `Subtotal: $${subtotal.toFixed(2)}`;
        // Complete tax display
        // Complete total display
        
        console.log('Subtotal:', subtotal);
        console.log('Tax:', tax);
        console.log('Total:', total);
    </script>
</body>
</html>
```

### Expected Output:
```
Shopping Cart Summary
---------------------
Item 1: $29.99
Item 2: $15.50
Item 3: $42.00
---------------------
Subtotal: $87.49
Tax (8%): $7.00
---------------------
Total: $94.49
```

**💡 Hint:** The `.toFixed(2)` method rounds numbers to 2 decimal places, perfect for money!

---

## Task 4: Counter with Increment/Decrement

**Goal:** Practice using `++` and `--`.

### Instructions:
1. Create a file called `score-tracker.html`
2. Create a variable called `score` starting at 0
3. Display the starting score
4. Use `++` to increase the score 5 times (one at a time)
5. Display the score after each increase
6. Use `--` to decrease the score 2 times
7. Display the final score

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Score Tracker</title>
</head>
<body>
    <h1>Game Score Tracker</h1>
    
    <p id="start"></p>
    <p id="point1"></p>
    <p id="point2"></p>
    <p id="point3"></p>
    <p id="point4"></p>
    <p id="point5"></p>
    <p id="penalty1"></p>
    <p id="penalty2"></p>
    <p id="final"></p>
    
    <script>
        // Starting score
        let score = 0;
        document.getElementById('start').textContent = `Starting score: ${score}`;
        
        // Increase score 5 times
        score++;  // This adds 1 to score
        document.getElementById('point1').textContent = `After point 1: ${score}`;
        
        score++;
        document.getElementById('point2').textContent = `After point 2: ${score}`;
        
        // You do the next 3 increases...
        
        // Decrease score 2 times
        score--;  // This subtracts 1 from score
        document.getElementById('penalty1').textContent = `After penalty 1: ${score}`;
        
        // You do the second decrease...
        
        // Display final
        document.getElementById('final').textContent = `Final Score: ${score}`;
    </script>
</body>
</html>
```

### Expected Display:
```
Starting score: 0
After point 1: 1
After point 2: 2
After point 3: 3
After point 4: 4
After point 5: 5
After penalty 1: 4
After penalty 2: 3
Final Score: 3
```

**💡 Remember:** 
- `score++` is the same as `score = score + 1`
- `score--` is the same as `score = score - 1`

---

## Task 5: Temperature Converter

**Goal:** Convert Celsius to Fahrenheit.

### Instructions:
1. Create a file called `temperature.html`
2. Create variables for temperatures in Celsius
3. Use the formula: `F = (C × 9/5) + 32`
4. Calculate and display both temperatures
5. Test with at least 3 different Celsius values

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Temperature Converter</title>
</head>
<body>
    <h1>Temperature Converter</h1>
    <h2>Celsius to Fahrenheit</h2>
    
    <p id="temp1"></p>
    <p id="temp2"></p>
    <p id="temp3"></p>
    
    <script>
        // Temperature in Celsius
        let celsius1 = 0;
        let celsius2 = 20;
        let celsius3 = 100;
        
        // Convert to Fahrenheit using formula: F = (C × 9/5) + 32
        let fahrenheit1 = (celsius1 * 9/5) + 32;
        let fahrenheit2 = (celsius2 * 9/5) + 32;
        // Calculate fahrenheit3 here...
        
        // Display conversions
        document.getElementById('temp1').textContent = `${celsius1}°C = ${fahrenheit1}°F`;
        document.getElementById('temp2').textContent = `${celsius2}°C = ${fahrenheit2}°F`;
        // Display temp3 here...
        
        console.log(`${celsius1}°C = ${fahrenheit1}°F`);
    </script>
</body>
</html>
```

### Example Output:
- 0°C = 32°F
- 20°C = 68°F
- 100°C = 212°F

**💡 Hint:** The formula has multiplication and division AND addition, so use parentheses to make sure multiplication/division happens first!

---

## Task 6: Percentage Calculator

**Goal:** Calculate percentages and practice division.

### Instructions:
1. Create a file called `percentages.html`
2. Create these scenarios:
   - You scored 42 out of 50 on a test - what percentage?
   - You answered 18 out of 20 questions correctly - what percentage?
   - You completed 75 out of 100 tasks - what percentage?

3. Display each calculation with the formula and result

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Percentage Calculator</title>
</head>
<body>
    <h1>Percentage Calculator</h1>
    
    <p id="test"></p>
    <p id="quiz"></p>
    <p id="tasks"></p>
    
    <script>
        // Test scenario
        let testScore = 42;
        let testMax = 50;
        let testPercent = (testScore / testMax) * 100;
        document.getElementById('test').textContent = `Test Score: ${testScore}/${testMax} = ${testPercent.toFixed(1)}%`;
        
        // Quiz scenario - you complete this
        let quizScore = 18;
        let quizMax = 20;
        // Calculate quizPercent here...
        // Display quiz result here...
        
        // Tasks scenario - you complete this
        let tasksComplete = 75;
        let tasksTotal = 100;
        // Calculate tasksPercent here...
        // Display tasks result here...
    </script>
</body>
</html>
```

### Formula:
```javascript
percentage = (score / maxScore) * 100
```

### Expected Output:
```
Test Score: 42/50 = 84.0%
Quiz Score: 18/20 = 90.0%
Tasks Completed: 75/100 = 75.0%
```

**💡 Hint:** Use `.toFixed(1)` to show one decimal place, or `.toFixed(0)` for no decimals.

---

## Task 7: Bill Splitter

**Goal:** Split a restaurant bill among friends.

### Instructions:
1. Create a file called `bill-split.html`
2. Create variables for the bill amount, number of people, and tip percentage
3. Calculate tip amount, total with tip, and amount per person
4. Display all calculations nicely formatted

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Bill Splitter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 400px;
            margin: 50px auto;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .bill {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <div class="bill">
        <h2>Bill Split Calculator</h2>
        <p id="bill"></p>
        <p id="tip"></p>
        <p id="total"></p>
        <hr>
        <p id="perPerson"></p>
    </div>
    
    <script>
        // Restaurant bill information
        let billAmount = 125.50;
        let numberOfPeople = 4;
        let tipPercent = 0.20;  // 20% tip
        
        // Calculate tip amount (bill × tip percentage)
        let tipAmount = billAmount * tipPercent;
        
        // Calculate total with tip (bill + tip)
        let totalWithTip = billAmount + tipAmount;
        
        // Calculate per person amount (total ÷ number of people)
        let perPerson = totalWithTip / numberOfPeople;
        
        // Display everything
        document.getElementById('bill').textContent = `Bill Amount: $${billAmount.toFixed(2)}`;
        // Complete the tip display (show tip percentage too!)
        // Complete the total display
        // Complete the per person display
        
        console.log('Tip:', tipAmount);
        console.log('Total:', totalWithTip);
        console.log('Per person:', perPerson);
    </script>
</body>
</html>
```

### Expected Output:
```
Bill Split Calculator
---------------------
Bill Amount: $125.50
Tip (20%): $25.10
Total with Tip: $150.60
---------------------
Split 4 ways: $37.65 per person
```

**✅ Success:** All amounts should be formatted to 2 decimal places using `.toFixed(2)`

**💡 Challenge:** Try changing the tip percentage to 15%, 18%, or 25% and see how it affects the calculations!

---

## Task 8: Compound Operators Practice

**Goal:** Practice using `+=`, `-=`, `*=`, `/=`.

### Instructions:
1. Create a file called `compound-ops.html`
2. Start with a variable: `let total = 100`
3. Perform these operations IN ORDER:
   - Add 50 using `+=`
   - Subtract 25 using `-=`
   - Multiply by 2 using `*=`
   - Divide by 5 using `/=`

4. Display the total after EACH operation

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Compound Operators</title>
</head>
<body>
    <h1>Compound Operators Practice</h1>
    
    <p id="start"></p>
    <p id="step1"></p>
    <p id="step2"></p>
    <p id="step3"></p>
    <p id="step4"></p>
    
    <script>
        // Starting value
        let total = 100;
        document.getElementById('start').textContent = `Starting value: ${total}`;
        
        // Step 1: Add 50
        total += 50;  // Same as: total = total + 50
        document.getElementById('step1').textContent = `After adding 50: ${total}`;
        
        // Step 2: Subtract 25
        // Use -= here
        // Display result
        
        // Step 3: Multiply by 2
        // Use *= here
        // Display result
        
        // Step 4: Divide by 5
        // Use /= here
        // Display result
        
        console.log('Final total:', total);
    </script>
</body>
</html>
```

### Expected Output:
```
Starting value: 100
After adding 50: 150
After subtracting 25: 125
After multiplying by 2: 250
After dividing by 5: 50
```

**💡 Remember:**
- `total += 50` means `total = total + 50`
- `total -= 25` means `total = total - 25`
- `total *= 2` means `total = total * 2`
- `total /= 5` means `total = total / 5`

---

## Challenge Task: Currency Converter

**Goal:** Create a multi-currency converter.

### Instructions:
1. Create a file called `currency-converter.html`
2. Start with an amount in US Dollars
3. Convert to at least 3 other currencies using the conversion rates provided
4. Display all conversions nicely formatted
5. Add CSS to make it look professional

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Currency Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        .converter {
            background-color: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        h1 {
            color: #333;
            text-align: center;
            border-bottom: 3px solid #667eea;
            padding-bottom: 10px;
        }
        .amount {
            font-size: 24px;
            color: #667eea;
            text-align: center;
            margin: 20px 0;
        }
        .conversion {
            font-size: 18px;
            padding: 10px;
            margin: 10px 0;
            background-color: #f8f9fa;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="converter">
        <h1>Currency Converter</h1>
        <div class="amount" id="usd"></div>
        
        <p class="conversion" id="euro"></p>
        <p class="conversion" id="pound"></p>
        <p class="conversion" id="yen"></p>
        <p class="conversion" id="cad"></p>
    </div>
    
    <script>
        // Starting amount in USD
        let usdAmount = 100;
        
        // Conversion rates (as of example date)
        let euroRate = 0.92;
        let poundRate = 0.79;
        let yenRate = 149.50;
        let cadRate = 1.36;
        
        // Display USD amount
        document.getElementById('usd').textContent = `$${usdAmount.toFixed(2)} USD equals:`;
        
        // Convert to Euros
        let euros = usdAmount * euroRate;
        document.getElementById('euro').textContent = `€${euros.toFixed(2)} EUR`;
        
        // Convert to British Pounds
        // Calculate and display here...
        
        // Convert to Japanese Yen
        // Calculate and display here...
        
        // Convert to Canadian Dollars
        // Calculate and display here...
        
        console.log('USD:', usdAmount);
        console.log('EUR:', euros);
    </script>
</body>
</html>
```

### Example Output:
```
Currency Converter
==================
$100.00 USD equals:

€92.00 EUR
£79.00 GBP
¥14,950.00 JPY
$136.00 CAD
```

### Bonus Challenges:
- Add more currencies (Mexican Peso: 17.25, Indian Rupee: 83.12)
- Show the conversion rates on the page
- Try different USD amounts
- Add even more styling with colors or borders

### Grading Yourself:
- ✅ Starts with a USD amount
- ✅ Converts to at least 3 currencies
- ✅ All amounts properly formatted with `.toFixed(2)`
- ✅ Display is clear and organized
- ✅ No errors in console
- ✅ Math is correct

---

## Challenge Task 2: Fitness Tracker

**Goal:** Track workout progress with calculations.

### Instructions:
1. Create a file called `fitness-tracker.html`
2. Track workout data with variables
3. Calculate progress metrics
4. Display everything in an organized way

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Fitness Tracker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #e8f5e9;
        }
        .tracker {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #2e7d32;
            text-align: center;
        }
        .stat {
            padding: 10px;
            margin: 10px 0;
            background-color: #f1f8e9;
            border-left: 4px solid #66bb6a;
        }
    </style>
</head>
<body>
    <div class="tracker">
        <h1>Fitness Progress Tracker</h1>
        
        <h3>Current Stats:</h3>
        <div class="stat" id="start"></div>
        <div class="stat" id="current"></div>
        <div class="stat" id="goal"></div>
        
        <h3>Progress:</h3>
        <div class="stat" id="lost"></div>
        <div class="stat" id="remaining"></div>
        <div class="stat" id="average"></div>
        <div class="stat" id="percent"></div>
        <div class="stat" id="estimate"></div>
    </div>
    
    <script>
        // Your fitness data
        let startWeight = 200;
        let currentWeight = 185;
        let goalWeight = 170;
        let weeksPassed = 8;
        
        // Calculate weight lost (starting weight - current weight)
        let weightLost = startWeight - currentWeight;
        
        // Calculate weight remaining (current weight - goal weight)
        let weightRemaining = currentWeight - goalWeight;
        
        // Calculate average loss per week (weight lost ÷ weeks passed)
        let averageLossPerWeek = weightLost / weeksPassed;
        
        // Calculate percentage complete (weight lost ÷ total needed) × 100
        let totalNeeded = startWeight - goalWeight;
        let percentComplete = (weightLost / totalNeeded) * 100;
        
        // Estimate weeks to goal (weight remaining ÷ average per week)
        let weeksToGoal = weightRemaining / averageLossPerWeek;
        
        // Display current stats
        document.getElementById('start').textContent = `Starting Weight: ${startWeight} lbs`;
        document.getElementById('current').textContent = `Current Weight: ${currentWeight} lbs`;
        document.getElementById('goal').textContent = `Goal Weight: ${goalWeight} lbs`;
        
        // Display progress (complete these using .toFixed() where needed)
        document.getElementById('lost').textContent = `Lost: ${weightLost} lbs`;
        // Complete the remaining displays...
        // Use .toFixed(2) for averageLossPerWeek
        // Use .toFixed(1) for percentComplete
        // Use .toFixed(1) for weeksToGoal
        
    </script>
</body>
</html>
```

### Expected Calculations:
```
Fitness Progress Tracker
========================
Starting Weight: 200 lbs
Current Weight: 185 lbs
Goal Weight: 170 lbs

Progress:
- Lost: 15 lbs
- Remaining: 15 lbs   (You need to figure this one out)
- Average loss: 1.88 lbs/week    (You need to figure this one out)
- Progress: 50.0% complete    (You need to figure this one out)
- Estimated weeks to goal: 8.0 weeks    (You need to figure this one out)
```

### Bonus Challenges:
- Calculate how many months until goal (weeks ÷ 4)
- Add a visual progress bar using CSS - `You can use AI to help with this CSS part.`
- Try different starting values to test your math

---

## Tips for Success
1. **Test your math manually first** - Use a calculator to verify
2. **Use parentheses** - Make order of operations clear: `(a + b) / 2`
3. **Format currency properly** - Always use `.toFixed(2)` for money
4. **Log values** - Check your calculations in the console as you go
5. **One step at a time** - Build calculations gradually
6. **Check order of operations** - Multiplication and division happen before addition and subtraction

## Common Mistakes to Avoid

❌ `let total = 10 + 5 * 2` (equals 20, not 30!)  
✅ `let total = (10 + 5) * 2` (equals 30)

❌ `let price = 19.99` then showing `$19.9` on page  
✅ `let price = 19.99` then using `$${price.toFixed(2)}` shows `$19.99`

❌ Forgetting to save variable changes:
```javascript
let score = 0;
score + 10;  // This doesn't save!
```
✅ Saving the change:
```javascript
let score = 0;
score = score + 10;  // or score += 10;
```

❌ Dividing by zero (causes `Infinity`)  
✅ Check your divisor is not zero before dividing

---

## Order of Operations (PEMDAS)
Remember: **P**arentheses, **E**xponents, **M**ultiplication, **D**ivision, **A**ddition, **S**ubtraction

```javascript
let result1 = 10 + 5 * 2;        // = 20 (multiply first)
let result2 = (10 + 5) * 2;      // = 30 (parentheses first)
let result3 = 100 / 10 + 5;      // = 15 (divide first)
let result4 = 100 / (10 + 5);    // = 6.67 (parentheses first)
```