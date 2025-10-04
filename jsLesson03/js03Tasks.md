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

### Expected Output on Page:
```
Addition: 10 + 5 = 15
Subtraction: 10 - 5 = 5
Multiplication: 10 * 5 = 50
Division: 10 / 5 = 2
Remainder: 10 % 5 = 0
```

**💡 Hint:** Create 5 different paragraph elements with ids, then populate them with results.

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

### Variables you need:
```javascript
let item1Price = 29.99;
let item2Price = 15.50;
let item3Price = 42.00;
let taxRate = 0.08;
```

### Expected Output:
```
Shopping Cart Summary
---------------------
Item 1: $29.99
Item 2: $15.50
Item 3: $42.00
Subtotal: $87.49
Tax (8%): $7.00
Total: $94.49
```

**💡 Hint:** Use `.toFixed(2)` to format prices to 2 decimal places.

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

**💡 Hint:** Create multiple paragraph elements, one for each score update.

---

## Task 5: Temperature Converter

**Goal:** Convert Celsius to Fahrenheit.

### Instructions:
1. Create a file called `temperature.html`
2. Create a variable for temperature in Celsius
3. Use the formula: `F = (C × 9/5) + 32`
4. Calculate and display both temperatures
5. Test with at least 3 different Celsius values

### Example:
- 0°C = 32°F
- 20°C = 68°F
- 100°C = 212°F

### Display Format:
```
Temperature Converter
---------------------
0°C = 32°F
20°C = 68°F
100°C = 212°F
```

**💡 Hint:** You can create multiple variables for different Celsius temperatures and convert each one.

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

### Formula:
```javascript
percentage = (score / maxScore) * 100
```

### Expected Output:
```
Test Score: 42/50 = 84%
Quiz Score: 18/20 = 90%
Tasks Completed: 75/100 = 75%
```

**💡 Hint:** Use `.toFixed(0)` or `.toFixed(1)` for clean percentage displays.

---

## Task 7: Bill Splitter

**Goal:** Split a restaurant bill among friends.

### Instructions:
1. Create a file called `bill-split.html`
2. Create variables for:
   - Total bill amount
   - Number of people
   - Tip percentage (as a decimal, like 0.18 for 18%)

3. Calculate:
   - Tip amount
   - Total with tip
   - Amount per person

4. Display all calculations nicely formatted

### Example Variables:
```javascript
let billAmount = 125.50;
let numberOfPeople = 4;
let tipPercent = 0.20;  // 20%
```

### Expected Output:
```
Bill Split Calculator
---------------------
Bill Amount: $125.50
Tip (20%): $25.10
Total with Tip: $150.60
Split 4 ways: $37.65 per person
```

**✅ Success:** All amounts should be formatted to 2 decimal places.

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

### Expected Output:
```
Starting value: 100
After adding 50: 150
After subtracting 25: 125
After multiplying by 2: 250
After dividing by 5: 50
```

**💡 Hint:** Log each step to verify your math is correct.

---

## Challenge Task: Currency Converter

**Goal:** Create a multi-currency converter.

### Instructions:
1. Create a file called `currency-converter.html`
2. Start with an amount in US Dollars
3. Convert to at least 3 other currencies:
   - Euros (multiply by 0.92)
   - British Pounds (multiply by 0.79)
   - Japanese Yen (multiply by 149.50)
   - Canadian Dollars (multiply by 1.36)

4. Display all conversions nicely formatted
5. Add CSS to make it look professional

### Example:
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
- Add more currencies
- Show the conversion rates
- Calculate the total if you had that amount in all currencies
- Add colors or styling to make it visually appealing
- Show percentages comparing each currency to USD

### Grading Yourself:
- ✅ Starts with a USD amount
- ✅ Converts to at least 3 currencies
- ✅ All amounts properly formatted
- ✅ Display is clear and organized
- ✅ No errors in console
- ✅ Math is correct

---

## Challenge Task 2: Fitness Tracker

**Goal:** Track workout progress with calculations.

### Instructions:
1. Create a file called `fitness-tracker.html`
2. Track this data:
   - Starting weight
   - Current weight
   - Goal weight
   - Weeks of working out

3. Calculate and display:
   - Weight lost so far
   - Weight remaining to goal
   - Average weight loss per week
   - Percentage of goal achieved
   - Estimated weeks to goal (at current rate)

### Example Variables:
```javascript
let startWeight = 200;
let currentWeight = 185;
let goalWeight = 170;
let weeksPassed = 8;
```

### Expected Calculations:
```
Fitness Progress Tracker
========================
Starting Weight: 200 lbs
Current Weight: 185 lbs
Goal Weight: 170 lbs

Progress So Far:
- Lost: 15 lbs
- Remaining: 15 lbs
- Average loss: 1.88 lbs/week
- Progress: 50% complete
- Estimated weeks to goal: 8 weeks
```

### Bonus:
- Add motivational messages based on progress
- Calculate BMI (research the formula)
- Track calories burned
- Add styling with colors (green for progress bars, etc.)

---

## Tips for Success
1. **Test your math manually first** - Use a calculator to verify
2. **Use parentheses** - Make order of operations clear
3. **Format currency properly** - Always use `.toFixed(2)` for money
4. **Log values** - Check your calculations in the console
5. **One step at a time** - Build calculations gradually

## Common Mistakes to Avoid
❌ Forgetting order of operations
✅ Use parentheses: `(a + b) / 2`

❌ Not rounding decimals
✅ Use `.toFixed(2)` for money

❌ Dividing by zero (causes Infinity)
✅ Check your divisor is not zero

❌ Confusing `=` with `==`
✅ `=` assigns, `==` compares (we'll learn this soon)