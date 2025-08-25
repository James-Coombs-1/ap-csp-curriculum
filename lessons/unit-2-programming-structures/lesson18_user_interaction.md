# Lesson 18: User Input and Interaction Design
**Duration:** 90 minutes (A/B Block) | **Week:** 9

## Learning Targets

### I am learning to...
1. **Design** intuitive user interfaces that make programs easy and enjoyable to use
2. **Implement** robust input validation and error handling to create reliable programs
3. **Apply** user experience principles to create programs that respond appropriately to diverse user needs

### Success Criteria - I can...
1. **Create** programs with multiple input methods that feel natural and responsive
2. **Build** validation systems that handle unexpected or incorrect user input gracefully
3. **Design** user interfaces that provide clear feedback and guidance for successful interaction

## AP Big Ideas Connections

### Primary Focus
- **CRD-2.F:** Design a program and its user interface
- **CRD-2.I:** For errors in an algorithm or program, explain the benefits of hand tracing, visualizing, and testing
- **AAP-4.A:** For determining the efficiency of an algorithm, use informal reasoning

### Supporting Connections
- **CRD-1.B:** Explain how a computing innovation's purpose influences its functionality
- **IOC-1.C:** Explain how the use of computing can raise legal and ethical concerns

## Materials Needed
- Computers with track-specific development environments
- User interface design examples from popular apps/websites
- Input validation scenarios and edge case examples
- User experience design principles reference guides
- Error handling templates and debugging strategies

## Lesson Structure (90 minutes)

### Opening: User Experience Everywhere (10 minutes)
**"What Makes Some Programs a Joy to Use and Others Frustrating?"**

#### User Experience Investigation (5 minutes)
**Class Discussion - Analyzing Familiar Interfaces:**

**Great User Experiences:**
Students identify apps/websites they love using:
- What makes them easy and enjoyable?
- How do they handle mistakes or confusion?
- What keeps users engaged and coming back?

**Frustrating User Experiences:**
Students share examples of confusing or annoying interfaces:
- What makes them difficult to use?
- How do they respond to user errors?
- What would make them better?

#### User Interface Design Principles (5 minutes)
**Teacher Explanation:**
- **Clarity:** Users should understand what to do immediately
- **Feedback:** Program should respond clearly to user actions
- **Forgiveness:** Mistakes should be easy to fix, not catastrophic
- **Consistency:** Similar actions should work similarly throughout
- **Accessibility:** Programs should work for users with different abilities and preferences

### I Do: Professional User Interface Design (25 minutes)
**Live Programming Demonstration of UX Principles**

*Students observe parallel track demonstrations*

#### Visual Programming Track: Interactive Survey System (25 minutes)

**Building User-Friendly Programs in Scratch:**

**Clear Input and Feedback Demo (8 minutes):**
```
Create variables [userName], [userAge], [validInput], [errorMessage]

Define custom block "get valid name":
  Set [validInput] to [false]
  Repeat until (validInput):
    Ask "Please enter your name (at least 2 letters):" and wait
    Set [userName] to (answer)
    
    If ((length of [userName]) > [1]) then
      If (not <[userName] = []>) then
        Set [validInput] to [true]
        Say (join "Welcome, " (join [userName] "!")) for 2 seconds
      Else
        Say "Please enter your actual name." for 2 seconds
    Else
      Say "Name must be at least 2 letters long." for 2 seconds

When flag clicked:
  get valid name :: custom
```

**Robust Age Validation Demo (8 minutes):**
```
Define custom block "get valid age":
  Set [validInput] to [false]
  Set [errorMessage] to []
  
  Repeat until (validInput):
    Ask "Please enter your age (must be a number between 1 and 120):" and wait
    Set [userAge] to (answer)
    
    If <([userAge] > [0]) and ([userAge] < [121])> then
      Set [validInput] to [true]
      Say (join "Got it! You're " (join [userAge] " years old.")) for 2 seconds
    Else
      If <not <(answer) = [userAge]>> then
        Set [errorMessage] to "Please enter a valid number."
      Else
        If ([userAge] < [1]) then
          Set [errorMessage] to "Age must be at least 1."
        Else
          Set [errorMessage] to "Age must be 120 or less."
      
      Say [errorMessage] for 3 seconds
      Say "Let's try again..." for 1 seconds

get valid age :: custom
```

**Multi-Modal Input Options Demo (9 minutes):**
```
Create variables [inputMethod], [selectedOption], [menuChoice]

Define custom block "choose input method":
  Say "How would you like to interact?" for 2 seconds
  Say "Press SPACE for typing, or click me for menus" for 3 seconds
  
  Set [inputMethod] to []
  Repeat until (not ([inputMethod] = [])):
    If <key [space] pressed?> then
      Set [inputMethod] to "typing"
      Say "Great! We'll use typing." for 2 seconds
    
    If <touching [mouse-pointer]?> then
      Set [inputMethod] to "clicking"
      Say "Perfect! We'll use click menus." for 2 seconds
      Wait until <not <touching [mouse-pointer]?>>

Define custom block "get preference with method" with input "question":
  If ([inputMethod] = "typing") then
    Ask [question] and wait
    Set [selectedOption] to (answer)
  Else
    Say [question] for 2 seconds
    Say "Click me for Option A, press any key for Option B" for 3 seconds
    
    Wait until <<touching [mouse-pointer]?> or <key [any] pressed?>>
    
    If <touching [mouse-pointer]?> then
      Set [selectedOption] to "Option A"
      Say "You chose Option A by clicking!" for 2 seconds
    Else
      Set [selectedOption] to "Option B"
      Say "You chose Option B with the keyboard!" for 2 seconds

When flag clicked:
  choose input method :: custom
  get preference with method "What's your favorite subject: Math or Science?" :: custom
```

#### Game Development Track: Player Input System (25 minutes)

**Building Responsive Game Controls in Godot:**

**Input Validation and Feedback Demo (8 minutes):**
```gdscript
extends Node2D

var player_name: String = ""
var is_valid_input: bool = false
var input_attempts: int = 0

func _ready():
    get_valid_player_name()
    get_valid_difficulty_level()

func get_valid_player_name():
    print("=== PLAYER REGISTRATION SYSTEM ===")
    
    while not is_valid_input:
        print("Please enter your player name (2-20 characters, no special symbols):")
        
        # Simulate user input (in real game, would get actual input)
        var simulated_inputs = ["", "A", "Player123!", "Alex", "SuperLongPlayerNameThatIsTooLong", "Sarah"]
        var test_input = simulated_inputs[input_attempts % simulated_inputs.size()]
        input_attempts += 1
        
        print("Input received: '" + test_input + "'")
        
        if validate_player_name(test_input):
            player_name = test_input
            is_valid_input = true
            print("✅ Welcome, " + player_name + "! Registration successful.")
        else:
            print("❌ Please try again with a valid name.")
        
        await get_tree().create_timer(1.0).timeout

func validate_player_name(input: String) -> bool:
    if input.length() < 2:
        print("   Error: Name must be at least 2 characters long.")
        return false
    
    if input.length() > 20:
        print("   Error: Name must be 20 characters or less.")
        return false
    
    # Check for special characters (simplified)
    var forbidden_chars = ["!", "@", "#", "$", "%", "^", "&", "*"]
    for char in forbidden_chars:
        if char in input:
            print("   Error: Name cannot contain special characters like " + char)
            return false
    
    return true
```

**Multiple Input Methods Demo (8 minutes):**
```gdscript
var input_mode: String = "keyboard"
var movement_speed: float = 200.0
var player_position: Vector2 = Vector2.ZERO

func _ready():
    print("=== ADAPTIVE INPUT SYSTEM ===")
    detect_preferred_input_method()
    demonstrate_input_methods()

func detect_preferred_input_method():
    print("Detecting preferred input method...")
    print("The game will adapt to how you like to play!")
    
    # Simulate input method detection
    var available_methods = ["keyboard", "mouse", "gamepad"]
    input_mode = available_methods[randi() % available_methods.size()]
    
    match input_mode:
        "keyboard":
            print("🎮 Keyboard controls detected! Use WASD or arrow keys.")
        "mouse":
            print("🖱️ Mouse control preferred! Click to move.")
        "gamepad":
            print("🎮 Gamepad detected! Use analog stick for movement.")

func demonstrate_input_methods():
    print("\n=== INPUT METHOD DEMONSTRATION ===")
    
    for i in range(5):
        await get_tree().create_timer(0.5).timeout
        process_movement_input()

func process_movement_input():
    match input_mode:
        "keyboard":
            simulate_keyboard_input()
        "mouse":
            simulate_mouse_input()
        "gamepad":
            simulate_gamepad_input()
    
    print("Player moved to: " + str(player_position))

func simulate_keyboard_input():
    # Simulate WASD input
    var directions = [Vector2.UP, Vector2.DOWN, Vector2.LEFT, Vector2.RIGHT, Vector2.ZERO]
    var input_direction = directions[randi() % directions.size()]
    
    if input_direction != Vector2.ZERO:
        player_position += input_direction * movement_speed * get_process_delta_time() * 10
        print("  Keyboard: Moving " + get_direction_name(input_direction))
    else:
        print("  Keyboard: No input - standing still")

func simulate_mouse_input():
    # Simulate mouse click movement
    var target_positions = [Vector2(100, 50), Vector2(-50, 100), Vector2(0, -75)]
    var target = target_positions[randi() % target_positions.size()]
    
    player_position = player_position.move_toward(target, movement_speed * get_process_delta_time() * 10)
    print("  Mouse: Moving toward " + str(target))

func simulate_gamepad_input():
    # Simulate analog stick input
    var stick_inputs = [Vector2(0.7, 0.3), Vector2(-0.5, -0.8), Vector2(0, 0)]
    var stick_direction = stick_inputs[randi() % stick_inputs.size()]
    
    if stick_direction.length() > 0.1:  # Deadzone
        player_position += stick_direction * movement_speed * get_process_delta_time() * 10
        print("  Gamepad: Analog stick " + str(stick_direction))
    else:
        print("  Gamepad: Stick in neutral position")

func get_direction_name(direction: Vector2) -> String:
    if direction == Vector2.UP:
        return "up"
    elif direction == Vector2.DOWN:
        return "down"
    elif direction == Vector2.LEFT:
        return "left"
    elif direction == Vector2.RIGHT:
        return "right"
    else:
        return "nowhere"
```

**Error Recovery and User Guidance Demo (9 minutes):**
```gdscript
var game_state: String = "menu"
var error_count: int = 0
var last_valid_state: String = "menu"

func demonstrate_error_recovery():
    print("\n=== ERROR RECOVERY SYSTEM ===")
    
    var test_scenarios = [
        "valid_input",
        "invalid_number",
        "out_of_range",
        "empty_input",
        "system_error"
    ]
    
    for scenario in test_scenarios:
        print("--- Testing scenario: " + scenario + " ---")
        simulate_user_scenario(scenario)
        await get_tree().create_timer(1.0).timeout

func simulate_user_scenario(scenario: String):
    match scenario:
        "valid_input":
            print("User: Selects valid menu option")
            process_menu_selection(1)
        
        "invalid_number":
            print("User: Enters 'abc' instead of a number")
            handle_invalid_input("abc", "number")
        
        "out_of_range":
            print("User: Selects option 99 (doesn't exist)")
            handle_out_of_range_selection(99)
        
        "empty_input":
            print("User: Presses enter without typing anything")
            handle_empty_input()
        
        "system_error":
            print("System: Unexpected error occurred")
            handle_system_error()

func process_menu_selection(option: int):
    if option >= 1 and option <= 3:
        print("✅ Valid selection: Option " + str(option))
        last_valid_state = game_state
        error_count = 0
    else:
        handle_out_of_range_selection(option)

func handle_invalid_input(input: String, expected_type: String):
    error_count += 1
    print("❌ Input Error: Expected " + expected_type + ", got '" + input + "'")
    
    if error_count == 1:
        print("💡 Hint: Please enter a number between 1 and 3.")
    elif error_count == 2:
        print("📚 Help: Here are your options: 1) Start Game, 2) Settings, 3) Quit")
    else:
        print("🔧 Auto-Help: Showing visual menu with clear options...")
        show_visual_menu()

func handle_out_of_range_selection(option: int):
    error_count += 1
    print("❌ Range Error: Option " + str(option) + " doesn't exist.")
    print("📝 Available options: 1, 2, or 3")
    
    if error_count >= 2:
        print("🎯 Suggestion: Try option 1 to start the game!")

func handle_empty_input():
    print("❓ No input received.")
    print("💬 Just press 1, 2, or 3 to make your choice!")

func handle_system_error():
    error_count += 1
    print("🚨 System Error: Something unexpected happened.")
    print("🔄 Recovery: Returning to last known good state...")
    
    game_state = last_valid_state
    print("✅ Recovered: Back to " + game_state + " safely.")
    
    if error_count >= 3:
        print("📞 Support: If problems continue, please restart the program.")

func show_visual_menu():
    print("┌─────────────────────────────┐")
    print("│        GAME MENU           │")
    print("├─────────────────────────────┤")
    print("│ 1. ▶️  Start New Game       │")
    print("│ 2. ⚙️  Settings             │")
    print("│ 3. 🚪 Exit Game             │")
    print("└─────────────────────────────┘")
    print("Just type the number of your choice!")
```

### We Do: User-Centered Design Challenge (30 minutes)
**Collaborative Interface Development**

*Students work in pairs within their track*

#### Both Tracks: "Accessibility-First Program Design"
**Building programs that work well for diverse users**

**Planning Phase (5 minutes):**
Students identify different user needs and preferences:
- Users who prefer typing vs. clicking
- Users with different reading levels or language backgrounds
- Users with limited time vs. users who want detailed information
- Users who make mistakes vs. users who are very careful
- Users with different technology comfort levels

#### Visual Programming Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Multiple Input Methods (8 minutes)**
```
Create variables [inputPreference], [userName], [userChoice]

Define custom block "detect input preference":
  Say "How do you prefer to interact with programs?" for 3 seconds
  Say "Press T for typing, C for clicking, or S for simple mode" for 4 seconds
  
  Wait until <<key [t] pressed?> or <key [c] pressed?> or <key [s] pressed?>>
  
  If <key [t] pressed?> then
    Set [inputPreference] to "typing"
    Say "Great! We'll use text input." for 2 seconds
  
  If <key [c] pressed?> then
    Set [inputPreference] to "clicking"
    Say "Perfect! We'll use click menus." for 2 seconds
  
  If <key [s] pressed?> then
    Set [inputPreference] to "simple"
    Say "Excellent! We'll keep things simple." for 2 seconds

Define custom block "get user info":
  If ([inputPreference] = "typing") then
    Ask "What's your name?" and wait
    Set [userName] to (answer)
  Else
    If ([inputPreference] = "clicking") then
      Say "Click me when ready to enter your name" for 3 seconds
      Wait until <touching [mouse-pointer]?>
      Ask "What's your name?" and wait
      Set [userName] to (answer)
    Else
      Set [userName] to "Friend"
      Say "Hi there, Friend!" for 2 seconds
```

**Step 2: Adaptive Complexity (8 minutes)**
```
Define custom block "present information" with input "complexity":
  If ([complexity] = "simple") then
    Say "Welcome! This program helps you learn." for 3 seconds
    Say "Press any key to continue." for 2 seconds
  Else
    If ([complexity] = "detailed") then
      Say "Welcome to our comprehensive learning system!" for 3 seconds
      Say "This program offers multiple ways to practice and learn new concepts." for 3 seconds
      Say "You can customize your experience and track your progress over time." for 3 seconds
    Else
      Say (join "Welcome, " (join [userName] "!")) for 2 seconds
      Say "This program adapts to how you like to learn." for 3 seconds

Define custom block "get complexity preference":
  If ([inputPreference] = "simple") then
    present information "simple" :: custom
  Else
    Ask "Would you like simple explanations or detailed information? (simple/detailed)" and wait
    If ((answer) contains "simple") then
      present information "simple" :: custom
    Else
      present information "detailed" :: custom
```

**Step 3: Error Prevention and Recovery (9 minutes)**
```
Create variables [attempts], [maxAttempts], [helpLevel], [validAnswer]

Define custom block "get safe input" with input "question":
  Set [attempts] to [0]
  Set [maxAttempts] to [3]
  Set [helpLevel] to [1]
  Set [validAnswer] to [false]
  
  Repeat until (([validAnswer] = [true]) or ([attempts] > [maxAttempts])):
    If ([helpLevel] = [1]) then
      Ask [question] and wait
    Else
      If ([helpLevel] = [2]) then
        Ask (join [question] " (Try a number between 1 and 10)") and wait
      Else
        Ask (join [question] " (Examples: 1, 5, or 10)") and wait
    
    Change [attempts] by (1)
    
    If <([answer] > [0]) and ([answer] < [11])> then
      Set [validAnswer] to [true]
      Say "Perfect! Thank you." for 2 seconds
    Else
      If ([attempts] < [maxAttempts]) then
        If ([helpLevel] = [1]) then
          Say "Hmm, that doesn't look right. Let me give you a hint!" for 3 seconds
        Else
          Say "Almost there! One more try with my help:" for 2 seconds
        
        Change [helpLevel] by (1)
      Else
        Say "No problem! Let's move on and come back to this later." for 3 seconds
        Set [validAnswer] to [true]  # Accept and move forward

When flag clicked:
  detect input preference :: custom
  get user info :: custom
  get complexity preference :: custom
  get safe input "What's your favorite number?" :: custom
```

#### Game Development Track Implementation (25 minutes)

**Collaborative Building Process:**

**Step 1: Adaptive Input System (8 minutes)**
```gdscript
extends Node2D

var user_preferences: Dictionary = {
    "input_method": "keyboard",
    "help_level": "normal",
    "error_tolerance": "medium"
}

func _ready():
    detect_user_preferences()
    demonstrate_adaptive_interface()

func detect_user_preferences():
    print("=== USER PREFERENCE DETECTION ===")
    
    print("Welcome! This program adapts to how you like to interact.")
    print("Let's figure out what works best for you...")
    
    # Simulate preference detection through usage patterns
    var interaction_patterns = [
        {"quick_inputs": true, "detailed_help": false, "error_recovery": "fast"},
        {"quick_inputs": false, "detailed_help": true, "error_recovery": "thorough"},
        {"quick_inputs": true, "detailed_help": true, "error_recovery": "medium"}
    ]
    
    var pattern = interaction_patterns[randi() % interaction_patterns.size()]
    
    if pattern["quick_inputs"]:
        user_preferences["input_method"] = "quick"
        print("📱 Quick input style detected - we'll keep prompts short")
    else:
        user_preferences["input_method"] = "detailed"
        print("📚 Detailed interaction preferred - we'll provide full explanations")
    
    if pattern["detailed_help"]:
        user_preferences["help_level"] = "detailed"
        print("🔍 Comprehensive help mode activated")
    else:
        user_preferences["help_level"] = "minimal"
        print("⚡ Streamlined help mode activated")
    
    user_preferences["error_tolerance"] = pattern["error_recovery"]
    print("🛠️ Error recovery set to: " + user_preferences["error_tolerance"])
    print("")

func demonstrate_adaptive_interface():
    print("=== ADAPTIVE INTERFACE DEMONSTRATION ===")
    
    var test_scenarios = ["menu_selection", "number_input", "text_entry"]
    
    for scenario in test_scenarios:
        print("--- Testing: " + scenario + " ---")
        handle_user_interaction(scenario)
        await get_tree().create_timer(1.0).timeout
```

**Step 2: Intelligent Error Handling (8 minutes)**
```gdscript
func handle_user_interaction(interaction_type: String):
    match interaction_type:
        "menu_selection":
            handle_menu_with_adaptation()
        "number_input":
            handle_number_with_validation()
        "text_entry":
            handle_text_with_assistance()

func handle_menu_with_adaptation():
    print("Menu Interaction:")
    
    if user_preferences["input_method"] == "quick":
        print("  Options: 1) Play 2) Quit")
    else:
        print("  ┌─ MAIN MENU ─┐")
        print("  │ 1. Start New Game - Begin your adventure │")
        print("  │ 2. Quit Game - Exit to desktop         │")
        print("  └─────────────┘")
    
    # Simulate user making an error
    var user_input = "5"  # Invalid option
    print("  User entered: " + user_input)
    
    handle_menu_error(user_input)

func handle_menu_error(invalid_input: String):
    match user_preferences["error_tolerance"]:
        "fast":
            print("  ⚡ Invalid option. Try 1 or 2.")
        "medium":
            print("  ❌ '" + invalid_input + "' isn't available.")
            print("  💡 Please choose 1 (Play) or 2 (Quit).")
        "thorough":
            print("  ❌ Error: '" + invalid_input + "' is not a valid menu option.")
            print("  📋 Available choices:")
            print("     • Enter '1' to start playing")
            print("     • Enter '2' to exit the program")
            print("  🤔 Would you like to see the menu again?")

func handle_number_with_validation():
    print("Number Input with Smart Validation:")
    
    var attempts = 0
    var max_attempts = 3
    var valid_input = false
    
    while not valid_input and attempts < max_attempts:
        attempts += 1
        
        # Simulate different user inputs
        var test_inputs = ["abc", "-5", "15", "7"]
        var current_input = test_inputs[min(attempts - 1, test_inputs.size() - 1)]
        
        print("  Attempt " + str(attempts) + ": User entered '" + current_input + "'")
        
        if validate_number_input(current_input, attempts):
            valid_input = true
            print("  ✅ Valid input accepted!")
        else:
            provide_adaptive_help(attempts)
    
    if not valid_input:
        print("  🎯 Auto-suggesting default value: 5")
        print("  💝 Don't worry - you can change this later!")

func validate_number_input(input: String, attempt: int) -> bool:
    if not input.is_valid_int():
        return false
    
    var number = int(input)
    if number < 1 or number > 10:
        return false
    
    return true

func provide_adaptive_help(attempt: int):
    match user_preferences["help_level"]:
        "minimal":
            if attempt == 1:
                print("  💫 Try a number 1-10")
            else:
                print("  🎯 Example: 5")
        "detailed":
            if attempt == 1:
                print("  📚 Please enter a whole number between 1 and 10.")
                print("  ✨ Examples of valid inputs: 1, 3, 7, 10")
            else:
                print("  🔍 Detailed help:")
                print("     • Must be a number (not letters)")
                print("     • Must be between 1 and 10 (inclusive)")
                print("     • Try typing just the number, like: 5")

func handle_text_with_assistance():
    print("Text Entry with Smart Assistance:")
    
    var sample_inputs = ["", "A", "My Name Is Too Long For This Field", "Alex"]
    
    for i in range(sample_inputs.size()):
        var input = sample_inputs[i]
        print("  Input " + str(i + 1) + ": '" + input + "'")
        
        if validate_text_input(input):
            print("  ✅ Text accepted: '" + input + "'")
            break
        else:
            provide_text_guidance(input, i + 1)
    
func validate_text_input(input: String) -> bool:
    return input.length() >= 2 and input.length() <= 20

func provide_text_guidance(invalid_input: String, attempt: int):
    if invalid_input.length() == 0:
        print("  📝 Please enter some text (at least 2 characters)")
    elif invalid_input.length() == 1:
        print("  📏 Just a bit longer - need at least 2 characters")
    elif invalid_input.length() > 20:
        print("  ✂️  A bit shorter please - maximum 20 characters")
        print("  💡 Maybe try: '" + invalid_input.substr(0, 17) + "...'")
```

**Step 3: Accessibility and Universal Design (9 minutes)**
```gdscript
var accessibility_features: Dictionary = {
    "high_contrast": false,
    "large_text": false,
    "audio_cues": false,
    "simplified_interface": false,
    "extra_time": false
}

func demonstrate_accessibility_features():
    print("\n=== ACCESSIBILITY & UNIVERSAL DESIGN ===")
    
    # Simulate different user needs
    var user_needs = [
        {"vision": "low", "motor": "normal", "cognitive": "normal"},
        {"vision": "normal", "motor": "limited", "cognitive": "normal"},
        {"vision": "normal", "motor": "normal", "cognitive": "processing_delay"}
    ]
    
    for need_profile in user_needs:
        print("--- Adapting for user profile ---")
        adapt_for_user_needs(need_profile)
        demonstrate_adapted_interface()
        await get_tree().create_timer(0.5).timeout

func adapt_for_user_needs(needs: Dictionary):
    # Reset all accessibility features
    for feature in accessibility_features:
        accessibility_features[feature] = false
    
    # Adapt based on needs
    if needs["vision"] == "low":
        accessibility_features["high_contrast"] = true
        accessibility_features["large_text"] = true
        accessibility_features["audio_cues"] = true
        print("  🔍 Visual accessibility: High contrast, large text, audio cues enabled")
    
    if needs["motor"] == "limited":
        accessibility_features["simplified_interface"] = true
        accessibility_features["extra_time"] = true
        print("  👋 Motor accessibility: Simplified interface, extended timeouts")
    
    if needs["cognitive"] == "processing_delay":
        accessibility_features["simplified_interface"] = true
        accessibility_features["extra_time"] = true
        print("  🧠 Cognitive accessibility: Clear interface, extra processing time")

func demonstrate_adapted_interface():
    print("  Interface adaptation:")
    
    if accessibility_features["high_contrast"]:
        print("    🎨 Using high contrast colors")
    
    if accessibility_features["large_text"]:
        print("    📖 TEXT SIZE INCREASED FOR READABILITY")
    
    if accessibility_features["audio_cues"]:
        print("    🔊 Audio: 'Welcome to the program' [spoken]")
    
    if accessibility_features["simplified_interface"]:
        print("    ⚡ Interface: Reduced to essential elements only")
        print("    🎯 Options: [BIG BUTTON] Start  [BIG BUTTON] Help")
    else:
        print("    🖥️  Standard interface with full feature set")
    
    if accessibility_features["extra_time"]:
        print("    ⏱️  Extended timeout: 30 seconds instead of 10")
    
    print("    ✨ All users can interact successfully!")
```

### You Do: Personal Accessibility Project (20 minutes)
**Independent User Experience Design**

#### Individual Challenge: "Universal Design Champion"
**Create a program that works well for diverse users with different needs and preferences**

**Project Options:**
1. **Study Helper Tool:** Support different learning styles, reading levels, and time constraints
2. **Game Menu System:** Accommodate different input preferences, experience levels, and accessibility needs
3. **Information Collector:** Handle various response styles, error patterns, and user comfort levels
4. **Creative Expression Tool:** Support different creative processes, technical skills, and artistic goals

**Universal Design Requirements:**
- **Multiple Input Methods:** At least 2 different ways users can interact
- **Adaptive Complexity:** Program adjusts detail level based on user preference or performance
- **Error Recovery:** Graceful handling of mistakes with helpful guidance
- **Clear Feedback:** Users always know what's happening and what to do next
- **Accessibility Features:** At least 2 accommodations for different user needs

**User Experience Goals:**
- **Inclusive:** Works for users with different abilities and preferences
- **Forgiving:** Mistakes don't cause frustration or program failure
- **Adaptive:** Program learns from user behavior and adjusts accordingly
- **Clear:** Purpose and next steps are always obvious to users

**Self-Assessment Questions:**
1. How does my program accommodate different user preferences and abilities?
2. What happens when users make mistakes, and how does my program help them recover?
3. How does my program provide feedback that helps users understand what's happening?
4. What would make my program even more accessible and user-friendly?

### Wrap-Up: User Experience Reflection (5 minutes)
**"Great Design is Invisible - Bad Design is Frustrating"**

#### User Experience Principles Review (3 minutes)
**Quick Class Discussion:**
- "What's the most user-friendly feature you added to your program?"
- "How did thinking about different user needs change your design approach?"
- "What's one way you could make your Unit 1 portfolio more accessible?"

#### Preview Tomorrow (2 minutes)
**"Next: Algorithms and Problem Solving - Systematic Approaches to Complex Challenges"**
- Tomorrow we'll learn formal problem-solving strategies and algorithm design
- We'll practice breaking complex problems into systematic, step-by-step solutions
- We'll explore how different algorithms can solve the same problem with different trade-offs

## Differentiation Strategies

### For Students Who Need More Support
- Provide user experience templates with guided questions about user needs
- Start with simple input validation before progressing to complex error handling
- Use pair programming with partners who can help think through user perspectives
- Offer concrete examples of accessibility features and their purposes

### For Advanced Students
- Challenge to research and implement advanced accessibility features
- Encourage exploration of professional UX design principles and industry standards
- Provide opportunities to conduct user testing with classmates and iterate based on feedback
- Offer extension activities with complex input validation and state management

### For Students With Accessibility Needs
- Ensure their own needs are accommodated in the development environment
- Connect their personal experiences to universal design principles
- Provide opportunities to share expertise about accessibility features that help them
- Consider their insights as valuable contributions to class understanding of inclusive design

## Assessment Strategy

### Formative Assessment
**User Experience Design Understanding:**
- Observation of student consideration of diverse user needs during design
- Quality of error handling and input validation implementation
- Evidence of testing programs with different types of user input

### User Interface Quality Assessment:**
- Working programs that handle unexpected input gracefully
- Clear, helpful feedback for user actions and errors
- Evidence of consideration for users with different abilities and preferences
- Demonstration of understanding how good design improves user experience

## Homework/Extension Activities

### For All Students (Required)
**"User Experience Audit of Daily Technology":**
- Choose one app or website you use regularly
- Identify 3 examples of excellent user experience design and explain why they work well
- Find 2 examples of poor user experience and suggest specific improvements
- Test how the technology handles errors or unexpected input
- Write a brief reflection on how this analysis will influence your programming projects

### For Students Wanting More Challenge
**"Advanced Accessibility Research":**
- Research accessibility guidelines like WCAG (Web Content Accessibility Guidelines)
- Implement advanced input validation techniques or error recovery systems
- Design and test interfaces with users who have different abilities or preferences
- Explore how professional software handles user experience challenges

### For Students Needing More Practice
**"User Experience Fundamentals Building":**
- Create simple programs focusing on one UX principle at a time (clarity, feedback, etc.)
- Practice writing clear, helpful error messages for common input mistakes
- Test programs with family or friends to get feedback on usability
- Study examples of excellent user interfaces in familiar apps and games

## Next Lesson Preview
**"Tomorrow: Algorithms and Problem Solving - The Science of Systematic Solutions"**

**What Students Will Learn:**
- Formal approaches to analyzing and breaking down complex problems
- Different algorithmic strategies and when to use each approach
- How to evaluate and compare different solutions to the same problem
- Professional problem-solving techniques used by software engineers

**What Students Will Do:**
- Practice systematic problem decomposition and solution design
- Implement multiple algorithms that solve the same problem different ways
- Analyze the trade-offs between different algorithmic approaches
- Apply algorithmic thinking to improve their existing programs

---

**🎨 Excellent! Your students now understand how to create programs that work well for diverse users with different needs, preferences, and abilities. They're ready to learn systematic approaches to solving complex problems with algorithms! 💻♿✨**