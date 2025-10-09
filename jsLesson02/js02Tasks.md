# Lesson 02 Tasks: Variables and Data Types

---

## Task 1: GUIDED EXAMPLE - Profile Page

**Follow these steps to create a profile page using variables.**

### Step 1: Create the HTML
Create a file called `profile.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Profile</title>
</head>
<body>
    <h1 id="name"></h1>
    <p id="bio"></p>
    <p id="details"></p>
    
    <script>
        // Store profile information in variables
        let firstName = "Alex";
        let lastName = "Johnson";
        let age = 20;
        let city = "Seattle";
        let isStudent = true;
        
        // Display the full name
        document.getElementById('name').textContent = `${firstName} ${lastName}`;
        
        // Display bio
        document.getElementById('bio').textContent = `I am ${age} years old and live in ${city}.`;
        
        // Display student status
        document.getElementById('details').textContent = `Student: ${isStudent}`;
        
        // Also log everything to console
        console.log('Name:', firstName, lastName);
        console.log('Age:', age);
        console.log('City:', city);
        console.log('Is Student:', isStudent);
    </script>
</body>
</html>
```

### Step 2: Test It
1. Open the file in your browser
2. You should see your profile information
3. Open console (F12) to see the logged data

### Step 3: Modify It
Now change the variable values to your own information:
- Change `firstName` to your first name
- Change `lastName` to your last name
- Change the other variables to match your info
- Save and refresh to see your changes

**Checkpoint:** The page should display YOUR information.

---

## Task 2: Data Types Practice

**Goal:** Practice creating variables with different data types.

### Instructions:
1. Create a file called `data-types.html`

2. Create the webpage using the starter code below.

3. Using Javascript, create variables for:
   - Your favorite food (string)
   - Your lucky number (number)
   - Whether you like pizza (boolean)
   - Your dream job (string)
   - Number of siblings you have (number)

4. Log each variable to the console with a label
5. Use `typeof` to check and log the data type of each variable

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Data Types Practice</title>
</head>
<body>
    <h1>Data Types Practice</h1>
    <p>Check the console (F12) to see your output!</p>
    
    <script>
        // Create your variables here
        let favoriteFood = "Pizza";
        let luckyNumber = 7;
        let likesPizza = true;
        let dreamJob = ""; // Fill this in
        let numSiblings = 0; // Fill this in
        
        // Log each variable with a label
        console.log("Favorite food:", favoriteFood);
        console.log("Type:", typeof favoriteFood);
        
        console.log("Lucky number:", luckyNumber);
        console.log("Type:", typeof luckyNumber);
        
        // Add the rest of your console.log statements here
        
    </script>
</body>
</html>
```

### Expected Console Output:
```
Favorite food: Pizza
Type: string
Lucky number: 7
Type: number
Likes pizza: true
Type: boolean
Dream job: Barber
Type: string
Number of siblings: 2
Type: number
```

**Hint:** Use `console.log()` to display each variable, then `console.log(typeof variableName)` for each type.

---

## Task 3: String Concatenation Challenge

**Goal:** Practice joining strings together.

### Instructions:
1. Create a file called `story.html`
2. Create these variables:
   - `character` (a character name)
   - `place` (a location)
   - `item` (an object)
   - `action` (a verb like "ran", "jumped", "found")

3. Use concatenation (`+`) to create a sentence and display it in an h1 element
4. Use a template literal to create a different sentence and display it in a p element

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Story Builder</title>
</head>
<body>
    <h1 id="sentence1"></h1>
    <p id="sentence2"></p>
    
    <script>
        // Create your variables here
        let character = "Luna";
        let place = "forest";
        let item = "key";
        let action = "discovered";
        
        // Use + to concatenate (join strings together)
        let firstSentence = character + " went to the " + place + ".";
        document.getElementById('sentence1').textContent = firstSentence;
        
        // Use template literals with ${}
        let secondSentence = `She ${action} a magical ${item}!`;
        document.getElementById('sentence2').textContent = secondSentence;
    </script>
</body>
</html>
```

### Example Output:
If your variables are:
- character = "Luna"
- place = "forest"
- item = "key"
- action = "discovered"

Your output will be:
- "Luna went to the forest."
- "She discovered a magical key!"

**Success Criteria:**
- At least one sentence uses `+` concatenation
- At least one sentence uses template literals with `${}`
- Both sentences appear on the page

**💡 Challenge:** Try changing the variables to create your own unique story!

---

## Task 4: Personal Info Display

**Goal:** Create a formatted information display.

### Instructions:
1. Create a file called `info-card.html`
2. Create variables for:
   - Full name
   - Email address
   - Phone number
   - City
   - Favorite hobby

3. Use JavaScript to populate each paragraph with formatted information

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Info Card</title>
</head>
<body>
    <h1>Personal Information</h1>
    
    <!-- These paragraph elements will be filled by JavaScript -->
    <p id="name"></p>
    <p id="email"></p>
    <p id="phone"></p>
    <p id="location"></p>
    <p id="hobby"></p>
    
    <script>
        // Create your variables here
        let fullName = "Your Name Here";
        let emailAddress = "your.email@example.com";
        let phoneNumber = "555-0123";
        let city = "Your City";
        let favoriteHobby = "Your Hobby";
        
        // Use template literals to format and display
        document.getElementById('name').textContent = `Name: ${fullName}`;
        document.getElementById('email').textContent = `Email: ${emailAddress}`;
        
        // Complete the rest here...
        
    </script>
</body>
</html>
```

### Expected Output Format:
```
Name: [Your Name]
Email: [Your Email]
Phone: [Your Phone]
Location: [Your City]
Hobby: [Your Hobby]
```

**💡 Hint:** Use template literals to create formatted strings like `Name: ${fullName}`

---

## Task 5: Variable Reassignment

**Goal:** Understand how `let` variables can change.

### Instructions:
1. Create a file called `counter.html`
2. Create a variable called `score` and set it to 0
3. Create three h2 elements with ids
4. Display the initial score on the page
5. Log the score to console
6. Add 10 to the score
7. Display the updated score
8. Log the updated score to console
9. Add 5 more to the score
10. Display and log the final score

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Variable Reassignment</title>
</head>
<body>
    <h1>Score Tracker</h1>
    
    <h2 id="initial"></h2>
    <h2 id="updated"></h2>
    <h2 id="final"></h2>
    
    <script>
        // Step 1: Create score variable
        let score = 0;
        
        // Step 2: Display and log initial score
        document.getElementById("initial").textContent = "Initial score: " + score;
        console.log("Score:", score);
        
        // Step 3: Add 10 to score
        score += 10;  // This means score = score + 10
        
        // Step 4: Display and log updated score
        // Your code here...
        
        // Step 5: Add 5 more to score
        // Your code here...
        
        // Step 6: Display and log final score
        // Your code here...
    </script>
</body>
</html>
```

### Expected Page Display:
```
Initial score: 0
Updated score: 10
Final score: 15
```

### Expected Console:
```
Score: 0
Score: 10
Score: 15
```

**Hint:** Use `score += 10` as shorthand for `score = score + 10`

**Full Answer:** The complete code is at the end of this document if you get stuck!

---

## Task 6: Const vs Let

**Goal:** Understand the difference between `const` and `let`.

### Instructions:
1. Create a file called `constants.html`
2. Create these variables:
   - Use `const` for: `birthYear`, `hometown`, `schoolName`
   - Use `let` for: `currentYear`, `age`, `grade`

3. Try to change a `const` variable
4. Look at the error in the console
5. Comment out that line
6. Change the `let` variables and display them

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Const vs Let</title>
</head>
<body>
    <h1>Understanding Const and Let</h1>
    <div id="output"></div>
    
    <script>
        // Use const for values that won't change
        const birthYear = 2005;  // Your birth year never changes
        const hometown = "Springfield";  // Where you were born doesn't change
        const schoolName = "Central High";
        
        // Use let for values that will change
        let currentYear = 2025;  // The year keeps changing
        let age = 20;  // Your age changes every year
        let grade = 10;  // Your grade changes
        
        // Try to change a const - this will cause an ERROR!
        // birthYear = 2006;  // Uncomment this line to see the error
        
        // Changing let variables is fine
        age = 21;
        grade = 11;
        
        // Display the information
        let info = `
            Birth Year: ${birthYear} (const - cannot change)<br>
            Hometown: ${hometown} (const - cannot change)<br>
            Current Age: ${age} (let - can change)<br>
            Current Grade: ${grade} (let - can change)
        `;
        
        document.getElementById('output').innerHTML = info;
        
        console.log("Birth Year:", birthYear);
        console.log("Age:", age);
    </script>
</body>
</html>
```

### Challenge:
Write comments explaining why you used `const` for some variables and `let` for others.

**Rule of Thumb:** Use `const` by default. Only use `let` if you know the value will change later.

---

## Task 7: Debug the Variables

**Goal:** Find and fix variable errors.

### Instructions:
1. Create a file called `debug-variables.html`
2. Copy this code (it has errors!):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Debug Practice</title>
</head>
<body>
    <h1 id="output"></h1>
    
    <script>
        // Fix the errors in this code!
        let first name = "Emma";
        let age = "25;
        const favoriteColor = "blue";
        let 2ndPlace = "silver";
        
        favoriteColor = "red";
        
        let message = `${firstName} is ${age} years old`;
        document.getElementById('output').textContent = message;
        
        console.log(message);
    </script>
</body>
</html>
```

3. Find and fix ALL errors
4. Code should run without any console errors

### Errors to Find (5 total):
- ❌ Variable naming error (spaces not allowed)
- ❌ String quote error (mismatched quotes)
- ❌ Const reassignment error (can't change const)
- ❌ Variable naming error (can't start with number)
- ❌ Undefined variable error (typo in variable name)

**Debugging Tips:**
1. Look at the console errors - they tell you the line number!
2. Check that variable names have no spaces
3. Make sure quotes match at the beginning and end
4. Remember: `const` variables cannot be changed
5. Variable names cannot start with numbers

**Success:** Page displays "Emma is 25 years old" with no console errors.

---

## Challenge Task: Mad Lib Generator

**Goal:** Create a Mad Lib story using variables.

### Instructions:
1. Create `madlib.html`
2. Create at least 8 variables for different types of words
3. Create a silly story using all the variables
4. Display the story on the page with proper formatting
5. Add styling to make it look nice

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mad Lib Story</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f0f8ff;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .story {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            line-height: 1.6;
        }
    </style>
</head>
<body>
    <h1>My Mad Lib Story</h1>
    <div class="story" id="storyOutput"></div>
    
    <script>
        // CHANGE THESE variables to make them your own
        const adjective = "sparkly";
        const noun = "banana";
        const verb = "danced";
        const place = "the moon";
        const animal = "penguin";
        const number = 42;
        const color = "purple";
        const personName = "Bob";
        
        // Create your OWN NEW story using template literals.  Example: 
        let story = `
            <p>Once upon a time, ${personName} went to ${place} and saw a 
            ${color} ${animal}.</p>
            
            <p>The ${animal} ${verb} over to a ${adjective} ${noun} and 
            counted to ${number}.</p>
            
            <p>It was very ${adjective}!</p>
        `;
        
        // Display the story
        document.getElementById('storyOutput').innerHTML = story;
        
        // Also log to console
        console.log("Story:", story);
    </script>
</body>
</html>
```

### Your Turn:
1. Change all the variable values to create YOUR own story
2. Add more variables if you want
3. Make your story longer and funnier!
4. Try using both `const` and `let` where appropriate

### Bonus Challenges:
- ✨ Add more paragraphs to your story
- ✨ Use both concatenation (`+`) and template literals (`${}`)
- ✨ Add more CSS styling
- ✨ Create a title variable for your story
- ✨ Add an image or emoji

### Grading Yourself:
- ✅ At least 8 different variables
- ✅ Story makes sense (even if silly!)
- ✅ All variables are displayed on the page
- ✅ No errors in console
- ✅ Used proper variable naming conventions (camelCase)
- ✅ Story is formatted nicely

---

## Tips for Success
1. **Check your spelling** - Variable names must match exactly
2. **Match your quotes** - Don't mix `'` and `"`
3. **Use descriptive names** - `userName` is better than `x`
4. **Test frequently** - Check the console after each change
5. **Use const by default** - Only use let if the value will change
6. **Save often** - Save your file before refreshing the browser

## Common Mistakes to Avoid

❌ `let first name = "John";` - No spaces in variable names  
✅ `let firstName = "John";`

❌ `let age = "25;` - Mismatched quotes  
✅ `let age = "25";`

❌ `let 1stPlace = "gold";` - Can't start with a number  
✅ `let firstPlace = "gold";`

❌ `const age = 20; age = 21;` - Can't change const  
✅ `let age = 20; age = 21;`

---

## Full Answer for Task 5:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Variable Reassignment</title>
</head>
<body>
    <h1>Task 5: Variable Reassignment</h1>

    <!-- Display areas -->
    <h2 id="initial"></h2>
    <h2 id="updated"></h2>
    <h2 id="final"></h2>

    <script>
        // Step 1: Create a variable called score and set it to 0
        let score = 0;

        // Step 2: Display the initial score and log to console
        document.getElementById("initial").textContent = "Initial score: " + score;
        console.log("Score:", score);

        // Step 3: Add 10 to the score
        score += 10;

        // Step 4: Display the updated score and log to console
        document.getElementById("updated").textContent = "Updated score: " + score;
        console.log("Score:", score);

        // Step 5: Add 5 more to the score
        score += 5;

        // Step 6: Display the final score and log to console
        document.getElementById("final").textContent = "Final score: " + score;
        console.log("Score:", score);
    </script>
</body>
</html>
```