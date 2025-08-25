# Lesson 13: Functions and Parameters
**Duration:** 90 minutes (A/B Block) | **Week:** 6

## Learning Targets

### I am learning to...
1. **Create** reusable functions to organize code and eliminate repetition
2. **Use** parameters to pass information into functions for flexible programming
3. **Apply** function concepts to break complex problems into manageable pieces

### Success Criteria - I can...
1. **Write** functions that perform specific tasks and can be called multiple times
2. **Design** functions with parameters that work with different input values
3. **Build** a program that uses multiple functions working together to solve a problem

## AP Big Ideas Connections

### Primary Focus
- **AAP-3.A:** For determining the efficiency of an algorithm
- **AAP-3.B:** Explain how the use of procedural abstraction can reduce complexity
- **CRD-2.G:** Describe the purpose of a code segment or program by writing documentation

### Supporting Connections
- **AAP-2.A:** Express an algorithm that uses sequencing, selection, and iteration
- **AAP-1.D:** Evaluate expressions that use arithmetic operators

## Materials Needed
- Computers with track-specific development environments
- Function reference guides for both tracks
- Problem-solving scenarios for function practice
- Code organization examples and templates

## Lesson Structure (90 minutes)

### Opening: The Power of Reusable Code (10 minutes)
**"Why Repeat Yourself When You Can Create Functions?"**

#### Real-World Function Examples (5 minutes)
**Class Discussion - Functions Everywhere:**
Students identify "functions" in real life:

**Kitchen Example:**
- Making a sandwich: same steps, different ingredients
- Recipe: reusable instructions that work with any ingredients
- Tools: can opener works on any can, not just one specific can

**School Example:**
- Morning routine: same steps, different days
- Class schedule: same structure, different subjects
- Login process: same steps, different accounts

#### Programming Functions Introduction (5 minutes)
**Teacher Explanation:**
- **Function:** A reusable block of code that performs a specific task
- **Parameters:** Information we give to functions so they can work with different data
- **Benefits:** Less repetition, easier debugging, better organization

### I Do: Functions in Action (25 minutes)
**Live Programming Demonstration**

*Students observe parallel track demonstrations*

#### Visual Programming Track: Custom Block Creation (25 minutes)

**Building Reusable Blocks in Scratch:**

**Simple Function Demo (8 minutes):**
```
Create custom block "introduce character"
Define "introduce character":
  Say "Hello! I'm a character in this program!" for 2 seconds
  Wait 1 seconds
  Say "I'm excited to meet you!" for 2 seconds

When flag clicked:
  introduce character :: custom
  Wait 3 seconds
  introduce character :: custom
```

**Function with Parameters Demo (8 minutes):**
```
Create custom block "greet person" with input "name"
Define "greet person" [name]:
  Say (join "Hello, " (join [name] "! Welcome to our program!")) for 2 seconds
  Wait 1 seconds
  Say (join "Nice to meet you, " [name]) for 2 seconds

When flag clicked:
  greet person "Sarah" :: custom
  Wait 2 seconds
  greet person "Alex" :: custom
  Wait 2 seconds
  greet person "Maya" :: custom
```

**Complex Function with Multiple Parameters Demo (9 minutes):**
```
Create custom block "create character profile" with inputs "name", "age", "hobby"
Define "create character profile" [name] [age] [hobby]:
  Say (join "Character Name: " [name]) for 2 seconds
  Say (join "Age: " (join [age] " years old")) for 2 seconds  
  Say (join "Favorite Hobby: " [hobby]) for 2 seconds
  Say "Character created successfully!" for 1 seconds

When flag clicked:
  create character profile "Dragon Slayer" "25" "Exploring" :: custom
  Wait 2 seconds
  create character profile "Wise Wizard" "150" "Reading Magic Books" :: custom
  Wait 2 seconds
  create character profile "Swift Archer" "30" "Target Practice" :: custom
```

#### Game Development Track: Function Organization (25 minutes)

**Building Reusable Functions in Godot:**

**Simple Function Demo (8 minutes):**
```gdscript
extends Node2D

func _ready():
    introduce_game()
    wait_and_introduce_again()

func introduce_game():
    print("=== WELCOME TO OUR GAME! ===")
    print("This is an awesome adventure!")
    print("Get ready for fun!")
    print("") # Empty line for spacing

func wait_and_introduce_again():
    await get_tree().create_timer(2.0).timeout
    introduce_game()
    print("Functions make programming so much easier!")
```

**Function with Parameters Demo (8 minutes):**
```gdscript
func greet_player(player_name: String):
    print("=== PLAYER GREETING ===")
    print("Hello, " + player_name + "! Welcome to our game!")
    print("We're excited to have you here, " + player_name + "!")
    print("Let the adventure begin!")
    print("")

func _ready():
    greet_player("Sarah")
    greet_player("Alex") 
    greet_player("Maya")
    print("All players have been welcomed!")
```

**Complex Function with Multiple Parameters Demo (9 minutes):**
```gdscript
func create_character(name: String, level: int, character_class: String, health: int):
    print("=== CHARACTER CREATION ===")
    print("Name: " + name)
    print("Level: " + str(level))
    print("Class: " + character_class)
    print("Health: " + str(health) + " HP")
    
    # Calculate derived stats
    var power = level * 10
    var experience_needed = level * 100
    
    print("Power Rating: " + str(power))
    print("Experience Needed for Next Level: " + str(experience_needed))
    print("Character " + name + " is ready for adventure!")
    print("") # Spacing

func _ready():
    create_character("Dragon Slayer", 25, "Warrior", 250)
    create_character("Wise Wizard", 30, "Mage", 180)
    create_character("Swift Archer", 22, "Ranger", 200)
```

### We Do: Guided Function Building (30 minutes)
**Collaborative Programming Exercise**

*Students work in pairs within their track*

#### Both Tracks: "Personal Assistant Program"
**Building functions that help with daily tasks**

**Planning Phase (5 minutes):**
Students brainstorm functions a personal assistant program might need:
- Calculate study time needed
- Plan daily schedule
- Track goal progress
- Give motivational messages

#### Visual Programming Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Simple Task Functions (8 minutes)**
```
Create custom block "give motivation"
Define "give motivation":
  Say "You've got this! Keep working hard!" for 2 seconds
  Say "Every expert was once a beginner!" for 2 seconds

Create custom block "celebrate success"  
Define "celebrate success":
  Play sound "cheer" ::
  Say "Congratulations! You did amazing work!" for 2 seconds
  Change color effect by 25
```

**Step 2: Functions with Single Parameters (8 minutes)**
```
Create custom block "calculate study time" with input "subject"
Define "calculate study time" [subject]:
  Ask (join "How many hours do you want to study " (join [subject] " today?")) and wait
  Set [studyTime] to (answer)
  Say (join "Great! You'll study " (join [subject] (join " for " (join [studyTime] " hours!")))) for 3 seconds

Create custom block "track goal progress" with input "goal"
Define "track goal progress" [goal]:
  Ask (join "How close are you to achieving your " (join [goal] " goal? (0-100%)")) and wait
  Set [progress] to (answer)
  If ((progress) > [80]) then
    Say (join "Amazing! You're almost done with your " (join [goal] " goal!")) for 3 seconds
  Else
    Say (join "Keep going! You're making progress on your " (join [goal] " goal!")) for 3 seconds
```

**Step 3: Complex Functions with Multiple Parameters (9 minutes)**
```
Create custom block "plan study session" with inputs "subject", "minutes", "difficulty"
Define "plan study session" [subject] [minutes] [difficulty]:
  Say (join "Planning your " [subject] " study session...") for 2 seconds
  
  If ((difficulty) = "easy") then
    Set [breakTime] to ((minutes) / 10)
  Else
    If ((difficulty) = "hard") then
      Set [breakTime] to ((minutes) / 5)
    Else
      Set [breakTime] to ((minutes) / 8)
  
  Say (join "Study " [subject] " for " [minutes] " minutes") for 2 seconds
  Say (join "Take a " [breakTime] " minute break every hour") for 2 seconds
  Say "You're ready to succeed!" for 2 seconds

When flag clicked:
  plan study session "Math" "90" "hard" :: custom
  Wait 3 seconds
  plan study session "History" "60" "easy" :: custom
```

#### Game Development Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Simple Task Functions (8 minutes)**
```gdscript
extends Node2D

func give_motivation():
    print("=== DAILY MOTIVATION ===")
    print("You've got this! Keep working hard!")
    print("Every expert was once a beginner!")
    print("Your future self will thank you for the work you do today!")
    print("")

func celebrate_success():
    print("🎉 === CELEBRATION TIME! === 🎉")
    print("Congratulations! You did amazing work!")
    print("Your hard work is paying off!")
    print("Keep up the fantastic effort!")
    print("")
```

**Step 2: Functions with Single Parameters (8 minutes)**
```gdscript
func calculate_study_time(subject: String):
    print("=== STUDY TIME CALCULATOR ===")
    print("Planning study session for: " + subject)
    
    # Simulated input - will improve with actual input later
    var planned_hours = 2
    var total_minutes = planned_hours * 60
    
    print("Subject: " + subject)
    print("Planned Time: " + str(planned_hours) + " hours")
    print("That's " + str(total_minutes) + " minutes of focused learning!")
    print("")

func track_goal_progress(goal: String):
    print("=== GOAL PROGRESS TRACKER ===")
    print("Tracking progress for: " + goal)
    
    # Simulated progress - will improve with actual input later
    var current_progress = 75
    
    print("Goal: " + goal)
    print("Progress: " + str(current_progress) + "%")
    
    if current_progress > 80:
        print("Amazing! You're almost done with your " + goal + " goal!")
    else:
        print("Keep going! You're making great progress on your " + goal + " goal!")
    print("")
```

**Step 3: Complex Functions with Multiple Parameters (9 minutes)**
```gdscript
func plan_study_session(subject: String, minutes: int, difficulty: String):
    print("=== STUDY SESSION PLANNER ===")
    print("Subject: " + subject)
    print("Duration: " + str(minutes) + " minutes")
    print("Difficulty: " + difficulty)
    
    var break_time: int
    var focus_blocks: int
    
    # Calculate breaks based on difficulty
    if difficulty == "easy":
        break_time = minutes / 10
        focus_blocks = 4
    elif difficulty == "hard":
        break_time = minutes / 5
        focus_blocks = 6
    else: # medium difficulty
        break_time = minutes / 8
        focus_blocks = 5
    
    print("Recommended break time: " + str(break_time) + " minutes per hour")
    print("Suggested focus blocks: " + str(focus_blocks))
    print("You're ready to succeed with " + subject + "!")
    print("")

func _ready():
    give_motivation()
    calculate_study_time("Mathematics")
    track_goal_progress("Learn Programming")
    plan_study_session("Computer Science", 120, "medium")
    celebrate_success()
```

### You Do: Personal Function Library (20 minutes)
**Independent Creative Application**

#### Individual Challenge: "My Programming Toolkit"
**Create a collection of useful functions for personal projects**

**Requirements:**
1. **Simple Function:** A function that performs one clear task (no parameters)
2. **Single Parameter Function:** A function that works with one piece of input information
3. **Multi-Parameter Function:** A function that combines multiple inputs to create useful output
4. **Function Chain:** Use your functions together in a main program

**Creative Function Ideas:**
- **Motivational System:** Functions for encouragement, celebration, goal-setting
- **School Helper:** Functions for calculating grades, planning homework, tracking assignments
- **Creative Generator:** Functions for story ideas, art prompts, music suggestions
- **Life Organizer:** Functions for scheduling, budgeting, habit tracking

**Self-Assessment Questions:**
1. How do functions help organize my code?
2. What makes a good parameter for a function?
3. How can I combine simple functions to create complex programs?
4. What would happen if I tried to use a function without the right parameters?

### Wrap-Up: Function Mastery Check (5 minutes)
**"Functions Are the Building Blocks of Great Programs"**

#### Concept Reinforcement (3 minutes)
**Quick Class Discussion:**
- "What's the most useful function you created today?"
- "How do parameters make functions more powerful?"
- "What big problem could you solve by breaking it into smaller functions?"

#### Preview Tomorrow (2 minutes)
**"Next: Conditional Logic - Teaching Programs to Make Decisions"**
- Tomorrow we'll learn how to make programs that respond differently to different situations
- We'll use if-statements and boolean logic to create adaptive, intelligent programs
- We'll combine today's functions with decision-making to create even more sophisticated programs

## Differentiation Strategies

### For Students Who Need More Support
- Provide function template worksheets with guided structure
- Start with simpler functions before adding parameters
- Pair with partners who can help explain function concepts
- Offer visual diagrams showing how information flows into and out of functions

### For Advanced Students
- Challenge to create functions that call other functions
- Encourage exploration of advanced parameter types and return values
- Provide opportunities to help classmates debug function issues
- Offer extension activities with recursive function concepts

### For Students With Accessibility Needs
- Ensure screen readers properly announce custom blocks and function definitions
- Provide alternative ways to organize and visualize function structure
- Consider keyboard shortcuts for function creation and calling
- Offer audio descriptions of function flow and parameter passing concepts

## Assessment Strategy

### Formative Assessment
**Function Understanding Check:**
- Observation of student ability to identify when functions would be helpful
- Quality of function naming and parameter choices
- Successful completion of guided function creation activities

### Program Organization Assessment:**
- Working programs that demonstrate effective function use
- Appropriate parameter design for flexible function usage
- Evidence of understanding how functions reduce code repetition and improve organization

## Homework/Extension Activities

### For All Students (Required)
**"Functions in Daily Life Analysis":**
- Identify 3 activities you do regularly that could be "functions" (same process, different inputs)
- For each activity, list what the "parameters" (variable inputs) would be
- Design one simple function in your programming track that would be useful for your schoolwork
- Write a brief explanation of how functions make programs better

### For Students Wanting More Challenge
**"Advanced Function Architecture":**
- Research how professional programmers organize code with functions and modules
- Create a function that calls other functions to solve a complex problem
- Explore return values and how functions can send information back to the main program
- Design a function library that other students could use in their projects

### For Students Needing More Practice
**"Function Fundamentals Building":**
- Create additional simple functions focusing on clear, single purposes
- Practice converting repeated code sections into reusable functions
- Work with peer mentor to understand parameter passing and function organization
- Complete guided exercises that demonstrate the benefits of function-based programming

## Next Lesson Preview
**"Tomorrow: Conditional Logic and Decision Making - Smart Programs That Adapt"**

**What Students Will Learn:**
- How to use if-statements to make programs respond to different conditions
- Boolean logic and comparison operations for decision-making
- Combining conditions with AND, OR, and NOT logic
- How conditional logic makes programs intelligent and adaptive

**What Students Will Do:**
- Build programs that make different choices based on user input
- Create decision trees that guide users through complex choices
- Combine today's functions with conditional logic for sophisticated programs
- Practice debugging logical errors and unexpected program behavior

---

**🔧 Excellent! Your students now understand how to organize code into powerful, reusable functions. They're ready to make their programs intelligent with conditional logic and decision-making! 💻⚙️**