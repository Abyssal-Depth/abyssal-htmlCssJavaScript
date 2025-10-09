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
        // Initialize counter variable
        let clicks = 0;
        
        // Select all the elements we need
        let countDisplay = document.getElementById('count');
        let clickBtn = document.getElementById('clickBtn');
        let resetBtn = document.getElementById('resetBtn');
        let message = document.getElementById('message');
        
        // Add click event listener to the click button
        clickBtn.addEventListener('click', function() {
            clicks++;  // Increase the counter
            countDisplay.textContent = clicks;  // Update the display
            message.textContent = `You've clicked ${clicks} times!`;
        });
        
        // Add click event listener to the reset button
        resetBtn.addEventListener('click', function() {
            clicks = 0;  // Reset counter to 0
            countDisplay.textContent = clicks;  // Update display
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
- A message that appears after 10 clicks (use an if statement)
- Different colors when count reaches certain numbers
- A button to decrease the count

**✅ Checkpoint:** Counter should increase with each click and reset to 0.

---

## Task 2: Button Click Practice

**Goal:** Practice basic click events.

### Instructions:
1. Create a file called `button-practice.html`
2. Create 3 buttons with different ids
3. When each button is clicked, display a different message

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Button Practice</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
        }
        button {
            padding: 15px 30px;
            font-size: 18px;
            margin: 10px;
            cursor: pointer;
            border-radius: 5px;
            border: 2px solid #333;
        }
        #btn1 { background-color: #ff9800; }
        #btn2 { background-color: #2196f3; }
        #btn3 { background-color: #4caf50; }
        #output {
            margin-top: 30px;
            font-size: 24px;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Click Any Button</h1>
    
    <button id="btn1">Button 1</button>
    <button id="btn2">Button 2</button>
    <button id="btn3">Button 3</button>
    
    <p id="output">Click a button to see a message!</p>
    
    <script>
        // Select all elements
        let btn1 = document.getElementById('btn1');
        let btn2 = document.getElementById('btn2');
        let btn3 = document.getElementById('btn3');
        let output = document.getElementById('output');
        
        // Add event listener to button 1
        btn1.addEventListener('click', function() {
            output.textContent = 'You clicked button 1!';
        });
        
        // Add event listener to button 2
        // Your code here...
        
        // Add event listener to button 3
        // Your code here...
    </script>
</body>
</html>
```

### Expected Behavior:
- Click Button 1 → "You clicked button 1!"
- Click Button 2 → "You clicked button 2!"
- Click Button 3 → "You clicked button 3!"

**💡 Hint:** Follow the pattern from button 1 for the other two buttons.

---

## Task 3: Hover Effects

**Goal:** Practice mouse enter and mouse leave events.

### Instructions:
1. Create a file called `hover-box.html`
2. Create a colored box that changes when you hover over it
3. Display status messages when mouse enters and leaves

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Hover Box</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
        }
        #hoverBox {
            width: 300px;
            height: 300px;
            background-color: lightblue;
            margin: 30px auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        #status {
            font-size: 20px;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Hover Over the Box</h1>
    
    <div id="hoverBox">
        Hover over me!
    </div>
    
    <p id="status">Waiting for hover...</p>
    
    <script>
        // Select elements
        let hoverBox = document.getElementById('hoverBox');
        let status = document.getElementById('status');
        
        // When mouse enters the box
        hoverBox.addEventListener('mouseenter', function() {
            hoverBox.style.backgroundColor = 'yellow';
            status.textContent = 'Mouse is inside!';
        });
        
        // When mouse leaves the box
        hoverBox.addEventListener('mouseleave', function() {
            // Change background back to lightblue
            // Change status text to "Mouse left!"
            // Your code here...
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Mouse enters box → Background turns yellow, status shows "Mouse is inside!"
- Mouse leaves box → Background returns to light blue, status shows "Mouse left!"

**💡 Hint:** The `mouseleave` event should reverse what `mouseenter` did.

---

## Task 4: Text Input Greeting

**Goal:** Practice working with input values.

### Instructions:
1. Create a file called `greeting-app.html`
2. Get text from an input field
3. Display a personalized greeting when button is clicked

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Greeting App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #e3f2fd;
        }
        .container {
            background-color: white;
            padding: 40px;
            max-width: 500px;
            margin: 0 auto;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        input {
            padding: 10px;
            font-size: 18px;
            border: 2px solid #2196f3;
            border-radius: 5px;
            width: 250px;
        }
        button {
            padding: 10px 30px;
            font-size: 18px;
            background-color: #2196f3;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-left: 10px;
        }
        button:hover {
            background-color: #1976d2;
        }
        #greeting {
            margin-top: 30px;
            font-size: 28px;
            font-weight: bold;
            color: #2196f3;
            min-height: 40px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Greeting Generator</h1>
        <p>Enter your name:</p>
        
        <input type="text" id="nameInput" placeholder="Your name here">
        <button id="greetBtn">Greet Me!</button>
        
        <div id="greeting"></div>
    </div>
    
    <script>
        // Select elements
        let nameInput = document.getElementById('nameInput');
        let greetBtn = document.getElementById('greetBtn');
        let greeting = document.getElementById('greeting');
        
        // Add click event to button
        greetBtn.addEventListener('click', function() {
            // Get the value from the input
            let name = nameInput.value;
            
            // Display the greeting
            greeting.textContent = `Hello, ${name}!`;
            
            // Change the greeting color
            greeting.style.color = '#4caf50';
            
            // Bonus: Clear the input field
            // nameInput.value = '';
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- User types "Sarah" and clicks button
- Display shows "Hello, Sarah!"
- Greeting text turns green

### Bonus Challenges:
- Clear the input field after clicking (uncomment the bonus line)
- Check if input is empty and show "Please enter a name!" instead
- Make the greeting text larger when displaying

**💡 Hint:** Use `.value` to get text from an input: `input.value`

---

## Task 5: Show/Hide Toggle

**Goal:** Create a button that shows and hides content.

### Instructions:
1. Create a file called `toggle-content.html`
2. Create a button that toggles visibility of content
3. Use CSS classes to show/hide

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Toggle Content</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
        }
        button {
            padding: 12px 25px;
            font-size: 16px;
            cursor: pointer;
            background-color: #2196f3;
            color: white;
            border: none;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        #content {
            background-color: #f0f0f0;
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid #2196f3;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <h1>Toggle Content Demo</h1>
    
    <button id="toggleBtn">Show/Hide</button>
    
    <div id="content">
        <h2>Hidden Content</h2>
        <p>This is some content that can be shown or hidden.</p>
        <p>Click the button above to toggle this content!</p>
        <p>Pretty cool, right?</p>
    </div>
    
    <script>
        // Select elements
        let toggleBtn = document.getElementById('toggleBtn');
        let content = document.getElementById('content');
        
        // Add click event to toggle button
        toggleBtn.addEventListener('click', function() {
            // Toggle the 'hidden' class on the content
            content.classList.toggle('hidden');
            
            // This will add the class if it's not there
            // Or remove it if it is there
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Content starts visible
- First click → Content hides
- Second click → Content shows
- Third click → Content hides again
- And so on...

**💡 Key Concept:** `.classList.toggle()` is perfect for show/hide buttons because it automatically adds or removes the class!

---

## Task 6: Background Color Picker

**Goal:** Change page background based on button clicks.

### Instructions:
1. Create a file called `color-picker.html`
2. Create buttons for different colors
3. Change body background when clicked
4. Add a random color button

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Color Picker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            transition: background-color 0.3s ease;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            display: inline-block;
        }
        button {
            padding: 15px 30px;
            font-size: 18px;
            margin: 10px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            color: white;
            font-weight: bold;
        }
        #redBtn { background-color: #f44336; }
        #blueBtn { background-color: #2196f3; }
        #greenBtn { background-color: #4caf50; }
        #yellowBtn { background-color: #ffeb3b; color: #333; }
        #purpleBtn { background-color: #9c27b0; }
        #randomBtn { 
            background: linear-gradient(135deg, #f44336, #2196f3, #4caf50);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Background Color Picker</h1>
        <p>Click a button to change the background!</p>
        
        <div>
            <button id="redBtn">Red</button>
            <button id="blueBtn">Blue</button>
            <button id="greenBtn">Green</button>
            <button id="yellowBtn">Yellow</button>
            <button id="purpleBtn">Purple</button>
        </div>
        <button id="randomBtn">Random Color</button>
    </div>
    
    <script>
        // Select all color buttons
        let redBtn = document.getElementById('redBtn');
        let blueBtn = document.getElementById('blueBtn');
        let greenBtn = document.getElementById('greenBtn');
        let yellowBtn = document.getElementById('yellowBtn');
        let purpleBtn = document.getElementById('purpleBtn');
        let randomBtn = document.getElementById('randomBtn');
        
        // Red button event
        redBtn.addEventListener('click', function() {
            document.body.style.backgroundColor = '#f44336';
        });
        
        // Blue button event
        blueBtn.addEventListener('click', function() {
            document.body.style.backgroundColor = '#2196f3';
        });
        
        // Complete the rest of the color buttons...
        // Green button
        // Your code here...
        
        // Yellow button
        // Your code here...
        
        // Purple button
        // Your code here...
        
        // Random color button
        randomBtn.addEventListener('click', function() {
            // Generate random RGB values (0-255)
            let r = Math.floor(Math.random() * 256);
            let g = Math.floor(Math.random() * 256);
            let b = Math.floor(Math.random() * 256);
            
            // Set background to random color
            document.body.style.backgroundColor = `rgb(${r}, ${g}, ${b})`;
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Each color button changes background to that color
- Random button picks a random color each time

**💡 Hint:** The pattern is the same for each color button - just change the color value!

---

## Task 7: Interactive Calculator

**Goal:** Build a simple addition calculator.

### Instructions:
1. Create a file called `simple-calc.html`
2. Get two numbers from inputs
3. Add them together and display the result

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #f5f5f5;
        }
        .calculator {
            background-color: white;
            padding: 40px;
            max-width: 400px;
            margin: 0 auto;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        input {
            width: 100px;
            padding: 10px;
            font-size: 24px;
            text-align: center;
            border: 2px solid #2196f3;
            border-radius: 5px;
            margin: 10px;
        }
        button {
            padding: 12px 40px;
            font-size: 18px;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {
            background-color: #45a049;
        }
        #result {
            margin-top: 30px;
            font-size: 32px;
            font-weight: bold;
            color: #2196f3;
            min-height: 40px;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>Simple Calculator</h1>
        
        <div>
            <input type="number" id="num1" placeholder="0">
            <span style="font-size: 32px;">+</span>
            <input type="number" id="num2" placeholder="0">
        </div>
        
        <button id="calcBtn">Calculate</button>
        
        <div id="result"></div>
    </div>
    
    <script>
        // Select elements
        let num1Input = document.getElementById('num1');
        let num2Input = document.getElementById('num2');
        let calcBtn = document.getElementById('calcBtn');
        let result = document.getElementById('result');
        
        // Add click event to calculate button
        calcBtn.addEventListener('click', function() {
            // Get the values from both inputs
            let num1 = num1Input.value;
            let num2 = num2Input.value;
            
            // Convert strings to numbers
            num1 = Number(num1);
            num2 = Number(num2);
            
            // Add them together
            let sum = num1 + num2;
            
            // Display the result
            result.textContent = `Result: ${sum}`;
            
            console.log(`${num1} + ${num2} = ${sum}`);
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Enter 5 and 3
- Click Calculate
- See "Result: 8"

### Bonus Challenges:
- Add subtraction, multiplication, and division buttons
- Show an error if inputs are empty
- Add a "Clear" button to reset inputs

**💡 Important:** Always convert input values to numbers using `Number()` or they'll be treated as text!

---

## Task 8: Like Button

**Goal:** Create a social media-style like button.

### Instructions:
1. Create a file called `like-button.html`
2. Track likes with a counter
3. Disable button after clicking (prevent double-liking)

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Like Button</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #f0f0f0;
        }
        .post {
            background-color: white;
            max-width: 400px;
            margin: 0 auto;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        #likeBtn {
            padding: 15px 30px;
            font-size: 20px;
            background-color: white;
            border: 2px solid #e91e63;
            color: #e91e63;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s;
        }
        #likeBtn:hover:not(:disabled) {
            background-color: #e91e63;
            color: white;
        }
        #likeBtn:disabled {
            background-color: #e91e63;
            color: white;
            cursor: not-allowed;
            opacity: 0.8;
        }
        #likeCount {
            font-size: 18px;
            margin-top: 15px;
            color: #666;
        }
    </style>
</head>
<body>
    <div class="post">
        <h2>Check out this awesome post!</h2>
        <p>Click the button below to show your appreciation!</p>
        
        <button id="likeBtn">♡ Like</button>
        
        <p id="likeCount">0 likes</p>
    </div>
    
    <script>
        // Initialize like counter
        let likes = 0;
        
        // Select elements
        let likeBtn = document.getElementById('likeBtn');
        let likeCount = document.getElementById('likeCount');
        
        // Add click event
        likeBtn.addEventListener('click', function() {
            // Increment likes
            likes++;
            
            // Update the count display
            likeCount.textContent = `${likes} likes`;
            
            // Change button text to show it's liked
            likeBtn.textContent = '❤️ Liked';
            
            // Disable the button so they can't like again
            likeBtn.disabled = true;
            
            console.log('Post liked! Total likes:', likes);
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Starts at "0 likes"
- Click button → Changes to "❤️ Liked", shows "1 likes", button becomes disabled
- Can't click again

### Bonus Challenges:
- Add an "Unlike" button to decrease count and re-enable like button
- Change the heart from ♡ (outline) to ❤️ (filled) when liked
- Add animation when liked
- Handle plural correctly ("1 like" vs "2 likes")

**💡 Hint:** `button.disabled = true` prevents further clicking!

---

## Task 9: Keypress Detector

**Goal:** Detect and display keyboard input.

### Instructions:
1. Create a file called `key-detector.html`
2. Listen for keyboard events
3. Display which key was pressed

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Key Detector</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: white;
        }
        #keyDisplay {
            background-color: white;
            color: #333;
            font-size: 120px;
            font-weight: bold;
            padding: 60px;
            border-radius: 20px;
            margin: 30px auto;
            max-width: 400px;
            min-height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        #info {
            font-size: 24px;
            margin-top: 20px;
        }
        #counter {
            font-size: 18px;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <h1>Keyboard Detector</h1>
    <p>Press any key on your keyboard!</p>
    
    <div id="keyDisplay">?</div>
    
    <p id="info">Waiting for keypress...</p>
    <p id="counter">Keys pressed: 0</p>
    
    <script>
        // Select elements
        let keyDisplay = document.getElementById('keyDisplay');
        let info = document.getElementById('info');
        let counter = document.getElementById('counter');
        
        // Initialize counter
        let keysPressed = 0;
        
        // Listen for keypress events on the entire document
        document.addEventListener('keypress', function(event) {
            // Get the key that was pressed
            let key = event.key;
            
            // Display the key in large text
            keyDisplay.textContent = key;
            
            // Update the info text
            info.textContent = `You pressed: "${key}"`;
            
            // Increment and display counter
            keysPressed++;
            counter.textContent = `Keys pressed: ${keysPressed}`;
            
            // Log to console
            console.log('Key pressed:', key);
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Press "a" → Large "a" appears, shows "You pressed: a"
- Press "5" → Large "5" appears, shows "You pressed: 5"
- Counter increases with each keypress

### Bonus Challenges:
- Change display color for letters vs numbers
- Show the key code as well
- Add a "Clear" button to reset the display
- Keep a history of the last 5 keys pressed

**💡 Hint:** The `event` object contains information about what happened. `event.key` tells you which key!

---

## Task 10: Live Character Counter

**Goal:** Count characters as user types (like Twitter).

### Instructions:
1. Create a file called `char-counter.html`
2. Count characters in real-time as user types
3. Change color when approaching limit

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Character Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #e8f5e9;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        textarea {
            width: 100%;
            height: 150px;
            padding: 15px;
            font-size: 16px;
            border: 2px solid #4caf50;
            border-radius: 8px;
            resize: vertical;
            font-family: Arial, sans-serif;
            box-sizing: border-box;
        }
        #charCount {
            margin-top: 10px;
            font-size: 18px;
            font-weight: bold;
            color: #4caf50;
        }
        .over-limit {
            color: #f44336 !important;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Tweet Composer</h1>
        <p>What's on your mind?</p>
        
        <textarea id="textInput" placeholder="Start typing..."></textarea>
        
        <div id="charCount">Characters: 0 / 280</div>
    </div>
    
    <script>
        // Select elements
        let textInput = document.getElementById('textInput');
        let charCount = document.getElementById('charCount');
        
        // Set the maximum character limit
        let maxChars = 280;
        
        // Listen for input events (fires every time user types)
        textInput.addEventListener('input', function() {
            // Get the current text length
            let currentLength = textInput.value.length;
            
            // Update the counter display
            charCount.textContent = `Characters: ${currentLength} / ${maxChars}`;
            
            // Change color to red if over limit
            if (currentLength > maxChars) {
                charCount.classList.add('over-limit');
            } else {
                charCount.classList.remove('over-limit');
            }
            
            console.log('Current character count:', currentLength);
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Type "Hello" → Shows "Characters: 5 / 280"
- Keep typing → Counter updates with every character
- Go over 280 characters → Counter turns red

### Bonus Challenges:
- Show remaining characters instead of total (280 - current)
- Disable a "Post" button when over limit
- Show a warning at 260 characters
- Add a progress bar showing how full it is

**💡 Key Concept:** The `input` event fires every single time the input value changes, perfect for live updates!

---

## Challenge Task: Todo List

**Goal:** Create an interactive todo list.

### Instructions:
1. Create a file called `todo-list.html`
2. Add new todos dynamically
3. Keep track of total todos

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Todo List</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
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
        h1 {
            color: #2196f3;
            text-align: center;
        }
        .input-section {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        #todoInput {
            flex: 1;
            padding: 12px;
            font-size: 16px;
            border: 2px solid #2196f3;
            border-radius: 5px;
        }
        #addBtn {
            padding: 12px 30px;
            font-size: 16px;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #addBtn:hover {
            background-color: #45a049;
        }
        .todo-item {
            padding: 15px;
            margin: 10px 0;
            background-color: #e3f2fd;
            border-left: 4px solid #2196f3;
            border-radius: 4px;
        }
        #todoCount {
            text-align: center;
            margin-top: 20px;
            font-weight: bold;
            color: #666;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>My Todo List</h1>
        
        <div class="input-section">
            <input type="text" id="todoInput" placeholder="Enter a new todo...">
            <button id="addBtn">Add</button>
        </div>
        
        <div id="todoDisplay">
            <!-- Todos will appear here -->
        </div>
        
        <div id="todoCount">Total todos: 0</div>
    </div>
    
    <script>
        // Initialize todo counter
        let todoCount = 0;
        
        // Select elements
        let todoInput = document.getElementById('todoInput');
        let addBtn = document.getElementById('addBtn');
        let todoDisplay = document.getElementById('todoDisplay');
        let todoCountDisplay = document.getElementById('todoCount');
        
        // Add click event to add button
        addBtn.addEventListener('click', function() {
            // Get the input value
            let todoText = todoInput.value;
            
            // Check if input is not empty
            if (todoText !== '') {
                // Increment counter
                todoCount++;
                
                // Create a new paragraph for the todo
                let todoPara = document.createElement('p');
                todoPara.classList.add('todo-item');
                todoPara.textContent = todoText;
                
                // Add it to the display
                todoDisplay.appendChild(todoPara);
                
                // Update the counter display
                todoCountDisplay.textContent = `Total todos: ${todoCount}`;
                
                // Clear the input
                todoInput.value = '';
                
                console.log('Todo added:', todoText);
            }
        });
        
        // Bonus: Also add todo when Enter key is pressed
        todoInput.addEventListener('keypress', function(event) {
            if (event.key === 'Enter') {
                addBtn.click(); // Trigger the button click
            }
        });
    </script>
</body>
</html>
```

### Expected Behavior:
- Type "Buy groceries" and click Add
- Todo appears in the list
- Counter shows "Total todos: 1"
- Input clears automatically
- Pressing Enter also adds the todo

### Bonus Challenges:
- Add a "Clear All" button to remove all todos
- Add a "Done" button next to each todo
- Prevent adding empty todos (already included!)
- Add timestamps to each todo
- Make todos deletable with a delete button

**💡 New Concept:** `document.createElement()` creates new HTML elements with JavaScript!

---

## Challenge Task 2: Temperature Converter

**Goal:** Convert between Celsius and Fahrenheit interactively.

### Instructions:
1. Create a file called `temp-converter.html`
2. Convert temperatures based on button clicks
3. Use the conversion formulas

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background: linear-gradient(to right, #74ebd5, #ACB6E5);
            min-height: 100vh;
        }
        .converter {
            background-color: white;
            max-width: 500px;
            margin: 0 auto;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
        }
        input {
            width: 200px;
            padding: 15px;
            font-size: 24px;
            text-align: center;
            border: 2px solid #4caf50;
            border-radius: 8px;
            margin: 20px 0;
        }
        button {
            padding: 12px 30px;
            font-size: 16px;
            margin: 10px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            color: white;
            font-weight: bold;
        }
        #toCelsius {
            background-color: #2196f3;
        }
        #toFahrenheit {
            background-color: #f44336;
        }
        #result {
            margin-top: 30px;
            font-size: 32px;
            font-weight: bold;
            color: #333;
            min-height: 50px;
        }
    </style>
</head>
<body>
    <div class="converter">
        <h1>🌡️ Temperature Converter</h1>
        <p>Enter a temperature:</p>
        
        <input type="number" id="tempInput" placeholder="0">
        
        <div>
            <button id="toFahrenheit">Convert to °F</button>
            <button id="toCelsius">Convert to °C</button>
        </div>
        
        <div id="result"></div>
    </div>
    
    <script>
        // Select elements
        let tempInput = document.getElementById('tempInput');
        let toFahrenheitBtn = document.getElementById('toFahrenheit');
        let toCelsiusBtn = document.getElementById('toCelsius');
        let result = document.getElementById('result');
        
        // Convert Celsius to Fahrenheit
        toFahrenheitBtn.addEventListener('click', function() {
            // Get the Celsius value
            let celsius = Number(tempInput.value);
            
            // Convert: F = (C × 9/5) + 32
            let fahrenheit = (celsius * 9/5) + 32;
            
            // Round to 1 decimal place
            fahrenheit = fahrenheit.toFixed(1);
            
            // Display result
            result.textContent = `${celsius}°C = ${fahrenheit}°F`;
            
            console.log(`${celsius}°C = ${fahrenheit}°F`);
        });
        
        // Convert Fahrenheit to Celsius
        toCelsiusBtn.addEventListener('click', function() {
            // Get the Fahrenheit value
            let fahrenheit = Number(tempInput.value);
            
            // Convert: C = (F - 32) × 5/9
            // Add your calculation here...
            
            // Round to 1 decimal place
            // Add your code here...
            
            // Display result
            // Add your code here...
        });
    </script>
</body>
</html>
```

### Formulas:
- Celsius to Fahrenheit: `F = (C × 9/5) + 32`
- Fahrenheit to Celsius: `C = (F - 32) × 5/9`

### Expected Behavior:
- Enter 0, click "Convert to °F" → Shows "0°C = 32.0°F"
- Enter 32, click "Convert to °C" → Shows "32°F = 0.0°C"
- Enter 100, click "Convert to °F" → Shows "100°C = 212.0°F"

### Bonus Challenges:
- Add labels to show what type of temperature was entered
- Color code hot (red) vs cold (blue) temperatures
- Add Kelvin conversions
- Show all three scales at once

**💡 Hint:** Complete the Fahrenheit to Celsius conversion following the same pattern as the Celsius to Fahrenheit!

---

## Challenge Task 3: Quiz App

**Goal:** Create a simple one-question quiz.

### Instructions:
1. Create a file called `quiz-app.html`
2. Display a question with answer options
3. Check if the answer is correct
4. Show feedback

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Quiz App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
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
            color: #2c3e50;
            text-align: center;
        }
        .question {
            font-size: 20px;
            margin: 30px 0;
            color: #34495e;
        }
        .option {
            padding: 15px;
            margin: 10px 0;
            background-color: #ecf0f1;
            border: 2px solid #bdc3c7;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s;
        }
        .option:hover {
            background-color: #d5dbdb;
            transform: translateX(5px);
        }
        #feedback {
            margin-top: 30px;
            padding: 20px;
            border-radius: 8px;
            font-size: 18px;
            font-weight: bold;
            text-align: center;
            display: none;
        }
        .correct {
            background-color: #d4edda;
            color: #155724;
            border: 2px solid #c3e6cb;
        }
        .incorrect {
            background-color: #f8d7da;
            color: #721c24;
            border: 2px solid #f5c6cb;
        }
        #score {
            text-align: center;
            font-size: 18px;
            margin-top: 20px;
            color: #7f8c8d;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <h1>🎯 Quick Quiz</h1>
        
        <div class="question">
            What does HTML stand for?
        </div>
        
        <div class="option" id="option1">
            Hyper Text Markup Language
        </div>
        <div class="option" id="option2">
            Hot Mail Language
        </div>
        <div class="option" id="option3">
            How To Make Lasagna
        </div>
        
        <div id="feedback"></div>
        
        <div id="score">Score: 0</div>
    </div>
    
    <script>
        // Initialize score
        let score = 0;
        
        // Select elements
        let option1 = document.getElementById('option1');
        let option2 = document.getElementById('option2');
        let option3 = document.getElementById('option3');
        let feedback = document.getElementById('feedback');
        let scoreDisplay = document.getElementById('score');
        
        // Option 1 - CORRECT ANSWER
        option1.addEventListener('click', function() {
            // Show correct feedback
            feedback.textContent = '✅ Correct! Well done!';
            feedback.className = 'correct';
            feedback.style.display = 'block';
            
            // Increase score
            score++;
            scoreDisplay.textContent = `Score: ${score}`;
        });
        
        // Option 2 - WRONG ANSWER
        option2.addEventListener('click', function() {
            feedback.textContent = '❌ Wrong! The correct answer is Hyper Text Markup Language.';
            feedback.className = 'incorrect';
            feedback.style.display = 'block';
        });
        
        // Option 3 - WRONG ANSWER
        // Add your event listener here...
        // Use the same pattern as option2
    </script>
</body>
</html>
```

### Expected Behavior:
- Click correct answer → Green feedback, score increases
- Click wrong answer → Red feedback, shows correct answer
- Score tracks correct answers

### Bonus Challenges:
- Add multiple questions with a "Next" button
- Disable options after answering
- Add a timer
- Show final score at the end
- Add a "Try Again" button

**💡 Hint:** Complete option3's event listener following the same pattern as option2!

---

## Tips for Success

1. **Select elements first** - Always get your elements before adding listeners
   ```javascript
   let button = document.getElementById('myBtn');
   button.addEventListener('click', function() {
       // Code here
   });
   ```

2. **Console.log everything** - Check that your events are firing
   ```javascript
   button.addEventListener('click', function() {
       console.log('Button was clicked!');
   });
   ```

3. **One event at a time** - Add and test each event separately

4. **Use meaningful IDs** - `submitBtn` is better than `btn1`

5. **Test user interactions** - Try clicking, typing, hovering multiple times

6. **Remember .value for inputs**
   ```javascript
   let text = input.value; // Get input text
   input.value = ''; // Clear input
   ```

## Common Mistakes to Avoid

❌ **Adding event listener before element exists**
```html
<script>
    let button = document.getElementById('btn'); // Element doesn't exist yet!
</script>
<button id="btn">Click</button>
```
✅ **Put script at end of body**
```html
<button id="btn">Click</button>
<script>
    let button = document.getElementById('btn'); // Now it exists!
</script>
```

❌ **Forgetting to use .value for inputs**
```javascript
let text = input; // Gets the element, not the text!
```
✅ **Use .value**
```javascript
let text = input.value; // Gets the text
```

❌ **Not updating both variables AND display**
```javascript
count++;
// Forgot to update the display!
```
✅ **Update both**
```javascript
count++;
display.textContent = count;
```

❌ **Misspelling event names**
```javascript
button.addEventListener('clik', ...); // Wrong!
button.addEventListener('mousEnter', ...); // Wrong!
```
✅ **Correct spelling**
```javascript
button.addEventListener('click', ...); // Correct
button.addEventListener('mouseenter', ...); // Correct
```

---

## Event Types Quick Reference

```javascript
// Click events
element.addEventListener('click', function() { });

// Mouse events
element.addEventListener('mouseenter', function() { });
element.addEventListener('mouseleave', function() { });
element.addEventListener('mouseover', function() { });

// Keyboard events
document.addEventListener('keypress', function(event) {
    console.log(event.key); // Which key was pressed
});

// Input events (for text fields)
input.addEventListener('input', function() {
    console.log(input.value); // Current text
});

// Form events
button.addEventListener('submit', function(event) {
    event.preventDefault(); // Stop form from submitting
});
```

## Common Event Properties

```javascript
element.addEventListener('click', function(event) {
    event.key          // Which keyboard key (for keypress events)
    event.target       // Which element triggered the event
    event.preventDefault()  // Stop default behavior
});
```