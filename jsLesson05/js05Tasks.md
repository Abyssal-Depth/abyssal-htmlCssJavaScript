# Lesson 05 Tasks: Events and Interactivity

---

## Task 1: GUIDED EXAMPLE - Click Counter

**Follow these steps to create an interactive click counter.**

### Step 1: Create the HTML File
Create a file called `click-counter.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Click Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #f0f0f0;
        }
        .container {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            max-width: 400px;
            margin: 0 auto;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        #count {
            font-size: 64px;
            color: #2196f3;
            margin: 30px 0;
            font-weight: bold;
        }
        button {
            padding: 15px 40px;
            font-size: 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 8px;
            transition: transform 0.1s;
        }
        button:hover {
            transform: scale(1.05);
        }
        #clickBtn {
            background-color: #4caf50;
            color: white;
        }
        #resetBtn {
            background-color: #f44336;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Click Counter</h1>
        <div id="count">0</div>
        <button id="clickBtn">Click Me!</button>
        <button id="resetBtn">Reset</button>
        <p id="message">Start clicking!</p>
    </div>
    
    <script>
        // Initialize counter
        let clicks = 0;
        
        // Select elements
        let countDisplay = document.getElementById('count');
        let clickBtn = document.getElementById('clickBtn');
        let resetBtn = document.getElementById('resetBtn');
        let message = document.getElementById('message');
        
        // Click button event
        clickBtn.addEventListener('click', function() {
            clicks++;
            countDisplay.textContent = clicks;
            message.textContent = `You've clicked ${clicks} times!`;
        });
        
        // Reset button event
        resetBtn.addEventListener('click', function() {
            clicks = 0;
            countDisplay.textContent = clicks;
            message.textContent = 'Counter reset! Start clicking!';
        });
    </script>
</body>
</html>
```

### Step 2: Test It
1. Open the file in your browser
2. Click the "Click Me!" button multiple times
3. Watch the counter increase
4. Click "Reset" to start over

### Step 3: Experiment
Try adding:
- A message that appears after 10 clicks
- Different colors when count reaches certain numbers
- A button to decrease the count

**✅ Checkpoint:** Counter should increase with each click and reset to 0.

---

## Task 2: Button Click Practice

**Goal:** Practice basic click events.

### Instructions:
1. Create a file called `button-practice.html`
2. Create 3 buttons with ids "btn1", "btn2", "btn3"
3. Create a paragraph with id "output"
4. When each button is clicked, display a different message in the output paragraph

### Example Messages:
- Button 1: "You clicked button 1!"
- Button 2: "You clicked button 2!"
- Button 3: "You clicked button 3!"

**💡 Hint:** You'll need three separate event listeners, one for each button.

---

## Task 3: Hover Effects

**Goal:** Practice mouse enter and mouse leave events.

### Instructions:
1. Create a file called `hover-box.html`
2. Create a div with id "hoverBox" (give it a background color and size)
3. Create a paragraph with id "status"
4. When mouse enters the box:
   - Change box background to yellow
   - Display "Mouse is inside!" in the status
5. When mouse leaves the box:
   - Change box background back to original color
   - Display "Mouse left!" in the status

**💡 Hint:** Use `mouseenter` and `mouseleave` events.

---

## Task 4: Text Input Greeting

**Goal:** Practice working with input values.

### Instructions:
1. Create a file called `greeting-app.html`
2. Create:
   - A text input with id "nameInput"
   - A button with id "greetBtn"
   - A div with id "greeting"
3. When button is clicked:
   - Get the value from the input
   - Display "Hello, [name]!" in the greeting div
   - Change the greeting text color

### Bonus:
- Clear the input field after clicking
- Show an error if input is empty

**💡 Hint:** Use `.value` to get input text: `input.value`

---

## Task 5: Show/Hide Toggle

**Goal:** Create a button that shows and hides content.

### Instructions:
1. Create a file called `toggle-content.html`
2. Create:
   - A button with id "toggleBtn" (text: "Show/Hide")
   - A div with id "content" containing some paragraphs
3. Create a CSS class `.hidden` with `display: none`
4. When button is clicked, toggle the hidden class on the content div

### Expected Behavior:
- Content starts visible
- First click hides it
- Second click shows it
- Continues toggling

**💡 Hint:** Use `.classList.toggle('hidden')`

---

## Task 6: Background Color Picker

**Goal:** Change page background based on button clicks.

### Instructions:
1. Create a file called `color-picker.html`
2. Create 5 buttons for different colors (red, blue, green, yellow, purple)
3. When each button is clicked, change the body background to that color
4. Add a "Random" button that sets a random background color

### Random Color Hint:
```javascript
let r = Math.floor(Math.random() * 256);
let g = Math.floor(Math.random() * 256);
let b = Math.floor(Math.random() * 256);
document.body.style.backgroundColor = `rgb(${r}, ${g}, ${b})`;
```

---

## Task 7: Interactive Calculator

**Goal:** Build a simple addition calculator.

### Instructions:
1. Create a file called `simple-calc.html`
2. Create:
   - Two number inputs (id "num1" and "num2")
   - A button "Calculate" (id "calcBtn")
   - A div to display the result (id "result")
3. When button is clicked:
   - Get both input values
   - Convert them to numbers
   - Add them together
   - Display "Result: [answer]"

### Example:
- Input 1: 5
- Input 2: 3
- Result: "Result: 8"

**💡 Hint:** Convert strings to numbers: `Number(input.value)`

---

## Task 8: Like Button

**Goal:** Create a social media-style like button.

### Instructions:
1. Create a file called `like-button.html`
2. Create:
   - A button with id "likeBtn" (text: "❤️ Like")
   - A counter display showing number of likes
3. When clicked:
   - Increment the like count
   - Change button text to "❤️ Liked" and button color
   - Prevent clicking again (disable button)

### Bonus:
- Add an "Unlike" button to decrease count
- Change heart emoji from ♡ to ❤️ when liked

**💡 Hint:** Disable button with `button.disabled = true`

---

## Task 9: Keypress Detector

**Goal:** Detect and display keyboard input.

### Instructions:
1. Create a file called `key-detector.html`
2. Create a large display div with id "keyDisplay"
3. Listen for keypress events on the document
4. Display the pressed key in large text
5. Show additional info: "You pressed: [key]"

### Bonus:
- Change display color for different types of keys (letters vs numbers)
- Keep track of how many keys have been pressed

**💡 Hint:** Use `document.addEventListener('keypress', function(event) {...})`

---

## Task 10: Live Character Counter

**Goal:** Count characters as user types (like Twitter).

### Instructions:
1. Create a file called `char-counter.html`
2. Create:
   - A textarea with id "textInput"
   - A display showing character count (id "charCount")
   - A max character limit (like 280)
3. As user types, update the count in real-time
4. Change count color to red when over limit

### Display Format:
"Characters: 45 / 280"

**💡 Hint:** Use the `input` event and `.value.length` to get character count

---

## Challenge Task: Todo List

**Goal:** Create an interactive todo list.

### Instructions:
1. Create a file called `todo-list.html`
2. Create:
   - An input field for new todos
   - An "Add" button
   - A div to display todos
   - A counter showing total todos

3. When "Add" is clicked:
   - Get the input value
   - Create a new paragraph with the todo text
   - Add it to the display div
   - Clear the input
   - Update the counter

### Bonus Challenges:
- Add a "Clear All" button
- Add a "Done" button next to each todo that crosses it out
- Prevent adding empty todos
- Add a timestamp to each todo
- Style todos with alternating colors

### Grading Yourself:
- ✅ Can add new todos
- ✅ Input clears after adding
- ✅ Counter updates correctly
- ✅ Todos display in a list
- ✅ Has styling and looks organized

---

## Challenge Task 2: Temperature Converter

**Goal:** Convert between Celsius and Fahrenheit interactively.

### Instructions:
1. Create a file called `temp-converter.html`
2. Create:
   - Input for temperature value
   - Two buttons: "Convert to °F" and "Convert to °C"
   - Display area for result

3. When "Convert to °F" is clicked:
   - Get Celsius value
   - Convert to Fahrenheit: F = (C × 9/5) + 32
   - Display result

4. When "Convert to °C" is clicked:
   - Get Fahrenheit value
   - Convert to Celsius: C = (F - 32) × 5/9
   - Display result

### Bonus:
- Add dropdown to select conversion direction
- Show both values at once
- Add input validation
- Style with colors (blue for cold, red for hot)
- Add a "Swap" button to switch between units

---

## Challenge Task 3: Quiz App

**Goal:** Create a simple one-question quiz.

### Instructions:
1. Create a file called `quiz-app.html`
2. Display a question with multiple choice options (use radio buttons or buttons)
3. User clicks their answer
4. Show feedback: "Correct!" or "Wrong! The answer is..."
5. Keep track of score

### Example Question:
"What does HTML stand for?"
- Hyper Text Markup Language ✓
- Hot Mail Language
- How To Make Lasagna

### Bonus:
- Add multiple questions
- Add a "Next Question" button
- Show final score
- Add a timer
- Add question counter (Question 1 of 5)

---

## Tips for Success
1. **Select elements first** - Always get your elements before adding listeners
2. **Console.log everything** - Check that your events are firing
3. **One event at a time** - Add and test each event separately
4. **Use meaningful IDs** - Makes code easier to understand
5. **Test user interactions** - Try clicking, typing, hovering multiple times

## Common Mistakes to Avoid
❌ Adding event listener before element exists
✅ Put script at end of body

❌ Forgetting to use `.value` for inputs
✅ `let text = input.value;`

❌ Not updating variables AND display
✅ Update both: `count++; display.textContent = count;`

❌ Misspelling event names ('clik' vs 'click')
✅ Double-check event type spelling