# Lesson 16: Lists and Data Collections
**Duration:** 90 minutes (A/B Block) | **Week:** 8

## Learning Targets

### I am learning to...
1. **Understand** how lists and arrays enable programs to store and organize multiple related pieces of information
2. **Create** programs that add, remove, and modify elements in data collections efficiently
3. **Apply** list processing techniques with loops to analyze and manipulate sets of data

### Success Criteria - I can...
1. **Build** lists that store related information and access individual elements by position
2. **Use** loops to process every item in a list and perform calculations or modifications
3. **Design** programs that collect user data into lists and provide meaningful analysis or feedback

## AP Big Ideas Connections

### Primary Focus
- **AAP-1.C:** Represent a list or string using a variable
- **AAP-2.M:** Loops can be used to iterate through each element of a list
- **AAP-2.N:** The exam reference sheet provides basic operations on lists

### Supporting Connections
- **DAT-2.A:** Describe what information can be extracted from data
- **AAP-2.O:** Write expressions to access list elements

## Materials Needed
- Computers with track-specific development environments
- List/array reference guides for both tracks
- Data collection scenarios and sample datasets
- List processing worksheets and debugging exercises

## Lesson Structure (90 minutes)

### Opening: Collections Everywhere (10 minutes)
**"Why Store One Thing When You Can Organize Many?"**

#### Real-World Collection Examples (5 minutes)
**Class Discussion - Identifying Data Collections:**

**School Examples:**
- Class roster: list of student names
- Grade book: collection of test scores for each student
- Schedule: list of class periods and subjects
- Library catalog: organized collection of all books

**Digital Examples:**
- Music playlist: ordered collection of songs
- Photo gallery: collection of images with timestamps
- Shopping cart: list of items with quantities and prices
- Social media feed: chronological collection of posts

**Everyday Examples:**
- Grocery list: items needed from the store
- To-do list: tasks that need completion
- Contact list: phone numbers and names
- Recipe ingredients: measured amounts of different foods

#### Programming Lists Introduction (5 minutes)
**Teacher Explanation:**
- **List/Array:** A container that holds multiple pieces of related information
- **Index:** The position number used to access specific elements (usually starts at 0)
- **Elements:** The individual pieces of information stored in the list
- **Benefits:** Organize related data, process multiple items efficiently, build flexible programs

### I Do: Lists in Action (25 minutes)
**Live Programming Demonstration**

*Students observe parallel track demonstrations*

#### Visual Programming Track: Dynamic Data Management (25 minutes)

**Building List-Based Programs in Scratch:**

**Basic List Creation and Access Demo (8 minutes):**
```
Create list [favoriteColors]
Create variables [colorChoice], [listPosition], [totalColors]

When flag clicked:
  Delete all of [favoriteColors]
  Add "Blue" to [favoriteColors]
  Add "Green" to [favoriteColors]
  Add "Purple" to [favoriteColors]
  Add "Orange" to [favoriteColors]
  
  Set [totalColors] to (length of [favoriteColors])
  Say (join "I have " (join [totalColors] " favorite colors!")) for 2 seconds
  
  Set [listPosition] to [1]
  Repeat (totalColors):
    Set [colorChoice] to (item (listPosition) of [favoriteColors])
    Say (join "Color " (join [listPosition] (join ": " [colorChoice]))) for 2 seconds
    Change [listPosition] by (1)
```

**Interactive List Building Demo (8 minutes):**
```
Create list [studentHobbies]
Create variables [newHobby], [hobbyCount], [keepAsking]

When flag clicked:
  Delete all of [studentHobbies]
  Set [keepAsking] to [true]
  Set [hobbyCount] to [0]
  
  Repeat until (not (keepAsking)):
    Ask "What's one of your hobbies? (or type 'done' to finish)" and wait
    Set [newHobby] to (answer)
    
    If ((newHobby) = "done") then
      Set [keepAsking] to [false]
    Else
      Add [newHobby] to [studentHobbies]
      Change [hobbyCount] by (1)
      Say (join "Added " (join [newHobby] (join "! You have " (join [hobbyCount] " hobbies so far.")))) for 2 seconds
  
  Say "Here are all your hobbies:" for 2 seconds
  Set [listPosition] to [1]
  Repeat (length of [studentHobbies]):
    Set [newHobby] to (item (listPosition) of [studentHobbies])
    Say (join [listPosition] (join ": " [newHobby])) for 2 seconds
    Change [listPosition] by (1)
```

**List Processing and Analysis Demo (9 minutes):**
```
Create list [testScores]
Create variables [score], [total], [average], [highScore], [lowScore], [passingCount]

When flag clicked:
  Delete all of [testScores]
  Add [85] to [testScores]
  Add [92] to [testScores]
  Add [78] to [testScores]
  Add [96] to [testScores]
  Add [88] to [testScores]
  Add [74] to [testScores]
  Add [91] to [testScores]
  
  Set [total] to [0]
  Set [highScore] to [0]
  Set [lowScore] to [100]
  Set [passingCount] to [0]
  Set [listPosition] to [1]
  
  Say "Processing test scores..." for 2 seconds
  
  Repeat (length of [testScores]):
    Set [score] to (item (listPosition) of [testScores])
    Change [total] by (score)
    
    If ((score) > [highScore]) then
      Set [highScore] to (score)
    
    If ((score) < [lowScore]) then
      Set [lowScore] to (score)
    
    If ((score) > [70]) then
      Change [passingCount] by (1)
    
    Change [listPosition] by (1)
  
  Set [average] to ((total) / (length of [testScores]))
  
  Say (join "Class Results: " (join (length of [testScores]) " students")) for 2 seconds
  Say (join "Average Score: " [average]) for 2 seconds
  Say (join "Highest Score: " [highScore]) for 2 seconds
  Say (join "Lowest Score: " [lowScore]) for 2 seconds
  Say (join "Students Passing: " (join [passingCount] (join "/" (length of [testScores])))) for 3 seconds
```

#### Game Development Track: Dynamic Data Systems (25 minutes)

**Building List-Based Game Logic in Godot:**

**Basic Array Creation and Access Demo (8 minutes):**
```gdscript
extends Node2D

var favorite_games: Array = []
var game_genres: Array = ["RPG", "Action", "Strategy", "Puzzle", "Adventure"]

func _ready():
    initialize_game_collections()
    display_collection_info()
    process_each_genre()

func initialize_game_collections():
    print("=== INITIALIZING GAME COLLECTIONS ===")
    
    favorite_games = ["The Legend of Zelda", "Minecraft", "Portal", "Stardew Valley"]
    
    print("Favorite games loaded: " + str(favorite_games.size()) + " games")
    print("Available genres: " + str(game_genres.size()) + " genres")
    print("")

func display_collection_info():
    print("=== FAVORITE GAMES LIST ===")
    
    for i in range(favorite_games.size()):
        var game_name = favorite_games[i]
        print(str(i + 1) + ". " + game_name)
    
    print("")
    print("=== GAME GENRES ===")
    
    for genre in game_genres:
        print("• " + genre)
    
    print("")
```

**Interactive Array Building Demo (8 minutes):**
```gdscript
var player_inventory: Array = []
var inventory_capacity: int = 10

func simulate_inventory_management():
    print("=== INVENTORY MANAGEMENT SYSTEM ===")
    print("Inventory Capacity: " + str(inventory_capacity) + " items")
    
    var items_to_collect = ["Health Potion", "Magic Sword", "Shield", "Gold Coin", "Map"]
    
    for item in items_to_collect:
        if player_inventory.size() < inventory_capacity:
            player_inventory.append(item)
            print("✓ Collected: " + item)
            print("  Inventory: " + str(player_inventory.size()) + "/" + str(inventory_capacity))
        else:
            print("✗ Inventory full! Cannot collect: " + item)
        
        await get_tree().create_timer(0.5).timeout
    
    print("")
    print("=== CURRENT INVENTORY ===")
    
    if player_inventory.is_empty():
        print("Inventory is empty")
    else:
        for i in range(player_inventory.size()):
            print(str(i + 1) + ". " + player_inventory[i])
    
    print("")
```

**Array Processing and Analysis Demo (9 minutes):**
```gdscript
var player_scores: Array = [1250, 2100, 850, 3200, 1800, 950, 2750]
var score_analysis: Dictionary = {}

func analyze_player_performance():
    print("=== PLAYER PERFORMANCE ANALYSIS ===")
    print("Analyzing " + str(player_scores.size()) + " game sessions...")
    
    var total_score: int = 0
    var high_score: int = 0
    var low_score: int = 999999
    var excellent_games: int = 0
    
    # Process each score
    for i in range(player_scores.size()):
        var current_score = player_scores[i]
        total_score += current_score
        
        print("Game " + str(i + 1) + ": " + str(current_score) + " points")
        
        # Track high and low scores
        if current_score > high_score:
            high_score = current_score
            print("  → New high score!")
        
        if current_score < low_score:
            low_score = current_score
        
        # Count excellent performances
        if current_score > 2000:
            excellent_games += 1
            print("  → Excellent performance!")
        
        await get_tree().create_timer(0.3).timeout
    
    # Calculate statistics
    var average_score = float(total_score) / player_scores.size()
    var excellent_percentage = float(excellent_games) / player_scores.size() * 100
    
    print("")
    print("=== PERFORMANCE SUMMARY ===")
    print("Games Played: " + str(player_scores.size()))
    print("Total Score: " + str(total_score))
    print("Average Score: " + str(round(average_score)))
    print("High Score: " + str(high_score))
    print("Low Score: " + str(low_score))
    print("Excellent Games: " + str(excellent_games) + "/" + str(player_scores.size()) + 
          " (" + str(round(excellent_percentage)) + "%)")
    
    # Provide feedback
    if excellent_percentage > 50:
        print("🏆 Outstanding player! Consistently excellent performance!")
    elif average_score > 1500:
        print("🌟 Great player! Above-average skills with room to grow!")
    else:
        print("💪 Keep practicing! Your skills are developing well!")
    
    print("")
```

### We Do: Guided List Building (30 minutes)
**Collaborative Programming Exercise**

*Students work in pairs within their track*

#### Both Tracks: "Class Survey System"
**Building programs that collect, organize, and analyze survey responses**

**Planning Phase (5 minutes):**
Students design a survey system:
- Collect responses from multiple students
- Store all responses in organized lists
- Analyze patterns and provide insights
- Display results in meaningful ways

#### Visual Programming Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Survey Data Collection (8 minutes)**
```
Create list [surveyQuestions]
Create list [responses]
Create variables [currentQuestion], [response], [questionNumber]

When flag clicked:
  Delete all of [surveyQuestions]
  Delete all of [responses]
  
  Add "What's your favorite subject?" to [surveyQuestions]
  Add "How many hours do you study per day?" to [surveyQuestions]
  Add "What's your favorite hobby?" to [surveyQuestions]
  Add "What career interests you most?" to [surveyQuestions]
  
  Say "Welcome to our class survey!" for 2 seconds
  
  Set [questionNumber] to [1]
  Repeat (length of [surveyQuestions]):
    Set [currentQuestion] to (item (questionNumber) of [surveyQuestions])
    Ask [currentQuestion] and wait
    Set [response] to (answer)
    Add [response] to [responses]
    Say "Thank you for your response!" for 1 seconds
    Change [questionNumber] by (1)
  
  Say "Survey complete! Let's see the results..." for 2 seconds
```

**Step 2: Response Display and Organization (8 minutes)**
```
Create variables [responseNumber], [questionIndex], [currentResponse]

Set [questionIndex] to [1]

Repeat (length of [surveyQuestions]):
  Set [currentQuestion] to (item (questionIndex) of [surveyQuestions])
  Set [currentResponse] to (item (questionIndex) of [responses])
  
  Say (join "Q" (join [questionIndex] (join ": " [currentQuestion]))) for 3 seconds
  Say (join "A" (join [questionIndex] (join ": " [currentResponse]))) for 3 seconds
  
  Change [questionIndex] by (1)
  Wait (1) seconds
```

**Step 3: Multi-Student Data Collection (9 minutes)**
```
Create list [allStudentResponses]
Create variables [studentName], [keepSurveying], [studentCount]

Set [keepSurveying] to [true]
Set [studentCount] to [0]

Repeat until (not (keepSurveying)):
  Ask "Student name (or type 'done' to finish):" and wait
  Set [studentName] to (answer)
  
  If ((studentName) = "done") then
    Set [keepSurveying] to [false]
  Else
    Change [studentCount] by (1)
    Say (join "Welcome " (join [studentName] "! Please answer these questions:")) for 2 seconds
    
    Delete all of [responses]
    Set [questionNumber] to [1]
    
    Repeat (length of [surveyQuestions]):
      Set [currentQuestion] to (item (questionNumber) of [surveyQuestions])
      Ask [currentQuestion] and wait
      Add (answer) to [responses]
      Change [questionNumber] by (1)
    
    Add (join [studentName] (join ": " (join (item (1) of [responses]) (join ", " (join (item (2) of [responses]) (join ", " (join (item (3) of [responses]) (join ", " (item (4) of [responses]))))))))) to [allStudentResponses]
    
    Say (join "Thank you " (join [studentName] "! Responses recorded.")) for 2 seconds

Say (join "Survey complete! Collected responses from " (join [studentCount] " students.")) for 3 seconds

Set [responseNumber] to [1]
Repeat (length of [allStudentResponses]):
  Say (join "Student " (join [responseNumber] (join ": " (item (responseNumber) of [allStudentResponses])))) for 4 seconds
  Change [responseNumber] by (1)
```

#### Game Development Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Survey Data Collection System (8 minutes)**
```gdscript
extends Node2D

var survey_questions: Array = [
    "What's your favorite subject?",
    "How many hours do you study per day?", 
    "What's your favorite hobby?",
    "What career interests you most?"
]

var current_responses: Array = []
var all_student_data: Array = []

func _ready():
    print("=== CLASS SURVEY SYSTEM ===")
    simulate_survey_collection()
    display_survey_results()
    analyze_survey_patterns()

func simulate_survey_collection():
    print("Initializing survey with " + str(survey_questions.size()) + " questions...")
    print("")
    
    # Simulate collecting responses from one student
    current_responses.clear()
    
    for i in range(survey_questions.size()):
        print("Question " + str(i + 1) + ": " + survey_questions[i])
        
        # Simulate different types of responses
        var simulated_response: String
        match i:
            0: simulated_response = "Computer Science"
            1: simulated_response = "3 hours"
            2: simulated_response = "Gaming"
            3: simulated_response = "Software Developer"
        
        current_responses.append(simulated_response)
        print("Response: " + simulated_response)
        
        await get_tree().create_timer(0.5).timeout
    
    print("Survey completed for this student!")
    print("")
```

**Step 2: Multi-Student Data Management (8 minutes)**
```gdscript
var student_names: Array = ["Alice", "Bob", "Charlie", "Diana", "Elena"]
var sample_responses: Array = [
    ["Math", "2 hours", "Reading", "Teacher"],
    ["Art", "1 hour", "Drawing", "Artist"], 
    ["Science", "4 hours", "Experiments", "Researcher"],
    ["History", "2.5 hours", "Music", "Historian"],
    ["English", "3 hours", "Writing", "Author"]
]

func collect_multiple_students():
    print("=== COLLECTING DATA FROM MULTIPLE STUDENTS ===")
    
    for i in range(student_names.size()):
        var student_name = student_names[i]
        var responses = sample_responses[i]
        
        print("--- Survey for " + student_name + " ---")
        
        var student_data = {"name": student_name, "responses": []}
        
        for j in range(survey_questions.size()):
            print("Q: " + survey_questions[j])
            print("A: " + responses[j])
            student_data.responses.append(responses[j])
        
        all_student_data.append(student_data)
        print("✓ Data recorded for " + student_name)
        print("")
        
        await get_tree().create_timer(0.3).timeout
    
    print("Survey collection complete! Data from " + str(all_student_data.size()) + " students.")
    print("")
```

**Step 3: Data Analysis and Pattern Recognition (9 minutes)**
```gdscript
func analyze_survey_patterns():
    print("=== SURVEY DATA ANALYSIS ===")
    
    var subject_counts = {}
    var hobby_counts = {}
    var study_hours = []
    
    # Analyze each student's responses
    for student_data in all_student_data:
        var responses = student_data.responses
        var student_name = student_data.name
        
        # Count favorite subjects
        var favorite_subject = responses[0]
        if subject_counts.has(favorite_subject):
            subject_counts[favorite_subject] += 1
        else:
            subject_counts[favorite_subject] = 1
        
        # Extract study hours for numerical analysis
        var hours_text = responses[1]
        var hours_number = extract_number_from_text(hours_text)
        study_hours.append(hours_number)
        
        # Count hobbies
        var hobby = responses[2]
        if hobby_counts.has(hobby):
            hobby_counts[hobby] += 1
        else:
            hobby_counts[hobby] = 1
    
    # Display subject preferences
    print("--- FAVORITE SUBJECTS ---")
    for subject in subject_counts:
        var count = subject_counts[subject]
        print(subject + ": " + str(count) + " students")
    
    # Calculate study time statistics
    print("--- STUDY TIME ANALYSIS ---")
    var total_hours = 0.0
    var max_hours = 0.0
    var min_hours = 999.0
    
    for hours in study_hours:
        total_hours += hours
        if hours > max_hours:
            max_hours = hours
        if hours < min_hours:
            min_hours = hours
    
    var average_hours = total_hours / study_hours.size()
    
    print("Average study time: " + str(round(average_hours * 100) / 100) + " hours")
    print("Maximum study time: " + str(max_hours) + " hours")
    print("Minimum study time: " + str(min_hours) + " hours")
    
    # Display hobby diversity
    print("--- HOBBY DIVERSITY ---")
    for hobby in hobby_counts:
        var count = hobby_counts[hobby]
        print(hobby + ": " + str(count) + " students")
    
    print("Total unique hobbies: " + str(hobby_counts.size()))
    
    # Provide insights
    print("--- INSIGHTS ---")
    if average_hours > 2.5:
        print("📚 This class studies above average!")
    else:
        print("⏰ This class could benefit from more study time.")
    
    if hobby_counts.size() == all_student_data.size():
        print("🎨 Amazing diversity! Every student has a unique hobby!")
    else:
        print("🤝 Some students share common interests!")

func extract_number_from_text(text: String) -> float:
    # Simple number extraction (in real implementation, would be more robust)
    var numbers = ["1", "2", "3", "4", "5"]
    var decimals = ["1.5", "2.5", "3.5", "4.5"]
    
    for num in decimals:
        if text.contains(num):
            return float(num)
    
    for num in numbers:
        if text.contains(num):
            return float(num)
    
    return 2.0  # Default fallback
```

### You Do: Personal Data Project (20 minutes)
**Independent Creative Application**

#### Individual Challenge: "My Data Dashboard"
**Create a program that collects, organizes, and analyzes data about something you care about**

**Project Options:**
1. **Music Library Organizer:** Track favorite songs, artists, genres, and listening patterns
2. **Fitness Progress Tracker:** Collect daily exercise data and analyze improvement trends
3. **Study Habit Analyzer:** Monitor study sessions across different subjects and identify patterns
4. **Creative Project Portfolio:** Organize art, writing, or other creative work with metadata and analysis
5. **Goal Achievement Tracker:** Track progress on multiple personal goals with detailed metrics

**Requirements:**
- **Data Collection:** Use lists to store related information from user input or predefined data
- **Data Processing:** Use loops to analyze all items in your lists
- **Statistical Analysis:** Calculate at least 3 meaningful statistics (average, maximum, count, etc.)
- **Pattern Recognition:** Identify and report interesting patterns or trends in the data
- **User-Friendly Display:** Present results in an organized, easy-to-understand format

**Creative Extensions:**
- Compare data across different categories or time periods
- Provide personalized recommendations based on data analysis
- Include data visualization elements (text-based charts, progress indicators)
- Add data filtering or searching capabilities

**Self-Assessment Questions:**
1. How do lists help me organize and work with multiple pieces of related information?
2. What insights can I discover by processing data with loops that I couldn't see otherwise?
3. How does my program handle edge cases (empty lists, unexpected data)?
4. What questions about my data can my program answer automatically?

### Wrap-Up: Data Collection Mastery Check (5 minutes)
**"Lists Turn Information Into Knowledge"**

#### Concept Reinforcement (3 minutes)
**Quick Class Discussion:**
- "What's the most interesting pattern you discovered in your data?"
- "How do lists combined with loops make data analysis more powerful?"
- "What real-world data collection problems could you solve with programming?"

#### Preview Tomorrow (2 minutes)
**"Next: Foundation Project Checkpoint - Bringing It All Together"**
- Tomorrow we'll combine all the concepts from this foundation phase into a comprehensive project
- We'll use variables, functions, conditionals, loops, and lists working together
- We'll create programs that demonstrate mastery of core programming concepts

## Differentiation Strategies

### For Students Who Need More Support
- Provide list manipulation reference cards with common operations and syntax
- Start with simple, small lists before progressing to complex data processing
- Use visual aids to show how list indices correspond to actual positions
- Offer pair programming with partners who can help explain list concepts

### For Advanced Students
- Challenge to work with multi-dimensional lists or complex data structures
- Encourage exploration of advanced list operations (sorting, filtering, mapping)
- Provide opportunities to help classmates debug list indexing issues
- Offer extension activities with real-world datasets and advanced analysis

### For Students With Accessibility Needs
- Ensure screen readers properly announce list contents and index positions
- Provide alternative ways to visualize list organization and data relationships
- Consider audio cues for list operations like adding, removing, or accessing elements
- Offer keyboard shortcuts for common list manipulation tasks

## Assessment Strategy

### Formative Assessment
**List Understanding Check:**
- Observation of student ability to organize related data into appropriate list structures
- Quality of list processing logic and proper use of indices
- Successful completion of guided list building and analysis exercises

### Data Analysis Skills Assessment:**
- Working programs that demonstrate meaningful data collection and processing
- Evidence of understanding how to combine lists with loops for efficient data analysis
- Appropriate use of statistical calculations and pattern recognition techniques

## Homework/Extension Activities

### For All Students (Required)
**"Data in Your World Analysis":**
- Identify one type of data you encounter regularly (grades, sports stats, music plays, etc.)
- List 5-10 actual data points and organize them by hand
- Calculate basic statistics (average, highest, lowest) manually
- Write a brief plan for how a program with lists could automate this analysis

### For Students Wanting More Challenge
**"Advanced Data Processing":**
- Research real-world applications of data analysis in your areas of interest
- Create a program that works with larger datasets (20+ items) and performs complex analysis
- Explore data import/export concepts and how programs handle data from external sources
- Study how professional data analysis tools organize and process information

### For Students Needing More Practice
**"List Fundamentals Building":**
- Complete additional exercises focusing on basic list creation and element access
- Practice converting related individual variables into organized list structures
- Work with study partner to trace through list processing loops step by step
- Create simple programs that demonstrate adding, removing, and modifying list elements

## Next Lesson Preview
**"Tomorrow: Foundation Project Checkpoint - Integration and Mastery"**

**What Students Will Learn:**
- How to combine variables, functions, conditionals, loops, and lists into comprehensive programs
- Strategies for planning and organizing larger programming projects
- Debugging techniques for complex programs with multiple interacting components
- Professional programming practices for code organization and documentation

**What Students Will Do:**
- Design and build a significant project that demonstrates mastery of all foundation concepts
- Practice systematic problem-solving and project planning skills
- Create programs that solve real-world problems using multiple programming concepts together
- Prepare for the more advanced programming challenges in the development phase

---

**📊 Excellent! Your students now understand how to collect, organize, and analyze data with lists and loops. They're ready to combine all their foundation knowledge into comprehensive programming projects! 💻🗃️**