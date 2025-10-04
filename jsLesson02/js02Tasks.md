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

**✅ Checkpoint:** The page should display YOUR information.

---

## Task 2: Data Types Practice

**Goal:** Practice creating variables with different data types.

### Instructions:
1. Create a file called `data-types.html`
2. Create variables for:
   - Your favorite food (string)
   - Your lucky number (number)
   - Whether you like pizza (boolean)
   - Your dream job (string)
   - Number of siblings you have (number)

3. Log each variable to the console with a label
4. Use `typeof` to check and log the data type of each variable

### Expected Console Output:
```
Favorite food: Pizza
Type: string
Lucky number: 7
Type: number
Likes pizza: true
Type: boolean
...
```

**💡 Hint:** Use console.log() for each variable, then console.log(typeof variableName) for each type.

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

### Example:
If your variables are:
- character = "Luna"
- place = "forest"
- item = "key"
- action = "discovered"

Your output might be:
- "Luna went to the forest."
- "She discovered a magical key!"

**✅ Success Criteria:**
- At least one sentence uses `+` concatenation
- At least one sentence uses template literals with `${}`
- Both sentences appear on the page

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

3. Create an HTML structure with 5 paragraph elements (each with an id)
4. Use JavaScript to populate each paragraph with formatted information

### Format:
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
3. Create an h2 element with id "score"
4. Display the initial score on the page
5. Log the score to console
6. Add 10 to the score
7. Display the updated score
8. Log the updated score to console
9. Add 5 more to the score
10. Display and log the final score

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

**💡 Hint:** You'll need three different elements on the page to show all three scores.

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

### Challenge:
Write comments explaining why you used `const` for some variables and `let` for others.

**💡 Hint:** Use `const` for things that won't change (like where you were born) and `let` for things that will change (like your current grade).

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

### Errors to Find:
- Variable naming errors
- String quote errors
- Const reassignment errors
- Undefined variable errors

**✅ Success:** Page displays the message correctly with no console errors.

---

## Challenge Task: Mad Lib Generator

**Goal:** Create a Mad Lib story using variables.

### Instructions:
1. Create `madlib.html`
2. Create at least 8 variables for different types of words:
   - An adjective
   - A noun
   - A verb (past tense)
   - A place
   - An animal
   - A number
   - A color
   - A person's name

3. Create a silly story using all the variables
4. Display the story on the page with proper formatting
5. Add styling to make it look nice (use CSS in a `<style>` tag)

### Example Story Template:
"Once upon a time, [name] went to [place] and saw a [color] [animal]. The [animal] [verb] over to a [noun] and counted to [number]. It was very [adjective]!"

### Bonus Challenges:
- Create multiple paragraphs for your story
- Use both concatenation and template literals
- Add a title to your story
- Log the full story to the console as well
- Make some variables `const` and others `let` (think about which should be which)

### Grading Yourself:
- ✅ At least 8 different variables
- ✅ Story makes sense (even if silly!)
- ✅ All variables are displayed on the page
- ✅ No errors in console
- ✅ Used proper variable naming conventions
- ✅ Story is formatted nicely

---

## Tips for Success
1. **Check your spelling** - Variable names must match exactly
2. **Match your quotes** - Don't mix ' and "
3. **Use descriptive names** - `userName` is better than `x`
4. **Test frequently** - Check the console after each change
5. **Use const by default** - Only use let if the value will change

## Common Mistakes to Avoid
❌ `let first name = "John";` - No spaces in names
✅ `let firstName = "John";`

❌ `let age = "25;` - Mismatched quotes
✅ `let age = "25";`

❌ Changing a const variable