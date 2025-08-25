# Student Programming Reference Guide - Unit 2
**Your Complete Guide to Programming Concepts | Visual Programming & Game Development Tracks**

---

## 🎯 How to Use This Guide

This reference guide is your programming companion throughout Unit 2! Whether you're in the Visual Programming track (Scratch & MIT App Inventor) or Game Development track (Godot & GDScript), the concepts are the same—only the tools are different.

**Quick Reference:** Use this guide to look up syntax, troubleshoot problems, and remind yourself of key concepts.

**Learning Support:** Each section includes examples from both tracks so you can see how the same ideas work in different environments.

**Problem Solving:** When you're stuck, start here to understand what you're trying to accomplish before diving into code.

---

## 📊 Variables and Data Types

### What Are Variables?
Variables are like labeled containers that store information your program needs to remember.

### Data Types You Need to Know

#### **Text/String Data**
*For storing words, names, messages*

**Visual Programming (Scratch):**
```
Set [playerName] to "Alex"
Set [favoriteColor] to "blue"
Ask "What's your hobby?" and wait
Set [userHobby] to (answer)
```

**Game Development (GDScript):**
```gdscript
var player_name: String = "Alex"
var favorite_color: String = "blue"
var user_hobby: String = "reading"
```

#### **Number Data**
*For storing counts, scores, measurements*

**Visual Programming (Scratch):**
```
Set [playerScore] to [1500]
Set [health] to [100]
Set [temperature] to [72.5]
```

**Game Development (GDScript):**
```gdscript
var player_score: int = 1500
var health: int = 100
var temperature: float = 72.5
```

#### **Boolean Data (True/False)**
*For storing yes/no, on/off information*

**Visual Programming (Scratch):**
```
Set [gameStarted] to [true]
Set [hasKey] to [false]
```

**Game Development (GDScript):**
```gdscript
var game_started: bool = true
var has_key: bool = false
```

### Variable Naming Tips
- Use descriptive names: `playerScore` not `x`
- Use camelCase: `currentLevel` not `current level`
- No spaces in variable names
- Choose names that explain what the variable stores

---

## ⚙️ Functions and Parameters

### What Are Functions?
Functions are reusable blocks of code that perform specific tasks. Think of them like recipes that you can use over and over with different ingredients.

### Creating Functions

**Visual Programming (Scratch):**
```
Define custom block "greet player" with input "name":
  Say (join "Hello, " [name]) for 2 seconds
  Say "Welcome to the game!" for 2 seconds

# Using the function
greet player "Sarah" :: custom
```

**Game Development (GDScript):**
```gdscript
func greet_player(name: String):
    print("Hello, " + name)
    print("Welcome to the game!")

# Using the function
greet_player("Sarah")
```

### Functions with Multiple Parameters

**Visual Programming (Scratch):**
```
Define custom block "calculate grade" with inputs "points", "totalPoints":
  Set [percentage] to (([points] / [totalPoints]) * 100)
  If ((percentage) > [90]) then
    Say "Excellent work!" for 2 seconds
  Else
    Say (join "You earned " (join [percentage] "%")) for 2 seconds

# Using the function
calculate grade "85" "100" :: custom
```

**Game Development (GDScript):**
```gdscript
func calculate_grade(points: int, total_points: int):
    var percentage = float(points) / total_points * 100
    
    if percentage > 90:
        print("Excellent work!")
    else:
        print("You earned " + str(percentage) + "%")

# Using the function
calculate_grade(85, 100)
```

### Why Use Functions?
- **Avoid repetition:** Write once, use many times
- **Organize code:** Break big problems into smaller pieces
- **Fix bugs easier:** Change code in one place instead of many
- **Make code readable:** Functions with good names explain what your program does

---

## 🤔 Conditional Logic and Decision Making

### What Are Conditionals?
Conditionals let your program make decisions and respond differently to different situations.

### Basic If-Statements

**Visual Programming (Scratch):**
```
If ((score) > [1000]) then
  Say "High score!" for 2 seconds
  Change color effect by 25
```

**Game Development (GDScript):**
```gdscript
if score > 1000:
    print("High score!")
    # Change visual effect
```

### If-Else Statements

**Visual Programming (Scratch):**
```
If ((health) > [50]) then
  Say "You're in good shape!" for 2 seconds
Else
  Say "You need healing!" for 2 seconds
  Change color effect by -25
```

**Game Development (GDScript):**
```gdscript
if health > 50:
    print("You're in good shape!")
else:
    print("You need healing!")
```

### Complex Conditions with AND, OR

**Visual Programming (Scratch):**
```
# AND condition (both must be true)
If (((score) > [500]) and ((lives) > [0])) then
  Say "Keep playing!" for 2 seconds

# OR condition (either can be true)
If (((hasKey) = [true]) or ((hasPassword) = [true])) then
  Say "You can enter!" for 2 seconds
```

**Game Development (GDScript):**
```gdscript
# AND condition
if score > 500 and lives > 0:
    print("Keep playing!")

# OR condition
if has_key or has_password:
    print("You can enter!")
```

### Comparison Operators
- `>` greater than
- `<` less than
- `>=` greater than or equal
- `<=` less than or equal
- `=` equals (Scratch) / `==` equals (GDScript)
- `≠` not equal (Scratch) / `!=` not equal (GDScript)

---

## 🔄 Loops and Repetition

### What Are Loops?
Loops let your program repeat actions automatically without writing the same code over and over.

### For-Loops (Count-Controlled)
*Use when you know how many times to repeat*

**Visual Programming (Scratch):**
```
Repeat (10):
  Move (10) steps
  Turn clockwise (36) degrees
  Wait (0.5) seconds
```

**Game Development (GDScript):**
```gdscript
for i in range(10):
    # Move character
    position.x += 10
    rotation_degrees += 36
    await get_tree().create_timer(0.5).timeout
```

### While-Loops (Condition-Controlled)
*Use when you want to repeat until something changes*

**Visual Programming (Scratch):**
```
Set [keepGoing] to [true]

Repeat until (not (keepGoing)):
  Ask "Continue? (yes/no)" and wait
  If ((answer) = "no") then
    Set [keepGoing] to [false]
  Else
    Say "Let's keep going!" for 1 seconds
```

**Game Development (GDScript):**
```gdscript
var keep_going = true

while keep_going:
    # Simulate user input
    var user_response = get_user_input()
    
    if user_response == "no":
        keep_going = false
    else:
        print("Let's keep going!")
```

### Processing Lists with Loops

**Visual Programming (Scratch):**
```
Create list [students]
Set [studentIndex] to [1]

Repeat (length of [students]):
  Set [currentStudent] to (item (studentIndex) of [students])
  Say (join "Hello, " [currentStudent]) for 1 seconds
  Change [studentIndex] by (1)
```

**Game Development (GDScript):**
```gdscript
var students = ["Alice", "Bob", "Charlie", "Diana"]

for student in students:
    print("Hello, " + student)

# Alternative with index
for i in range(students.size()):
    print("Hello, " + students[i])
```

### Loop Safety Tips
- **Avoid infinite loops:** Make sure your condition will eventually become false
- **Test your conditions:** Check that your loop will stop when expected
- **Use meaningful loop variables:** `i` for counters, descriptive names for data

---

## 📋 Lists and Data Collections

### What Are Lists?
Lists store multiple pieces of related information in an organized way, like a digital filing cabinet.

### Creating and Using Lists

**Visual Programming (Scratch):**
```
Create list [favoriteGames]

# Adding items
Add "Minecraft" to [favoriteGames]
Add "Portal" to [favoriteGames]
Add "Stardew Valley" to [favoriteGames]

# Accessing items (first item is position 1)
Set [firstGame] to (item (1) of [favoriteGames])
Say [firstGame] for 2 seconds

# List length
Set [totalGames] to (length of [favoriteGames])
```

**Game Development (GDScript):**
```gdscript
# Creating list/array
var favorite_games = []

# Adding items
favorite_games.append("Minecraft")
favorite_games.append("Portal")
favorite_games.append("Stardew Valley")

# Accessing items (first item is position 0)
var first_game = favorite_games[0]
print(first_game)

# List length
var total_games = favorite_games.size()
```

### Common List Operations

**Visual Programming (Scratch):**
```
# Insert at specific position
Insert "New Game" at (2) of [favoriteGames]

# Delete item
Delete (1) of [favoriteGames]

# Replace item
Replace item (3) of [favoriteGames] with "Updated Game"

# Check if list contains item
If <[favoriteGames] contains "Minecraft"> then
  Say "Found Minecraft!" for 2 seconds
```

**Game Development (GDScript):**
```gdscript
# Insert at specific position
favorite_games.insert(1, "New Game")

# Remove item
favorite_games.remove_at(0)

# Replace item
favorite_games[2] = "Updated Game"

# Check if list contains item
if "Minecraft" in favorite_games:
    print("Found Minecraft!")
```

### Processing Lists
Always use loops to work with all items in a list:

**Visual Programming (Scratch):**
```
Set [total] to [0]
Set [index] to [1]

Repeat (length of [testScores]):
  Change [total] by (item (index) of [testScores])
  Change [index] by (1)

Set [average] to ([total] / (length of [testScores]))
```

**Game Development (GDScript):**
```gdscript
var test_scores = [85, 92, 78, 96, 88]
var total = 0

for score in test_scores:
    total += score

var average = float(total) / test_scores.size()
```

---

## 🐛 Debugging Tips and Common Mistakes

### General Debugging Strategy
1. **Read error messages carefully** - they usually tell you exactly what's wrong
2. **Check your spelling** - variable names must match exactly
3. **Test small pieces** - don't try to debug a huge program all at once
4. **Use print/say statements** - show what your program is thinking
5. **Ask for help** - explain your problem to someone else

### Common Mistakes and Fixes

#### **Variable Problems**
❌ **Using undefined variables**
```
Say [userName] for 2 seconds  # userName was never created
```
✅ **Fix: Define variables before using**
```
Set [userName] to "Default"
Say [userName] for 2 seconds
```

#### **Logic Problems**
❌ **Confusing assignment and comparison**
```
If ((score) = [100]) then  # This assigns 100 to score!
```
✅ **Fix: Use comparison operator**
```
If ((score) = [100]) then  # In Scratch this is correct
if score == 100:  # In GDScript use ==
```

#### **Loop Problems**
❌ **Infinite loops**
```
Set [count] to [1]
Repeat until ((count) > [10]):
  Say "Counting..." for 1 seconds
  # Forgot to change count!
```
✅ **Fix: Update loop variable**
```
Set [count] to [1]
Repeat until ((count) > [10]):
  Say "Counting..." for 1 seconds
  Change [count] by (1)  # Now it will end!
```

#### **List Problems**
❌ **Wrong list position**
```
# Trying to access position 0 in Scratch (starts at 1)
Set [first] to (item (0) of [myList])  # Error!
```
✅ **Fix: Use correct starting position**
```
# Scratch lists start at position 1
Set [first] to (item (1) of [myList])  # Correct!

# GDScript lists start at position 0
var first = my_list[0]  # Correct!
```

---

## 💡 Problem-Solving Strategies

### When You're Stuck
1. **Break it down:** What is the smallest piece you can work on?
2. **Write it out:** Describe what you want your program to do in plain English
3. **Find examples:** Look for similar problems you've solved before
4. **Ask specific questions:** "Why doesn't this loop stop?" instead of "This doesn't work"

### Planning Your Programs
1. **Define the problem:** What exactly are you trying to solve?
2. **List the steps:** What does your program need to do, in order?
3. **Identify the concepts:** What variables, functions, loops, etc. do you need?
4. **Start simple:** Build a basic version first, then add features
5. **Test frequently:** Make sure each piece works before adding the next

### Getting Help Effectively
- **Show your code:** Let others see what you've tried
- **Explain your goal:** What is the program supposed to do?
- **Describe the problem:** What happens vs. what you expected?
- **Share error messages:** Copy exact error text if there is any

---

## 🎯 Track-Specific Quick References

### Visual Programming Track (Scratch) Essentials
- **Projects save automatically** when you're logged in
- **Share projects** using the Share button (only if appropriate)
- **Remix others' work** to learn new techniques (give credit!)
- **Use costumes and sounds** to make programs engaging
- **Test frequently** by clicking the green flag

### Game Development Track (Godot) Essentials
- **Save your project** regularly (Ctrl+S / Cmd+S)
- **Play your scene** using F6 or the play button
- **Debug with print()** statements to see what's happening
- **Check the debugger** panel for error messages
- **Organize scenes** and scripts with clear names

---

## 📚 Additional Resources

### When You Want to Learn More
- **Scratch Community:** scratch.mit.edu/explore for inspiration
- **Godot Documentation:** docs.godotengine.org for detailed guides
- **Programming Tutorials:** Search for "[concept] tutorial" online
- **Peer Learning:** Work with classmates to share discoveries

### Career Connections
- **Visual Programming:** Used in education, data analysis, app development, workflow automation
- **Game Development:** Used in entertainment, education, simulation, interactive media
- **Both Tracks:** Teach problem-solving skills valuable in any technology career

---

**🚀 Remember: Programming is problem-solving! Every expert programmer started exactly where you are. Focus on understanding concepts, practice regularly, and don't be afraid to experiment and make mistakes—that's how you learn! 💻✨**