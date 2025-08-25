# Lesson 15: Loops and Repetition
**Duration:** 90 minutes (A/B Block) | **Week:** 7

## Learning Targets

### I am learning to...
1. **Understand** how loops enable programs to efficiently repeat actions and process collections of data
2. **Create** programs using for-loops for counting repetition and while-loops for condition-based repetition
3. **Apply** loop concepts to automate repetitive tasks and create interactive programs that continue until completion

### Success Criteria - I can...
1. **Write** for-loops that repeat actions a specific number of times with proper loop structure
2. **Design** while-loops that continue based on changing conditions and user input
3. **Build** programs that combine loops with variables, functions, and conditional logic effectively

## AP Big Ideas Connections

### Primary Focus
- **AAP-2.K:** For loops, the variable controlling the loop must be initialized, checked, and updated within the loop
- **AAP-2.L:** Iteration statements can be combined with conditional statements
- **AAP-2.M:** Loops can be used to iterate through each element of a list

### Supporting Connections
- **AAP-2.B:** Represent a step-by-step algorithmic process using sequential, conditional, and iterative statements
- **AAP-1.D:** Evaluate expressions that use arithmetic operations in loops

## Materials Needed
- Computers with track-specific development environments
- Loop reference guides and syntax cards for both tracks
- Repetitive task scenarios for practice exercises
- Loop debugging worksheets and common error examples

## Lesson Structure (90 minutes)

### Opening: Repetition Powers Automation (10 minutes)
**"Why Do the Same Thing Over and Over When Loops Can Do It for You?"**

#### Real-World Repetition Examples (5 minutes)
**Class Discussion - Identifying Repetitive Patterns:**

**Manufacturing Example:**
- Assembly line: same process, different products
- Quality control: check every item with same criteria
- Packaging: repeat folding/sealing process for each box

**Daily Life Examples:**
- Morning routine: same steps every day
- Exercise: repeat movements for sets and reps
- Studying: review flashcards until all are mastered

**Digital Examples:**
- Music playlist: play each song in sequence
- Photo slideshow: display each image for set time
- Email notifications: check for new messages every few minutes

#### Programming Loops Introduction (5 minutes)
**Teacher Explanation:**
- **For-Loop:** Repeat something a specific number of times ("do this 10 times")
- **While-Loop:** Keep repeating while a condition is true ("keep going until finished")
- **Loop Benefits:** Eliminate repetitive code, process large amounts of data, create interactive experiences

### I Do: Loops in Action (25 minutes)
**Live Programming Demonstration**

*Students observe parallel track demonstrations*

#### Visual Programming Track: Automated Animation System (25 minutes)

**Building Repetitive Programs in Scratch:**

**Basic For-Loop Demo (8 minutes):**
```
Create variable [counter] for this sprite only

When flag clicked:
  Set [counter] to [1]
  Repeat (10):
    Say (join "This is repetition number " [counter]) for 1 seconds
    Change [counter] by (1)
    Move (20) steps
    Wait (0.5) seconds
  Say "All done with the loop!" for 2 seconds
```

**Interactive While-Loop Demo (8 minutes):**
```
Create variables [keepGoing], [userResponse]
Set [keepGoing] to [true]

When flag clicked:
  Repeat until (not (keepGoing)):
    Ask "Do you want to see a fun animation? (yes/no)" and wait
    Set [userResponse] to (answer)
    
    If ((userResponse) = "yes") then
      Repeat (5):
        Turn clockwise (72) degrees
        Change color effect by (20)
        Wait (0.3) seconds
      Say "That was fun! Want to see another?" for 2 seconds
    Else
      Set [keepGoing] to [false]
      Say "Thanks for watching my animations!" for 3 seconds
```

**Complex Loop with Data Processing Demo (9 minutes):**
```
Create variables [numbers], [total], [average], [count]
Create list [testScores]

When flag clicked:
  Delete all of [testScores]
  Add [85] to [testScores]
  Add [92] to [testScores]  
  Add [78] to [testScores]
  Add [96] to [testScores]
  Add [88] to [testScores]
  
  Set [total] to [0]
  Set [count] to [1]
  
  Repeat (length of [testScores]):
    Set [numbers] to (item (count) of [testScores])
    Say (join "Processing score " (join [count] (join ": " [numbers]))) for 1 seconds
    Change [total] by (numbers)
    Change [count] by (1)
  
  Set [average] to ((total) / (length of [testScores]))
  Say (join "Total of all scores: " [total]) for 2 seconds
  Say (join "Average score: " [average]) for 3 seconds
  
  If ((average) > [90]) then
    Say "Excellent class performance!" for 2 seconds
  Else
    Say "Good work, room for improvement!" for 2 seconds
```

#### Game Development Track: Automated Game Systems (25 minutes)

**Building Repetitive Game Logic in Godot:**

**Basic For-Loop Demo (8 minutes):**
```gdscript
extends Node2D

func _ready():
    demonstrate_counting_loop()
    demonstrate_position_loop()

func demonstrate_counting_loop():
    print("=== COUNTING DEMONSTRATION ===")
    
    for i in range(10):
        print("This is repetition number " + str(i + 1))
        await get_tree().create_timer(0.5).timeout
    
    print("All done with the counting loop!")
    print("")

func demonstrate_position_loop():
    print("=== POSITION MOVEMENT DEMO ===") 
    
    for step in range(5):
        position.x += 50  # Move 50 pixels right
        print("Moved to position: " + str(position))
        await get_tree().create_timer(0.3).timeout
    
    print("Movement sequence complete!")
    print("")
```

**Interactive While-Loop Demo (8 minutes):**
```gdscript
var game_running: bool = true
var user_wants_to_continue: bool = true

func demonstrate_while_loop():
    print("=== INTERACTIVE GAME LOOP ===")
    
    while game_running and user_wants_to_continue:
        print("Running game cycle...")
        await simulate_game_round()
        
        # Simulate user decision (in real game, this would be actual input)
        var continue_playing = randi() % 2 == 0  # Random true/false
        
        if continue_playing:
            print("Player wants to continue!")
        else:
            print("Player chose to quit.")
            user_wants_to_continue = false
        
        await get_tree().create_timer(1.0).timeout
    
    print("Game session ended. Thanks for playing!")
    print("")

func simulate_game_round():
    print("  → Playing round...")
    print("  → Calculating score...")
    print("  → Updating display...")
    await get_tree().create_timer(0.5).timeout
```

**Complex Loop with Data Processing Demo (9 minutes):**
```gdscript
var test_scores: Array = [85, 92, 78, 96, 88, 91, 84]
var total_score: int = 0
var average_score: float = 0.0

func process_score_data():
    print("=== SCORE PROCESSING SYSTEM ===")
    print("Processing " + str(test_scores.size()) + " test scores...")
    
    # Process each score with detailed feedback
    for i in range(test_scores.size()):
        var current_score = test_scores[i]
        total_score += current_score
        
        print("Student " + str(i + 1) + ": " + str(current_score) + " points")
        
        if current_score >= 90:
            print("  → Excellent performance!")
        elif current_score >= 80:
            print("  → Good work!")
        else:
            print("  → Needs improvement")
        
        await get_tree().create_timer(0.2).timeout
    
    # Calculate and display results
    average_score = float(total_score) / test_scores.size()
    print("")
    print("=== FINAL RESULTS ===")
    print("Total Points: " + str(total_score))
    print("Average Score: " + str(round(average_score * 100) / 100))
    
    var grade_letter: String
    if average_score >= 90:
        grade_letter = "A"
    elif average_score >= 80:
        grade_letter = "B"  
    elif average_score >= 70:
        grade_letter = "C"
    else:
        grade_letter = "F"
    
    print("Class Grade: " + grade_letter)
    print("")
```

### We Do: Guided Loop Building (30 minutes)
**Collaborative Programming Exercise**

*Students work in pairs within their track*

#### Both Tracks: "Habit Tracker System"
**Building programs that help track and encourage daily habits**

**Planning Phase (5 minutes):**
Students design a habit tracking system:
- Daily check-ins for multiple habits
- Progress tracking over time
- Motivational feedback based on consistency
- Goal achievement celebration

#### Visual Programming Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Basic Habit Counter (8 minutes)**
```
Create variables [habitName], [days], [completedDays], [dayCounter]
Create list [habits]

When flag clicked:
  Delete all of [habits]
  Add "Exercise" to [habits]
  Add "Reading" to [habits]
  Add "Coding Practice" to [habits]
  
  Set [days] to [7]  # Track for one week
  Set [dayCounter] to [1]
  
  Repeat (length of [habits]):
    Set [habitName] to (item (dayCounter) of [habits])
    Say (join "Let's track your " [habitName] " habit!") for 2 seconds
    
    Set [completedDays] to [0]
    Repeat (days):
      Ask (join "Day " (join [dayCounter] (join ": Did you complete " (join [habitName] "? (yes/no)")))) and wait
      If ((answer) = "yes") then
        Change [completedDays] by (1)
    
    Say (join "You completed " (join [habitName] (join " " (join [completedDays] (join "/" [days] " days!"))))) for 3 seconds
    Change [dayCounter] by (1)
```

**Step 2: Progress Analysis Loop (8 minutes)**
```
Create variables [percentage], [feedback], [totalHabits], [habitCounter]

Set [totalHabits] to (length of [habits])
Set [habitCounter] to [1]

Repeat (totalHabits):
  Set [habitName] to (item (habitCounter) of [habits])
  Set [percentage] to (([completedDays] / [days]) * (100))
  
  If ((percentage) = [100]) then
    Set [feedback] to "Perfect! You're building a strong habit!"
  Else
    If ((percentage) > [70]) then
      Set [feedback] to "Great progress! Keep it up!"
    Else
      If ((percentage) > [40]) then
        Set [feedback] to "Good start! Try to be more consistent."
      Else
        Set [feedback] to "Keep trying! Building habits takes time."
  
  Say (join [habitName] (join ": " (join [percentage] (join "% - " [feedback])))) for 4 seconds
  Change [habitCounter] by (1)
```

**Step 3: Interactive Habit Maintenance (9 minutes)**
```
Create variables [keepTracking], [todayComplete], [streakCount]

Set [keepTracking] to [true]
Set [streakCount] to [0]

Repeat until (not (keepTracking)):
  Ask "Ready for today's habit check-in? (yes/quit)" and wait
  
  If ((answer) = "quit") then
    Set [keepTracking] to [false]
    Say "Great job tracking your habits! See you tomorrow!" for 3 seconds
  Else
    Set [todayComplete] to [0]
    Set [habitCounter] to [1]
    
    Repeat (totalHabits):
      Set [habitName] to (item (habitCounter) of [habits])
      Ask (join "Did you complete " (join [habitName] " today? (yes/no)")) and wait
      
      If ((answer) = "yes") then
        Change [todayComplete] by (1)
        Say "Awesome!" for 1 seconds
      Else
        Say "That's okay, try again tomorrow!" for 1 seconds
      
      Change [habitCounter] by (1)
    
    If ((todayComplete) = (totalHabits)) then
      Change [streakCount] by (1)
      Say (join "Perfect day! Streak: " (join [streakCount] " days!")) for 3 seconds
      If ((streakCount) > [7]) then
        Say "🏆 One week streak! You're amazing!" for 2 seconds
    Else
      Set [streakCount] to [0]
      Say "Keep working on consistency!" for 2 seconds
```

#### Game Development Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Basic Habit Counter (8 minutes)**
```gdscript
extends Node2D

var habits: Array = ["Exercise", "Reading", "Coding Practice"]
var tracking_days: int = 7
var completion_data: Dictionary = {}

func _ready():
    initialize_habit_tracking()
    simulate_habit_tracking()
    analyze_habit_progress()

func initialize_habit_tracking():
    print("=== HABIT TRACKER INITIALIZATION ===")
    print("Tracking " + str(habits.size()) + " habits for " + str(tracking_days) + " days")
    
    for habit in habits:
        completion_data[habit] = 0
        print("Added habit: " + habit)
    print("")

func simulate_habit_tracking():
    print("=== HABIT TRACKING SIMULATION ===")
    
    for day in range(1, tracking_days + 1):
        print("--- Day " + str(day) + " ---")
        
        for habit in habits:
            # Simulate completion (random for demo - real version would get user input)
            var completed = randi() % 10 > 2  # 80% chance of completion
            
            if completed:
                completion_data[habit] += 1
                print("✓ " + habit + ": Completed")
            else:
                print("✗ " + habit + ": Missed")
        
        print("")
        await get_tree().create_timer(0.3).timeout
```

**Step 2: Progress Analysis Loop (8 minutes)**
```gdscript
func analyze_habit_progress():
    print("=== HABIT PROGRESS ANALYSIS ===")
    
    var total_possible = habits.size() * tracking_days
    var total_completed = 0
    
    for habit in habits:
        var completed_days = completion_data[habit]
        var percentage = float(completed_days) / tracking_days * 100
        total_completed += completed_days
        
        print("Habit: " + habit)
        print("  Completed: " + str(completed_days) + "/" + str(tracking_days) + " days")
        print("  Success Rate: " + str(round(percentage)) + "%")
        
        var feedback: String
        if percentage == 100:
            feedback = "🏆 Perfect! You're building a strong habit!"
        elif percentage > 70:
            feedback = "🌟 Great progress! Keep it up!"
        elif percentage > 40:
            feedback = "👍 Good start! Try to be more consistent."
        else:
            feedback = "💪 Keep trying! Building habits takes time."
        
        print("  " + feedback)
        print("")
    
    var overall_percentage = float(total_completed) / total_possible * 100
    print("=== OVERALL PERFORMANCE ===")
    print("Total Completion Rate: " + str(round(overall_percentage)) + "%")
    
    if overall_percentage > 80:
        print("🎉 Outstanding habit development!")
    elif overall_percentage > 60:
        print("💫 Solid progress on building habits!")
    else:
        print("🌱 Keep working - habits take time to develop!")
```

**Step 3: Interactive Habit Maintenance (9 minutes)**
```gdscript
var current_streak: int = 0
var longest_streak: int = 0
var keep_tracking: bool = true

func interactive_daily_checkin():
    print("=== DAILY HABIT CHECK-IN SYSTEM ===")
    
    while keep_tracking:
        print("--- Today's Habit Check-In ---")
        var daily_completions = 0
        
        for habit in habits:
            # Simulate user response (real version would get actual input)
            var completed_today = randi() % 2 == 1  # 50% chance
            
            if completed_today:
                daily_completions += 1
                print("✅ " + habit + ": Completed today!")
            else:
                print("⏰ " + habit + ": Try again tomorrow!")
        
        # Update streak tracking
        if daily_completions == habits.size():
            current_streak += 1
            if current_streak > longest_streak:
                longest_streak = current_streak
            print("🔥 Perfect day! Current streak: " + str(current_streak) + " days!")
            
            if current_streak == 7:
                print("🏆 ONE WEEK STREAK! You're building amazing habits!")
            elif current_streak % 30 == 0:
                print("🌟 " + str(current_streak) + " DAY MILESTONE! Incredible dedication!")
        else:
            if current_streak > 0:
                print("Streak ended at " + str(current_streak) + " days. Start again tomorrow!")
            current_streak = 0
            print("💪 Keep working on consistency!")
        
        print("Longest streak: " + str(longest_streak) + " days")
        
        # Simulate decision to continue (real version would get user input)
        var continue_tracking = randi() % 4 > 0  # 75% chance to continue
        if not continue_tracking:
            keep_tracking = false
            print("Great job tracking your habits! See you tomorrow! 👋")
        
        print("")
        await get_tree().create_timer(1.0).timeout
```

### You Do: Personal Loop Project (20 minutes)
**Independent Creative Application**

#### Individual Challenge: "Automation Assistant"
**Create a program that uses loops to automate or track something important to you**

**Project Options:**
1. **Study Session Timer:** Use loops to create focused study periods with breaks
2. **Fitness Challenge Tracker:** Track daily exercise goals and progress over time
3. **Creative Practice Logger:** Monitor daily practice for art, music, writing, or other skills
4. **Goal Achievement Calculator:** Break big goals into daily actions and track completion
5. **Memory Game:** Use loops to create repeating patterns for brain training

**Requirements:**
- **For-Loop:** At least one loop that repeats a specific number of times
- **While-Loop:** At least one loop that continues based on a changing condition
- **Data Processing:** Use loops to work with collections of information
- **User Interaction:** Program responds to user input within loop structures

**Creative Extensions:**
- Combine loops with conditional logic for smart responses
- Use nested loops (loops inside other loops) for complex patterns
- Include progress tracking and motivational feedback
- Add visual or audio elements that change based on loop iterations

**Self-Assessment Questions:**
1. How do loops eliminate repetitive code in my program?
2. When should I use a for-loop versus a while-loop?
3. What would happen if my while-loop condition never became false?
4. How can loops help me process large amounts of data efficiently?

### Wrap-Up: Loop Mastery Check (5 minutes)
**"Loops Are the Engine of Automation"**

#### Concept Reinforcement (3 minutes)
**Quick Class Discussion:**
- "What's the most useful automation you created with loops today?"
- "How do loops make programs more efficient than writing repetitive code?"
- "What's one real-world process you could improve with loop-based automation?"

#### Preview Tomorrow (2 minutes)
**"Next: Lists and Data Collections - Organizing Information Like a Pro"**
- Tomorrow we'll learn how to store and work with collections of related information
- We'll use arrays/lists to organize data and combine them with loops for powerful data processing
- We'll build programs that can handle large amounts of information efficiently

## Differentiation Strategies

### For Students Who Need More Support
- Provide loop structure templates with clear initialization, condition, and update sections
- Start with simple counting loops before progressing to condition-based loops
- Use visual aids to show how loop variables change with each iteration
- Offer pair programming with stronger partners for complex loop logic

### For Advanced Students
- Challenge to create nested loops for complex pattern generation
- Encourage exploration of different loop types and optimization techniques
- Provide opportunities to help classmates debug infinite loop issues
- Offer extension activities with advanced loop applications (sorting algorithms, data analysis)

### For Students With Accessibility Needs
- Ensure screen readers properly announce loop structure and iteration progress
- Provide alternative ways to visualize loop execution and variable changes
- Consider audio cues for loop start, iteration, and completion events
- Offer keyboard shortcuts for creating and testing different types of loops

## Assessment Strategy

### Formative Assessment
**Loop Understanding Check:**
- Observation of student ability to identify when loops are appropriate
- Quality of loop condition design and loop variable management
- Successful completion of guided loop programming exercises

### Program Efficiency Assessment:**
- Working programs that demonstrate appropriate loop usage
- Evidence of understanding when to use for-loops versus while-loops
- Proper loop termination conditions and prevention of infinite loops

## Homework/Extension Activities

### For All Students (Required)
**"Loop Applications in Daily Life":**
- Identify 3 repetitive tasks you do regularly that could be automated with programming
- For each task, determine whether it would need a for-loop or while-loop and explain why
- Write pseudocode (plain English) describing how a program could automate one of these tasks
- Research one real-world example of how loops are used in technology you use every day

### For Students Wanting More Challenge
**"Advanced Loop Techniques":**
- Research and implement nested loops to create interesting patterns or solve complex problems
- Explore loop optimization techniques and when they matter for program performance
- Create a program that uses loops to process data from a file or large dataset
- Study how loops are used in algorithms like sorting and searching

### For Students Needing More Practice
**"Loop Fundamentals Reinforcement":**
- Complete additional loop exercises focusing on proper syntax and structure
- Practice identifying and fixing common loop errors (infinite loops, off-by-one errors)
- Create simple programs that demonstrate the difference between for-loops and while-loops
- Work with study partner to trace through loop execution step by step

## Next Lesson Preview
**"Tomorrow: Lists and Data Collections - Managing Multiple Pieces of Information"**

**What Students Will Learn:**
- How to create and work with arrays/lists that store multiple related values
- Techniques for adding, removing, and modifying elements in data collections
- Combining loops with lists for efficient data processing and analysis
- Real-world applications of data structures in programming and problem-solving

**What Students Will Do:**
- Build programs that collect, organize, and analyze sets of information
- Use loops to process every item in a list automatically
- Create interactive programs that grow and change their data over time
- Practice debugging common issues with list indexing and data management

---

**🔄 Excellent! Your students now understand how to automate repetitive tasks with loops and create efficient, powerful programs. They're ready to learn how to organize and process collections of data! 💻📋**
        