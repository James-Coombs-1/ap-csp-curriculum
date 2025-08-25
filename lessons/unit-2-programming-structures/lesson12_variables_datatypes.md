# Lesson 12: Variables and Data Types in Context
**Duration:** 90 minutes (A/B Block) | **Week:** 6

## Learning Targets

### I am learning to...
1. **Understand** how different data types (numbers, text, boolean) serve different purposes in programming
2. **Create** and modify variables to store and manipulate information in my programs
3. **Apply** variable concepts to solve real-world problems through interactive programming

### Success Criteria - I can...
1. **Identify** appropriate data types for different kinds of information in my programs
2. **Use** variables to store user input, calculations, and program state effectively
3. **Build** an interactive program that demonstrates multiple data types working together

## AP Big Ideas Connections

### Primary Focus
- **AAP-1.A:** Represent a value with a variable
- **AAP-1.B:** Determine the value of a variable as a result of an assignment
- **AAP-1.C:** Represent a list or string using a variable

### Supporting Connections
- **CRD-2.B:** Explain how a program or code segment functions
- **AAP-2.A:** Express an algorithm that uses sequencing

## Materials Needed
- Computers with track-specific development environments set up
- Variable reference sheets for both tracks
- Real-world data type examples and scenarios
- Debugging practice worksheets

## Lesson Structure (90 minutes)

### Opening: Data All Around Us (10 minutes)
**"What Information Do Programs Need to Remember?"**

#### Real-World Data Investigation (5 minutes)
**Class Discussion - Identifying Data Types:**
Students examine familiar apps and identify different types of information:

**Social Media Example:**
- Username: "Sarah_2024" (text/string)
- Follower count: 847 (number)
- Account verified: true (boolean)
- Posts liked: false/true for each post (boolean)

**Gaming Example:**
- Player name: "DragonSlayer" (text/string)  
- Current score: 15,420 (number)
- Game paused: true (boolean)
- Level completed: false (boolean)

#### Data Type Categories Introduction (5 minutes)
**Teacher Explanation with Examples:**
- **Text/String:** Words, names, messages - information we read and display
- **Numbers:** Scores, counts, measurements - information we calculate with
- **Boolean:** True/false, on/off, yes/no - information about states or conditions

### I Do: Variables in Action (25 minutes)
**Live Programming Demonstration**

*Students observe parallel track demonstrations*

#### Visual Programming Track: Interactive Profile Creator (25 minutes)

**Building a Personal Profile Program in Scratch:**

**Text Variables Demo (8 minutes):**
```
Create variables: [userName], [favoriteColor], [dreamJob]

When flag clicked:
  Ask "What's your name?" and wait
  Set [userName] to (answer)
  
  Ask "What's your favorite color?" and wait  
  Set [favoriteColor] to (answer)
  
  Ask "What's your dream job?" and wait
  Set [dreamJob] to (answer)
  
  Say (join "Hi " (join [userName] "! I love that you want to be a " (join [dreamJob] "!"))) for 3 seconds
```

**Number Variables Demo (8 minutes):**
```
Create variables: [age], [favoriteNumber], [birthYear]

Ask "How old are you?" and wait
Set [age] to (answer)

Ask "What's your favorite number?" and wait
Set [favoriteNumber] to (answer)

Set [birthYear] to ((2025) - (age))
Say (join "You were born in " [birthYear]) for 3 seconds
Say (join "Your favorite number times your age is " ((favoriteNumber) * (age))) for 3 seconds
```

**Boolean Variables Demo (9 minutes):**
```
Create variables: [likesMusic], [playsInstrument], [readyToProgram]

Ask "Do you like music? (yes/no)" and wait
If ((answer) = "yes") then
  Set [likesMusic] to [true]
  Say "Music lovers make great programmers!" for 2 seconds
Else
  Set [likesMusic] to [false]
  Say "That's okay, programming is like making music with code!" for 2 seconds

Set [readyToProgram] to [true]
If (([likesMusic]) = [true]) then
  Say "Since you like music AND you're ready to program, let's make something awesome!" for 3 seconds
```

#### Game Development Track: Player Character System (25 minutes)

**Building a Character Statistics System in Godot:**

**Text Variables Demo (8 minutes):**
```gdscript
extends Node2D

var player_name: String = ""
var character_class: String = ""
var special_ability: String = ""

func _ready():
    # Simulate getting player input
    player_name = "Alex the Brave"
    character_class = "Warrior"
    special_ability = "Lightning Strike"
    
    print("=== CHARACTER PROFILE ===")
    print("Name: " + player_name)
    print("Class: " + character_class)
    print("Special Ability: " + special_ability)
    print("Ready for adventure!")
```

**Number Variables Demo (8 minutes):**
```gdscript
var health_points: int = 100
var experience_level: int = 5
var gold_coins: float = 247.75
var magic_power: int = 80

func calculate_character_stats():
    var total_power = (experience_level * 10) + magic_power
    var health_percentage = (health_points / 100.0) * 100
    
    print("=== CHARACTER STATS ===")
    print("Health: " + str(health_points) + "/100 (" + str(health_percentage) + "%)")
    print("Level: " + str(experience_level))
    print("Gold: $" + str(gold_coins))
    print("Total Power: " + str(total_power))
```

**Boolean Variables Demo (9 minutes):**
```gdscript
var is_alive: bool = true
var has_weapon: bool = true
var quest_completed: bool = false
var can_cast_magic: bool = true

func check_character_status():
    print("=== CHARACTER STATUS ===")
    
    if is_alive:
        print(player_name + " is alive and ready for adventure!")
        
        if has_weapon and can_cast_magic:
            print("Fully equipped with weapon and magic!")
        elif has_weapon:
            print("Armed with weapon, but no magic available.")
        elif can_cast_magic:
            print("Can cast magic, but needs a weapon.")
        else:
            print("Needs both weapon and magic training.")
            
        if quest_completed:
            print("Quest completed! Ready for the next challenge.")
        else:
            print("Current quest still in progress.")
    else:
        print("Character needs healing before continuing.")
```

### We Do: Guided Variable Practice (30 minutes)
**Collaborative Programming Exercise**

*Students work in pairs within their track*

#### Both Tracks: "Dream Vacation Planner" Program

**Planning Phase (5 minutes):**
Students discuss what information a vacation planning program needs:
- Destination name (text)
- Number of days (number)
- Budget amount (number)
- Has passport (boolean)
- Wants adventure activities (boolean)

#### Visual Programming Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Text Data Collection (8 minutes)**
```
Create variables: [destination], [favoriteFood], [travelCompanion]

When flag clicked:
  Ask "Where do you want to travel?" and wait
  Set [destination] to (answer)
  
  Ask "What's your favorite food to try when traveling?" and wait
  Set [favoriteFood] to (answer)
  
  Ask "Who would you travel with?" and wait
  Set [travelCompanion] to (answer)
```

**Step 2: Number Calculations (8 minutes)**
```
Create variables: [days], [budget], [dailyBudget]

Ask "How many days would you travel?" and wait
Set [days] to (answer)

Ask "What's your total budget?" and wait
Set [budget] to (answer)

Set [dailyBudget] to ((budget) / (days))
Say (join "You can spend $" (dailyBudget) " per day!") for 3 seconds
```

**Step 3: Boolean Logic (9 minutes)**
```
Create variables: [hasPassport], [wantsAdventure], [canTravel]

Ask "Do you have a passport? (yes/no)" and wait
If ((answer) = "yes") then
  Set [hasPassport] to [true]
Else
  Set [hasPassport] to [false]

Ask "Do you want adventure activities? (yes/no)" and wait
If ((answer) = "yes") then
  Set [wantsAdventure] to [true]
Else
  Set [wantsAdventure] to [false]

If (([hasPassport]) = [true]) then
  Set [canTravel] to [true]
  If (([wantsAdventure]) = [true]) then
    Say (join "Perfect! You're ready for an adventure in " [destination]) for 3 seconds
  Else
    Say (join "Great! You're ready for a relaxing trip to " [destination]) for 3 seconds
Else
  Say "You'll need to get a passport first, but then you can visit " [destination]) for 3 seconds
```

#### Game Development Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Text Data Setup (8 minutes)**
```gdscript
extends Node2D

var destination: String = ""
var travel_style: String = ""
var accommodation: String = ""

func _ready():
    collect_travel_preferences()
    display_trip_summary()

func collect_travel_preferences():
    # Simulated user input - will improve with actual input later
    destination = "Japan"
    travel_style = "Cultural Explorer"
    accommodation = "Traditional Ryokan"
    
    print("=== TRAVEL PREFERENCES ===")
    print("Destination: " + destination)
    print("Style: " + travel_style)
    print("Accommodation: " + accommodation)
```

**Step 2: Number Calculations (8 minutes)**
```gdscript
var trip_days: int = 14
var total_budget: float = 3500.0
var daily_budget: float = 0.0
var spending_money: float = 0.0

func calculate_budget():
    daily_budget = total_budget / trip_days
    spending_money = daily_budget * 0.6  # 60% for daily expenses
    
    print("=== BUDGET BREAKDOWN ===")
    print("Trip Duration: " + str(trip_days) + " days")
    print("Total Budget: $" + str(total_budget))
    print("Daily Budget: $" + str(daily_budget))
    print("Daily Spending Money: $" + str(spending_money))
```

**Step 3: Boolean Logic (9 minutes)**
```gdscript
var has_passport: bool = true
var wants_adventure: bool = true
var speaks_language: bool = false
var trip_approved: bool = false

func check_travel_readiness():
    print("=== TRAVEL READINESS CHECK ===")
    
    if has_passport:
        print("✓ Passport: Ready")
        trip_approved = true
    else:
        print("✗ Passport: Need to apply")
        trip_approved = false
    
    if wants_adventure and trip_approved:
        print("✓ Adventure Mode: Activated!")
        print("Planning exciting activities for " + destination)
    elif trip_approved:
        print("✓ Relaxation Mode: Activated!")
        print("Planning peaceful experiences in " + destination)
    
    if not speaks_language:
        print("💡 Tip: Consider learning basic " + destination + " phrases!")
```

### You Do: Personal Variable Project (20 minutes)
**Independent Creative Application**

#### Individual Challenge: "About Me Interactive Profile"
**Both tracks create personalized programs using all three data types**

**Requirements:**
1. **Text Variables (minimum 3):** Name, hometown, favorite hobby, future goal
2. **Number Variables (minimum 3):** Age, favorite number, years programming goal
3. **Boolean Variables (minimum 2):** Likes coding, has traveled internationally, wants tech career

**Creative Extensions:**
- Add calculations using number variables
- Use boolean variables to control program flow
- Include personalized responses based on variable combinations
- Add visual or audio elements that reflect personal information

**Self-Assessment Questions:**
1. How do different data types serve different purposes in my program?
2. What calculations can I perform with my number variables?
3. How do boolean variables help control what happens in my program?
4. What would happen if I used the wrong data type for certain information?

### Wrap-Up: Variable Mastery Check (5 minutes)
**"Variables Are the Memory of Programs"**

#### Concept Reinforcement (3 minutes)
**Quick Class Discussion:**
- "What data types did you use and why?"
- "How did variables help your program remember information?"
- "What's one thing you want to improve about using variables?"

#### Preview Tomorrow (2 minutes)
**"Next: Functions - Teaching Your Program New Tricks"**
- Tomorrow we'll learn how to organize code into reusable functions
- Functions will help us avoid repeating code and make programs easier to understand
- We'll build on today's variable knowledge to create more sophisticated programs

## Differentiation Strategies

### For Students Who Need More Support
- Provide variable reference cards with data type examples
- Pair with strong partners for collaborative programming exercises
- Offer simplified versions of practice programs with fewer variables
- Provide extra debugging support for variable naming and usage

### For Advanced Students
- Challenge to use more complex data type combinations
- Encourage exploration of advanced variable operations (string manipulation, complex calculations)
- Provide opportunities to help struggling classmates as peer tutors
- Offer extension activities with arrays/lists preview

### For Students With Accessibility Needs
- Ensure screen readers work well with chosen development environments
- Provide alternative input methods for variable naming and data entry
- Consider visual accommodations for distinguishing different data types
- Offer audio descriptions of visual programming elements when needed

## Assessment Strategy

### Formative Assessment
**Variable Understanding Check:**
- Observation of student discussions about appropriate data types
- Quality of variable naming conventions and organization
- Successful completion of guided practice activities

### Program Functionality Assessment:**
- Working programs that demonstrate all three data types
- Appropriate use of variables for storing and manipulating information
- Creative application of variable concepts to personal programming projects

## Homework/Extension Activities

### For All Students (Required)
**"Variables in Real Life Investigation":**
- Find one mobile app or website you use regularly
- Identify 5 pieces of information it stores (3 different data types)
- Explain why each data type is appropriate for that information
- Sketch a simple program that would use similar variables

### For Students Wanting More Challenge
**"Advanced Variable Operations":**
- Research string manipulation functions in your programming track
- Create a program that performs complex calculations with multiple number variables
- Explore how boolean variables can create more sophisticated program logic
- Begin planning a program that uses variables to track changing information over time

### For Students Needing More Practice
**"Variable Fundamentals Reinforcement":**
- Complete additional variable creation exercises in your development environment
- Practice identifying data types in everyday situations
- Create simple programs focusing on one data type at a time
- Review today's programs and explain how each variable contributes to the program's function

## Next Lesson Preview
**"Tomorrow: Functions and Parameters - Organizing Code Like a Pro"**

**What Students Will Learn:**
- How to create reusable code blocks called functions
- How to pass information to functions using parameters
- Why functions make programs easier to understand and debug
- How to build more complex programs by combining simple functions

**What Students Will Do:**
- Transform repeated code into efficient functions
- Create functions that work with the variables they learned today
- Build a program that demonstrates the power of organized, modular code
- Practice the problem-solving approach of breaking big problems into smaller functions

---

**🎯 Excellent! Your students now understand how programs remember and work with different types of information. They're ready to learn how to organize their code into powerful, reusable functions! 💻📊**