# Lesson 21: Introduction to Game Development with Godot
**AP Computer Science Principles | Unit 2: Programming Structures - Track B**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 11
- **Unit:** Programming Structures & Computational Thinking - Track B (Game Development)
- **Prerequisites:** Completed Unit 1 (Web Development), Track selection completed

## Learning Targets

### I am learning to...
1. **Understand** game development as a professional programming discipline that applies computational thinking to interactive entertainment
2. **Analyze** how game engines organize code, art, and logic into cohesive interactive experiences
3. **Create** my first functional game using Godot's node system, GDScript, and fundamental programming concepts

### Success Criteria - I can...
1. **Navigate** the Godot interface confidently and explain the purpose of scenes, nodes, and the scripting system
2. **Build** a simple interactive game with player movement and basic game mechanics using GDScript
3. **Connect** game development concepts to AP Computer Science Principles Big Ideas and real-world programming applications

## AP Big Ideas Connections

### Primary Focus
- **AAP-2.A:** Express an algorithm that uses sequencing without using a programming language
  - *Connection:* Game design documents and flowcharts represent game logic before coding
- **AAP-2.B:** Represent a step-by-step algorithmic process using sequential code statements
  - *Connection:* GDScript functions execute game logic in response to player actions and game events
- **AAP-1.A:** Represent a value with a variable
  - *Connection:* Game variables store player data, game state, and dynamic information

### Supporting Connections
- **CRD-2.A:** Describe the purpose of a computing innovation
  - *Connection:* Games are computing innovations that entertain, educate, and solve problems
- **AAP-3.A:** For procedure calls: write statements to call procedures
  - *Connection:* Game functions organize code into reusable, modular components

## Materials Needed

### Technology
- Computers with Godot Engine 4.x installed
- Sufficient processing power for game development (test on school hardware)
- Access to simple game art assets (provided or student-created)
- Audio support for sound effects and music (headphones recommended)

### Resources
- Godot interface navigation guide
- GDScript syntax reference sheet
- Game design planning template
- Simple sprite and sound asset library

### Preparation
- Install Godot on all classroom computers and test performance
- Create sample game project for demonstration purposes
- Prepare art assets and sounds appropriate for educational use
- Set up backup plans for hardware that cannot run Godot smoothly

## Why Track B? Game Development Benefits

### Pedagogical Advantages
**High Engagement:** Students naturally motivated by game creation and interactive entertainment experiences.

**Professional Relevance:** Godot is a real game engine used by indie developers and studios worldwide, providing authentic development experience.

**Interdisciplinary Integration:** Games combine programming, art, music, storytelling, and mathematics in creative ways.

**Complex Problem-Solving:** Game development requires planning, debugging, and iterative improvement - core computational thinking skills.

### Connection to AP Goals
**Same Programming Concepts:** Students learn variables, functions, conditionals, and loops through game development rather than abstract examples.

**Real-World Application:** Game mechanics demonstrate algorithms, data structures, and user interface design in engaging contexts.

**Creative Expression:** Games allow personal creativity while meeting technical requirements, similar to AP Performance Task expectations.

## Lesson Structure (90 minutes)

### Warm-Up Activity (10 minutes)
**"What Makes a Game Fun?" Analysis**

#### Part 1: Game Deconstruction (5 minutes)
**Interactive Discussion:**
1. Display screenshots from 3-4 popular games (age-appropriate: Minecraft, Among Us, simple mobile games)
2. Ask students to identify what makes each game engaging
3. Guide discussion toward game mechanics, challenge, and interactivity

**Discussion Prompts:**
- "What do you DO in this game?"
- "What keeps players coming back?"
- "How does the game respond to player actions?"

#### Part 2: Games as Programs (5 minutes)
**Connect to Programming Concepts:**
- "Every game is a computer program responding to user input"
- "Game logic uses the same programming concepts as websites: variables, functions, conditionals"
- "Today we'll learn to think like game developers and create interactive experiences"

**Key Teaching Point:**
"Games are complex programs that manage graphics, sound, user input, and logic simultaneously. We'll start simple and build up to creating complete game experiences."

### I Do: Teacher Demonstration (25 minutes)
**"Welcome to Godot: Building Games with Code"**

#### Part 1: Godot Interface Tour (10 minutes)
**Guided Interface Exploration:**

**Scene System (top left):**
- "Scenes are like levels or screens in our game"
- "Each scene contains nodes that handle different parts of game functionality"
- "We can have menu scenes, game scenes, and game over scenes"

**Node Hierarchy (left panel):**
- "Nodes are building blocks: sprites for graphics, physics bodies for movement, etc."
- "Nodes are organized in parent-child relationships"
- "Child nodes inherit properties from their parents"

**Viewport (center):**
- "This is where we see our game as players will see it"
- "We can move, scale, and position game elements here"
- "The camera determines what players see"

**Inspector (right panel):**
- "Properties and settings for selected nodes"
- "We can adjust behavior without writing code"
- "Connect visual properties to code functionality"

**Script Editor (bottom/separate window):**
- "Where we write GDScript code to control game behavior"
- "Each node can have a script that defines what it does"
- "Scripts respond to events and update game state"

#### Part 2: First Game Creation (15 minutes)
**Live Coding: "Moving Character Game"**

**Step 1: Scene Setup (5 minutes)**
```gdscript
# Create new 2D scene
# Add CharacterBody2D node (for player)
# Add Sprite2D as child (for player appearance)  
# Add CollisionShape2D as child (for physics)
```

**Teaching Narration:**
- "CharacterBody2D handles player movement and physics"
- "Sprite2D displays the visual representation"
- "CollisionShape2D defines the physical boundaries"

**Step 2: Basic Player Script (10 minutes)**
```gdscript
extends CharacterBody2D

# Variables store game data - just like in JavaScript!
var speed = 200.0

# This function runs every frame (60 times per second)
func _physics_process(delta):
    # Get input from player
    var direction = Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
    
    # Apply movement
    velocity = direction * speed
    
    # Move the character
    move_and_slide()
```

**Key Concepts Emphasized:**
- **Variables:** `speed` stores how fast character moves
- **Functions:** `_physics_process()` runs continuously like a loop
- **Input:** `Input.get_vector()` detects what keys player presses
- **Physics:** `move_and_slide()` handles collision and movement

**Live Testing:**
- Run the game and demonstrate character movement
- Show how changing `speed` variable affects gameplay
- Demonstrate that this is real programming with immediate visual results

### We Do: Guided Practice (25 minutes)
**"Let's Build a Collect-the-Items Game Together"**

#### Setup and Project Creation (10 minutes)
**Getting Everyone Started:**
1. Students open Godot and create new project
2. Walk through creating 2D scene with CharacterBody2D player
3. Help students add sprite and collision shape to their player
4. Ensure everyone can run basic project and see character on screen

**Troubleshooting Support:**
- Check Godot installation issues
- Help with project creation and saving
- Assist with node creation and hierarchy understanding
- Address performance issues on slower computers

#### Collaborative Game Building (15 minutes)
**Build Game Features Together with Student Input:**

**Teacher Facilitates, Students Contribute Ideas:**
"Let's create a game where the player collects items! What should our character collect?"

**Feature 1: Collectible Items (8 minutes)**
```gdscript
# Create new scene for collectible item
# Add Area2D node (detects when player touches it)
# Add Sprite2D child (visual appearance)
# Add CollisionShape2D child (detection area)

# Collectible item script:
extends Area2D

func _ready():
    # Connect signal when something enters the area
    body_entered.connect(_on_body_entered)

func _on_body_entered(body):
    if body.name == "Player":
        print("Item collected!")  # Show message
        queue_free()  # Remove item from game
```

**Feature 2: Score Tracking (7 minutes)**
```gdscript
# Add to player script:
extends CharacterBody2D

var speed = 200.0
var score = 0  # New variable to track score

# Add score label to scene
# Update player movement function to include score display

func collect_item():
    score += 1
    print("Score: " + str(score))
```

**Teaching Strategies During Guided Practice:**
- **Students make design choices:** "What color should our collectible items be?"
- **Explain programming concepts:** "Why do we use signals to detect collisions?"
- **Show immediate results:** Run game after each feature to see progress
- **Connect to prior learning:** "This variable works just like JavaScript variables!"

### Break (5 minutes)
**Movement and Mental Reset**
- Stand up and stretch
- Quick discussion about favorite games and why they're engaging
- Prepare for independent creative work

### You Do: Independent Practice (20 minutes)
**"Create Your Personal Game Prototype"**

#### Assignment Instructions
**Build a simple game that demonstrates programming concepts:**

**Required Game Elements:**
1. **Player character** that moves in response to keyboard input
2. **At least one game mechanic** (collecting items, avoiding obstacles, reaching goals)
3. **Variables** that store and track game information (score, lives, time, etc.)
4. **Game feedback** that responds to player actions (messages, score updates, etc.)
5. **Proper GDScript syntax** with functions and game logic

#### Creative Game Ideas:

**Beginner Level:**
- Collect items scattered around the screen
- Simple maze navigation game
- Character that grows or changes as it collects things

**Intermediate Level:**  
- Avoid moving obstacles while collecting items
- Timer-based challenges with countdown
- Simple platformer with jumping mechanics

**Advanced Level:**
- Multiple levels or scenes
- Different types of collectibles with different point values
- Power-ups that change player abilities

#### Code Examples for Reference:

**Basic Player Movement:**
```gdscript
extends CharacterBody2D

var speed = 300.0

func _physics_process(delta):
    var direction = Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
    velocity = direction * speed
    move_and_slide()
```

**Simple Collision Detection:**
```gdscript
extends Area2D

func _ready():
    body_entered.connect(_on_body_entered)

func _on_body_entered(body):
    if body.has_method("collect_item"):
        body.collect_item()
        queue_free()
```

**Score Display:**
```gdscript
extends Label

var current_score = 0

func update_score(new_score):
    current_score = new_score
    text = "Score: " + str(current_score)
```

### Teacher Support During Independent Work
**Circulate and Provide Just-in-Time Help:**

**Common Issues and Solutions:**
- **"My character doesn't move!"** → Check script is attached to correct node, verify input map
- **"I can't see my character!"** → Check sprite texture is assigned, verify camera position
- **"Collisions don't work!"** → Ensure collision shapes are properly configured and connected
- **"My script has errors!"** → Review GDScript syntax, check for missing colons and indentation

**Game Design Guidance:**
- "Start simple - get one mechanic working before adding more"
- "Test frequently - run your game after each small change"
- "Think like a player - what would make this fun?"
- "Use print() statements to debug - see what your code is doing"

**Encouraging Development:**
- "I love the creativity in your game concept!"
- "Great job getting the basic mechanics working first!"
- "Your problem-solving approach is very professional!"
- "This game mechanic shows excellent understanding of variables and functions!"

#### Differentiation Strategies

**For Advanced Students:**
- Implement multiple scenes (menu, game, game over)
- Add sound effects and background music
- Create more complex physics interactions