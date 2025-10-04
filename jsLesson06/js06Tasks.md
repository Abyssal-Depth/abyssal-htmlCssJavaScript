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
            let score = Number(input.value);
            
            // Validate input
            if (score < 0 || score > 100) {
                result.textContent = 'Please enter a score between 0 and 100!';
                result.style.backgroundColor = '#ffcdd2';
                result.style.color = '#c62828';
            }
            // Check grade ranges
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

---

## Task 2: Simple Number Checker

**Goal:** Practice basic if-else statements.

### Instructions:
1. Create a file called `number-checker.html`
2. Create an input for a number and a button
3. When button is clicked, check if the number is:
   - Positive (> 0)
   - Negative (< 0)
   - Zero (=== 0)
4. Display the result

### Example Output:
- Input: 5 → "The number is positive"
- Input: -3 → "The number is negative"
- Input: 0 → "The number is zero"

**💡 Hint:** Use if-else if-else structure.

---

## Task 3: Even or Odd

**Goal:** Use the modulo operator (%) with conditionals.

### Instructions:
1. Create a file called `even-odd.html`
2. Create an input and button
3. When button is clicked:
   - Check if number is even or odd
   - Display result with different colors

### How to Check:
```javascript
if (number % 2 === 0) {
    // Even
} else {
    // Odd
}
```

**Bonus:** Add validation to ensure a number was entered.

---

## Task 4: Voting Eligibility

**Goal:** Practice comparison operators.

### Instructions:
1. Create a file called `voting-check.html`
2. Create an input for age and a button
3. Check if person can vote (age >= 18)
4. Display one of these messages:
   - "You can vote! 🗳️" (if 18 or older)
   - "You cannot vote yet. Wait X more years." (if under 18)

### Bonus:
- Calculate how many years until they can vote
- Add different styling for each message

**💡 Hint:** For years remaining: `18 - age`

---

## Task 5: Password Strength Checker

**Goal:** Practice multiple conditions with logical operators.

### Instructions:
1. Create a file called `password-checker.html`
2. Create a password input and button
3. Check password strength based on length:
   - Less than 6 characters: "Weak" (red)
   - 6-10 characters: "Medium" (orange)
   - More than 10 characters: "Strong" (green)
4. Display the strength with appropriate color

### Bonus:
- Check if password contains numbers
- Check if password contains uppercase letters
- Show specific improvement suggestions

---

## Task 6: Temperature Advisory

**Goal:** Use if-else if chains.

### Instructions:
1. Create a file called `temp-advisory.html`
2. Create an input for temperature (Fahrenheit) and button
3. Display advisory based on temperature:
   - Below 32°: "Freezing! Stay inside! ❄️"
   - 32° - 50°: "Cold! Wear a jacket! 🧥"
   - 51° - 70°: "Nice weather! 🌤️"
   - 71° - 85°: "Warm! 🌞"
   - Above 85°: "Hot! Stay hydrated! 🔥"

### Bonus:
- Change background color based on temperature
- Add weather emoji
- Create a Celsius version

---

## Task 7: Login Form

**Goal:** Practice combining conditions with AND operator.

### Instructions:
1. Create a file called `simple-login.html`
2. Create inputs for username and password
3. Set correct credentials (hardcoded):
   - Username: "student"
   - Password: "learn123"
4. When login button clicked:
   - If both fields empty: "Please fill in all fields"
   - If both correct: "Login successful! ✅"
   - If either wrong: "Invalid credentials ❌"

### Bonus:
- Add a "show password" toggle
- Disable button if fields are empty
- Add a character counter for password

**💡 Hint:** Use `username === 'student' && password === 'learn123'`

---

## Task 8: Discount Calculator

**Goal:** Practice nested conditionals and calculations.

### Instructions:
1. Create a file called `discount-calc.html`
2. Create inputs for:
   - Product price
   - Customer age
3. Apply discounts based on rules:
   - Kids under 12: 20% off
   - Seniors 65+: 15% off
   - Everyone else: No discount
   - If purchase over $100: Add additional 10% off
4. Display original price, discount, and final price

### Example Output:
```
Original Price: $120.00
Discount: 30% (Senior + Over $100)
Final Price: $84.00
```

---

## Task 9: Traffic Light Simulator

**Goal:** Practice multiple conditions and styling.

### Instructions:
1. Create a file called `traffic-light.html`
2. Create three div elements (styled as circles) for:
   - Red light
   - Yellow light
   - Green light
3. Create three buttons: "Red", "Yellow", "Green"
4. When each button is clicked:
   - Turn on that light (bright color)
   - Turn off other lights (dim/gray)
   - Display message: "STOP", "CAUTION", or "GO"

### CSS Hint:
```css
.light {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin: 10px;
}
.light-off {
    background-color: #ddd;
}
```

---

## Task 10: BMI Calculator

**Goal:** Practice calculations with multiple conditional ranges.

### Instructions:
1. Create a file called `bmi-calculator.html`
2. Create inputs for:
   - Weight (in pounds)
   - Height (in inches)
3. Calculate BMI: `(weight / (height * height)) * 703`
4. Display BMI category:
   - Below 18.5: "Underweight"
   - 18.5 - 24.9: "Normal weight"
   - 25.0 - 29.9: "Overweight"
   - 30.0 and above: "Obese"
5. Show BMI number and category with color coding

### Bonus:
- Add metric system option (kg and cm)
- Show ideal weight range
- Add visual progress bar

---

## Challenge Task: Quiz Game

**Goal:** Create a multi-question quiz with scoring.

### Instructions:
1. Create a file called `quiz-game.html`
2. Create a quiz with at least 3 questions
3. Use radio buttons or buttons for answers
4. Track the score
5. After all questions, show:
   - Total score (e.g., "You got 2 out of 3 correct")
   - Percentage
   - Message based on score:
     - 100%: "Perfect! 🏆"
     - 70-99%: "Great job! 🌟"
     - 50-69%: "Good try! 👍"
     - Below 50%: "Keep practicing! 📚"

### Example Question Structure:
```
Question 1: What is 5 + 3?
○ 7
○ 8 (correct)
○ 9
```

### Bonus Challenges:
- Add a "Next Question" button
- Show correct answer if wrong
- Add a timer for each question
- Highlight correct/wrong answers
- Store high score

---

## Challenge Task 2: Shipping Calculator

**Goal:** Complex conditionals with multiple factors.

### Instructions:
1. Create a file called `shipping-calc.html`
2. Create inputs for:
   - Order total (dollars)
   - Shipping destination (dropdown: Domestic/International)
   - Shipping speed (dropdown: Standard/Express)

3. Calculate shipping cost based on rules:
   - **Domestic Standard:** $5.99 (free if order > $50)
   - **Domestic Express:** $12.99 (free if order > $100)
   - **International Standard:** $19.99 (free if order > $150)
   - **International Express:** $39.99 (free if order > $200)

4. Display:
   - Subtotal
   - Shipping cost
   - Total

### Bonus:
- Add weight-based pricing
- Add handling fee for fragile items
- Show estimated delivery date
- Add tax calculation by state

### Grading Yourself:
- ✅ All shipping options work correctly
- ✅ Free shipping thresholds work
- ✅ Calculations are accurate
- ✅ Display is clear and formatted
- ✅ Input validation included

---

## Challenge Task 3: Character Creator

**Goal:** Use conditionals to build a character profile.

### Instructions:
1. Create a file called `character-creator.html`
2. Create a form with options:
   - Character class (Warrior/Mage/Rogue)
   - Starting weapon choice
   - Difficulty (Easy/Normal/Hard)

3. Based on choices, set character stats:
   - Different health, attack, defense for each class
   - Bonus stats from weapon choice
   - Modify stats based on difficulty

4. Display complete character sheet with:
   - All stats
   - Special abilities (based on class)
   - Starting equipment
   - Character portrait/icon (emoji or color)

### Example Logic:
```javascript
if (characterClass === 'Warrior') {
    health = 150;
    attack = 20;
    defense = 30;
} else if (characterClass === 'Mage') {
    health = 80;
    attack = 40;
    defense = 10;
}

if (difficulty === 'Hard') {
    health = health * 0.8; // 20% less health
}
```

---

## Tips for Success
1. **Test all paths** - Try every possible condition
2. **Order matters** - Put most specific conditions first
3. **Use === not ==** - Avoid type conversion issues
4. **Validate input** - Always check for invalid data
5. **Console.log conditions** - Debug by logging true/false values

## Common Mistakes to Avoid
❌ Using = instead of ===
✅ `if (age === 18)` not `if (age = 18)`

❌ Wrong order in else-if chains
✅ Start with highest/most specific values

❌ Forgetting to convert input to number
✅ `let age = Number(input.value);`

❌ Not handling edge cases
✅ Check for empty, negative, or extreme values
