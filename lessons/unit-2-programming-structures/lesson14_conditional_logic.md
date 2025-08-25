# Lesson 14: Conditional Logic and Decision Making
**Duration:** 90 minutes (A/B Block) | **Week:** 7

## Learning Targets

### I am learning to...
1. **Understand** how conditional statements enable programs to make decisions and respond adaptively
2. **Create** programs that use if-statements, else-statements, and complex boolean logic
3. **Apply** decision-making concepts to build interactive programs that respond intelligently to user input

### Success Criteria - I can...
1. **Write** conditional statements that control program flow based on different conditions
2. **Use** comparison operators and boolean logic to create sophisticated decision-making systems
3. **Build** a program that demonstrates multiple types of conditional logic working together

## AP Big Ideas Connections

### Primary Focus
- **AAP-2.B:** Represent a step-by-step algorithmic process using sequential, conditional, and iterative statements
- **AAP-2.F:** Express an algorithm that uses selection without using a programming language
- **AAP-2.G:** Express an algorithm that uses iteration without using a programming language

### Supporting Connections
- **AAP-1.D:** Evaluate expressions that use relational and logical operators
- **CRD-2.B:** Explain how a program or code segment functions

## Materials Needed
- Computers with track-specific development environments
- Conditional logic reference sheets for both tracks
- Decision tree templates and flowchart materials
- Real-world decision-making scenario examples

## Lesson Structure (90 minutes)

### Opening: Decisions Everywhere (10 minutes)
**"How Do Programs Make Smart Choices?"**

#### Real-World Decision Examples (5 minutes)
**Class Discussion - Decision Making in Daily Life:**

**Traffic Light System:**
- If light is green → go
- If light is yellow → slow down
- If light is red → stop

**Weather App Logic:**
- If temperature > 80°F → recommend shorts
- If temperature < 40°F → recommend coat
- If raining → recommend umbrella

**Gaming Examples:**
- If health < 20% → show warning
- If score > high score → save new record
- If player level > 10 → unlock new abilities

#### Programming Conditionals Introduction (5 minutes)
**Teacher Explanation:**
- **Conditional Statements:** Code that only runs when certain conditions are true
- **Boolean Logic:** True/false decisions that control program behavior
- **Comparison Operators:** Tools for comparing values (>, <, =, !=)
- **Complex Logic:** Combining multiple conditions with AND, OR, NOT

### I Do: Conditional Logic in Action (25 minutes)
**Live Programming Demonstration**

*Students observe parallel track demonstrations*

#### Visual Programming Track: Smart Response System (25 minutes)

**Building Intelligent Programs in Scratch:**

**Basic If-Statement Demo (8 minutes):**
```
Create variables: [temperature], [weatherAdvice]

When flag clicked:
  Ask "What's the temperature outside?" and wait
  Set [temperature] to (answer)
  
  If ((temperature) > [75]) then
    Set [weatherAdvice] to "Perfect weather for outdoor fun!"
    Say [weatherAdvice] for 3 seconds
    Change color effect by 25
  
  If ((temperature) < [40]) then  
    Set [weatherAdvice] to "Bundle up! It's cold outside!"
    Say [weatherAdvice] for 3 seconds
    Change color effect by -25
```

**If-Else Logic Demo (8 minutes):**
```
Create variables: [userAge], [movieRecommendation]

When flag clicked:
  Ask "How old are you?" and wait
  Set [userAge] to (answer)
  
  If ((userAge) < [13]) then
    Set [movieRecommendation] to "G-rated family movies are perfect for you!"
  Else
    If ((userAge) < [17]) then
      Set [movieRecommendation] to "You can enjoy PG-13 movies!"
    Else
      Set [movieRecommendation] to "All movies are available to you!"
  
  Say [movieRecommendation] for 4 seconds
```

**Complex Boolean Logic Demo (9 minutes):**
```
Create variables: [mathScore], [scienceScore], [englishScore], [gpa], [honor]

When flag clicked:
  Ask "Enter your Math score (0-100):" and wait
  Set [mathScore] to (answer)
  
  Ask "Enter your Science score (0-100):" and wait  
  Set [scienceScore] to (answer)
  
  Ask "Enter your English score (0-100):" and wait
  Set [englishScore] to (answer)
  
  Set [gpa] to (((mathScore) + (scienceScore) + (englishScore)) / (3))
  
  If (((mathScore) > [90]) and ((scienceScore) > [90]) and ((englishScore) > [90])) then
    Set [honor] to "Perfect! You made High Honor Roll!"
    Say [honor] for 3 seconds
    Play sound "applause"
  Else
    If ((gpa) > [85]) then
      Set [honor] to "Great job! You made Honor Roll!"
      Say [honor] for 3 seconds
      Play sound "cheer"
    Else
      If ((gpa) > [70]) then
        Set [honor] to "Good work! Keep improving!"
        Say [honor] for 3 seconds
      Else
        Set [honor] to "You can do better! Let's make a study plan."
        Say [honor] for 3 seconds

  Say (join "Your GPA is " [gpa]) for 2 seconds
```

#### Game Development Track: Adaptive Game System (25 minutes)

**Building Smart Game Logic in Godot:**

**Basic Conditional Demo (8 minutes):**
```gdscript
extends Node2D

var player_health: int = 85
var game_message: String = ""

func _ready():
    check_player_status()
    display_health_advice()

func check_player_status():
    print("=== PLAYER STATUS CHECK ===")
    print("Current Health: " + str(player_health) + "%")
    
    if player_health > 75:
        game_message = "You're in great shape! Keep exploring!"
        print("✓ Status: Excellent condition")
    
    if player_health < 25:
        game_message = "Warning! Find health items immediately!"
        print("⚠️ Status: Critical - seek healing!")
    
    print("Advice: " + game_message)
    print("")
```

**If-Else Chain Demo (8 minutes):**
```gdscript
var player_level: int = 12
var recommended_area: String = ""

func determine_play_area():
    print("=== AREA RECOMMENDATION SYSTEM ===")
    print("Player Level: " + str(player_level))
    
    if player_level < 5:
        recommended_area = "Training Grounds"
        print("Recommendation: Start with basic training")
    elif player_level < 15:
        recommended_area = "Forest Adventures" 
        print("Recommendation: Explore the mystical forest")
    elif player_level < 25:
        recommended_area = "Mountain Challenges"
        print("Recommendation: Take on mountain quests")
    else:
        recommended_area = "Dragon's Lair"
        print("Recommendation: Face the ultimate challenge!")
    
    print("Suggested Area: " + recommended_area)
    print("")
```

**Complex Boolean Logic Demo (9 minutes):**
```gdscript
var math_score: int = 92
var science_score: int = 88
var english_score: int = 95
var gpa: float = 0.0
var achievement_level: String = ""

func calculate_academic_achievement():
    print("=== ACADEMIC ACHIEVEMENT CALCULATOR ===")
    print("Math Score: " + str(math_score))
    print("Science Score: " + str(science_score))  
    print("English Score: " + str(english_score))
    
    gpa = float(math_score + science_score + english_score) / 3.0
    print("Calculated GPA: " + str(round(gpa * 100) / 100))
    
    # Complex conditional logic with multiple criteria
    if math_score > 90 and science_score > 90 and english_score > 90:
        achievement_level = "High Honor Roll - Perfect Excellence!"
        print("🏆 Achievement: " + achievement_level)
        print("Outstanding performance across all subjects!")
    elif (math_score > 85 and science_score > 85 and english_score > 85) or gpa > 87:
        achievement_level = "Honor Roll - Excellent Work!"
        print("🥇 Achievement: " + achievement_level)
        print("Strong performance with consistent excellence!")
    elif gpa > 75 and (math_score > 80 or science_score > 80 or english_score > 80):
        achievement_level = "Good Standing - Keep Improving!"
        print("👍 Achievement: " + achievement_level)
        print("Solid foundation with room for growth!")
    else:
        achievement_level = "Needs Improvement - Let's Make a Plan!"
        print("💪 Achievement: " + achievement_level)
        print("Focus on study strategies and ask for help!")
    
    print("")
```

### We Do: Guided Decision Tree Building (30 minutes)
**Collaborative Programming Exercise**

*Students work in pairs within their track*

#### Both Tracks: "Smart Study Planner" Program
**Building an adaptive system that gives personalized study recommendations**

**Planning Phase (5 minutes):**
Students design decision logic for study planning:
- Available study time (< 1 hour, 1-3 hours, > 3 hours)
- Subject difficulty (easy, medium, hard)
- Current understanding (struggling, okay, confident)
- Test date proximity (tomorrow, this week, next week)

#### Visual Programming Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Basic Time-Based Decisions (8 minutes)**
```
Create variables: [studyTime], [studyPlan], [priority]

When flag clicked:
  Ask "How much time do you have to study? (hours)" and wait
  Set [studyTime] to (answer)
  
  If ((studyTime) < [1]) then
    Set [studyPlan] to "Quick review: flashcards and key concepts"
    Set [priority] to "high"
  Else
    If ((studyTime) < [3]) then
      Set [studyPlan] to "Focused session: practice problems and notes review"
      Set [priority] to "medium"
    Else
      Set [studyPlan] to "Deep dive: complete practice, create summaries, teach concepts"
      Set [priority] to "comprehensive"
  
  Say (join "Recommended plan: " [studyPlan]) for 4 seconds
```

**Step 2: Subject and Difficulty Logic (8 minutes)**
```
Create variables: [subject], [difficulty], [studyMethod]

Ask "What subject are you studying?" and wait
Set [subject] to (answer)

Ask "How difficult is this subject for you? (easy/medium/hard)" and wait  
Set [difficulty] to (answer)

If ((difficulty) = "easy") then
  If ((studyTime) > [2]) then
    Set [studyMethod] to "Review quickly, then help others or explore advanced topics"
  Else
    Set [studyMethod] to "Light review and confidence building"
Else
  If ((difficulty) = "hard") then
    If ((studyTime) > [2]) then
      Set [studyMethod] to "Break into small chunks, frequent breaks, ask for help"
    Else
      Set [studyMethod] to "Focus on most important concepts, skip advanced topics"
  Else
    Set [studyMethod] to "Balanced approach: review, practice, and self-test"

Say (join "For " (join [subject] (join " (" (join [difficulty] "): " [studyMethod])))) for 4 seconds
```

**Step 3: Complex Multi-Factor Decision System (9 minutes)**
```
Create variables: [testDate], [confidence], [finalRecommendation]

Ask "When is your test? (tomorrow/this week/next week)" and wait
Set [testDate] to (answer)

Ask "How confident do you feel? (struggling/okay/confident)" and wait
Set [confidence] to (answer)

If ((testDate) = "tomorrow") then
  If ((confidence) = "struggling") then
    Set [finalRecommendation] to "URGENT: Focus only on most important concepts, get help immediately"
  Else
    If ((confidence) = "confident") then
      Set [finalRecommendation] to "Light review and get good sleep - you're ready!"
    Else
      Set [finalRecommendation] to "Quick but thorough review of all key concepts"
Else
  If ((testDate) = "this week") then
    If ((confidence) = "struggling") then
      Set [finalRecommendation] to "Daily study sessions with help from teacher or tutor"
    Else
      Set [finalRecommendation] to "Steady practice and review - you have time to improve"
  Else
    If ((confidence) = "struggling") then
      Set [finalRecommendation] to "Start with basics and build up - you have time!"
    Else
      Set [finalRecommendation] to "Maintain current knowledge and gradually deepen understanding"

Say "📚 PERSONALIZED STUDY PLAN:" for 2 seconds
Say [finalRecommendation] for 5 seconds
```

#### Game Development Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Basic Time-Based Decisions (8 minutes)**
```gdscript
extends Node2D

var study_time: float = 0.0
var study_plan: String = ""
var priority: String = ""

func _ready():
    get_study_time()
    create_time_based_plan()
    display_recommendations()

func get_study_time():
    # Simulated user input - will improve with actual input later
    study_time = 2.5  # hours available
    print("=== STUDY TIME ASSESSMENT ===")
    print("Available study time: " + str(study_time) + " hours")

func create_time_based_plan():
    if study_time < 1.0:
        study_plan = "Quick review: flashcards and key concepts"
        priority = "high-intensity"
        print("Plan Type: Quick Review Session")
    elif study_time < 3.0:
        study_plan = "Focused session: practice problems and notes review" 
        priority = "medium-intensity"
        print("Plan Type: Focused Study Session")
    else:
        study_plan = "Deep dive: complete practice, create summaries, teach concepts"
        priority = "comprehensive"
        print("Plan Type: Comprehensive Study Session")
    
    print("Recommended approach: " + study_plan)
    print("")
```

**Step 2: Subject and Difficulty Logic (8 minutes)**
```gdscript
var subject: String = "Mathematics"
var difficulty: String = "medium"  
var study_method: String = ""

func determine_study_method():
    print("=== SUBJECT-SPECIFIC PLANNING ===")
    print("Subject: " + subject)
    print("Difficulty Level: " + difficulty)
    
    if difficulty == "easy":
        if study_time > 2.0:
            study_method = "Review quickly, then help others or explore advanced topics"
        else:
            study_method = "Light review and confidence building"
    elif difficulty == "hard":
        if study_time > 2.0:
            study_method = "Break into small chunks, frequent breaks, ask for help"
        else:
            study_method = "Focus on most important concepts, skip advanced topics"
    else:  # medium difficulty
        study_method = "Balanced approach: review, practice, and self-test"
    
    print("Recommended method: " + study_method)
    print("")
```

**Step 3: Complex Multi-Factor Decision System (9 minutes)**
```gdscript
var test_date: String = "this week"
var confidence_level: String = "okay"
var final_recommendation: String = ""

func create_personalized_plan():
    print("=== PERSONALIZED STUDY STRATEGY ===")
    print("Test Date: " + test_date)
    print("Confidence Level: " + confidence_level)
    
    if test_date == "tomorrow":
        if confidence_level == "struggling":
            final_recommendation = "🚨 URGENT: Focus only on most important concepts, get help immediately"
        elif confidence_level == "confident":
            final_recommendation = "😌 Light review and get good sleep - you're ready!"
        else:  # okay confidence
            final_recommendation = "📖 Quick but thorough review of all key concepts"
    elif test_date == "this week":
        if confidence_level == "struggling":
            final_recommendation = "📚 Daily study sessions with help from teacher or tutor"
        else:
            final_recommendation = "⚡ Steady practice and review - you have time to improve!"
    else:  # next week
        if confidence_level == "struggling":
            final_recommendation = "🌱 Start with basics and build up - you have time!"
        else:
            final_recommendation = "🎯 Maintain current knowledge and gradually deepen understanding"
    
    print("FINAL RECOMMENDATION:")
    print(final_recommendation)
    print("")

func display_recommendations():
    create_time_based_plan()
    determine_study_method()
    create_personalized_plan()
```

### You Do: Personal Decision System (20 minutes)
**Independent Creative Application**

#### Individual Challenge: "Life Decision Helper"
**Create a program that helps make decisions about something important to you**

**Project Options:**
1. **Course Selection Helper:** Help choose classes based on interests, difficulty, and career goals
2. **Weekend Activity Planner:** Decide what to do based on weather, budget, and mood
3. **College Preparation Tracker:** Recommend actions based on grade level, goals, and current progress
4. **Career Explorer:** Suggest career paths based on interests, strengths, and preferences

**Requirements:**
- **Simple If-Statements:** At least 2 basic conditional checks
- **If-Else Chains:** At least one decision tree with multiple branches
- **Complex Boolean Logic:** At least one condition using AND, OR, or NOT
- **User Interaction:** Program responds to user input with personalized advice

**Self-Assessment Questions:**
1. How do conditional statements make my program more intelligent?
2. What happens when multiple conditions could be true at the same time?
3. How can I test my program to make sure all decision paths work correctly?
4. What real-world decision-making processes could be improved with programming logic?

### Wrap-Up: Decision Logic Mastery Check (5 minutes)
**"Conditional Logic Makes Programs Smart"**

#### Concept Reinforcement (3 minutes)
**Quick Class Discussion:**
- "What's the most useful decision-making feature you created today?"
- "How do boolean operators (AND, OR, NOT) make conditions more powerful?"
- "What kinds of real-world problems could be solved with decision trees?"

#### Preview Tomorrow (2 minutes)
**"Next: Loops and Repetition - Teaching Programs to Repeat Tasks Efficiently"**
- Tomorrow we'll learn how to make programs repeat actions automatically
- We'll use for-loops and while-loops to handle repetitive tasks
- We'll combine loops with today's conditional logic for sophisticated program control

## Differentiation Strategies

### For Students Who Need More Support
- Provide flowchart templates for visualizing conditional logic
- Start with simple true/false conditions before adding complex comparisons
- Use pair programming with stronger logic partners
- Offer step-by-step debugging guides for conditional statement issues

### For Advanced Students
- Challenge to create nested conditional statements with multiple levels
- Encourage exploration of switch/case statements if available in their track
- Provide opportunities to help classmates debug logical errors
- Offer extension activities with complex multi-condition decision systems

### For Students With Accessibility Needs
- Ensure screen readers properly announce conditional statement structure
- Provide alternative ways to visualize decision trees and logic flows
- Consider audio cues for different types of conditional outcomes
- Offer keyboard shortcuts for creating and testing conditional statements

## Assessment Strategy

### Formative Assessment
**Conditional Logic Understanding:**
- Observation of student ability to identify when conditions are needed
- Quality of boolean logic design and comparison operator usage
- Successful completion of guided conditional programming exercises

### Decision System Functionality:**
- Working programs that demonstrate appropriate conditional responses
- Logical decision trees that handle multiple scenarios correctly
- Evidence of understanding how to test and debug conditional logic

## Homework/Extension Activities

### For All Students (Required)
**"Decision Trees in Real Life":**
- Choose one decision you make regularly (what to wear, what to eat, how to spend free time)
- Create a flowchart showing all the factors that influence this decision
- Write pseudocode (plain English) describing the conditional logic you use
- Identify how programming concepts could make this decision-making process more efficient

### For Students Wanting More Challenge
**"Advanced Conditional Systems":**
- Research how artificial intelligence uses conditional logic for decision making
- Create a program with nested conditional statements (if-statements inside other if-statements)
- Design a complex scoring system that uses multiple weighted factors
- Explore how conditional logic applies to your interests (sports statistics, music recommendations, etc.)

### For Students Needing More Practice
**"Conditional Logic Fundamentals":**
- Complete additional if-statement exercises focusing on single conditions
- Practice converting real-world decisions into simple conditional statements
- Work with study partner to test and debug conditional logic programs
- Create truth tables showing when different boolean expressions are true or false

## Next Lesson Preview
**"Tomorrow: Loops and Repetition - Automating Repetitive Tasks Like a Pro"**

**What Students Will Learn:**
- How to use for-loops to repeat actions a specific number of times
- When and how to use while-loops for condition-based repetition
- Combining loops with conditional logic for sophisticated program control
- How loops make programs efficient and eliminate code repetition

**What Students Will Do:**
- Build programs that automate repetitive tasks
- Create interactive programs that keep running until the user chooses to stop
- Combine loops with functions and conditionals for complex program behavior
- Practice debugging infinite loops and off-by-one errors

---

**🤖 Excellent! Your students now understand how to make programs intelligent with conditional logic and decision-making. They're ready to learn how to automate repetitive tasks with loops! 💻🔄**