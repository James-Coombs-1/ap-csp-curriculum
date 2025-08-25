# Lesson 11: Programming Track Introduction & Setup
**Duration:** 90 minutes (A/B Block) | **Week:** 6

## Learning Targets

### I am learning to...
1. **Set up** professional development environments for my chosen programming track
2. **Understand** how fundamental programming concepts apply across different languages and platforms
3. **Create** my first program in my chosen track that demonstrates basic computational thinking

### Success Criteria - I can...
1. **Successfully install** and configure my track's development environment with proper account setup
2. **Explain** how variables, functions, and control structures work in my chosen programming language
3. **Build** a simple interactive program that demonstrates user input, processing, and output

## AP Big Ideas Connections

### Primary Focus
- **CRD-2.B:** Explain how a program or code segment functions
- **AAP-1.A:** Represent a value with a variable
- **AAP-2.A:** Express an algorithm that uses sequencing without using a programming language

### Supporting Connections
- **CRD-2.F:** Design a program and its user interface
- **AAP-3.A:** Explain how abstraction manages complexity

## Materials Needed

### For Both Tracks
- Computers with admin access for software installation
- Account creation access for required platforms
- Backup plans for installation difficulties
- Cross-track collaboration materials

### Visual Programming Track
- Scratch accounts (scratch.mit.edu)
- MIT App Inventor accounts (appinventor.mit.edu)
- Visual programming reference guides
- Block-based programming examples

### Game Development Track  
- Godot Engine installation files (godotengine.org)
- GDScript reference documentation
- Game development asset libraries
- Text editor preferences and setup

## Lesson Structure (90 minutes)

### Opening: Programming Concepts Bridge (10 minutes)
**"Same Ideas, Different Tools"**

#### Universal Programming Concepts (5 minutes)
**Connecting Unit 1 to Unit 2:**

**Teacher Live Demonstration:**
Show the same program logic in three formats side-by-side:

**JavaScript (familiar from Unit 1):**
```javascript
let playerName = prompt("What's your name?");
if (playerName.length > 0) {
    alert("Welcome to programming, " + playerName + "!");
} else {
    alert("Hello, mysterious programmer!");
}
```

**Scratch blocks (visual):**
```
When flag clicked
Ask "What's your name?" and wait
Set [playerName] to (answer)
If ((length of [playerName]) > 0) then
  Say (join "Welcome to programming, " [playerName]) for 3 seconds
Else
  Say "Hello, mysterious programmer!" for 3 seconds
```

**GDScript (text-based game development):**
```gdscript
extends Node2D

func _ready():
    var player_name = get_user_input("What's your name?")
    if player_name.length() > 0:
        print("Welcome to programming, " + player_name + "!")
    else:
        print("Hello, mysterious programmer!")
```

**Key Teaching Message:** "The thinking is the same - only the tools change!"

#### Track-Specific Applications (5 minutes)
**Visual Programming Applications:**
- Interactive educational content and tutorials
- Mobile apps solving real-world problems
- Data visualization and storytelling projects
- Accessible programming for diverse users and abilities

**Game Development Applications:**
- Entertainment and educational games
- Simulation and modeling of complex systems  
- Interactive art and experimental media
- Technical skills valuable across the software industry

### I Do: Development Environment Setup (35 minutes)
**Professional Environment Configuration**

*Students split into track-specific groups for parallel instruction*

#### Visual Programming Track Setup (35 minutes)
**Teacher Live Setup Process:**

**Scratch Account and Interface (15 minutes)**
1. **Account Creation (5 minutes):** 
   - Navigate to scratch.mit.edu
   - Create account with appropriate username and password
   - Verify email and set up profile information
   - Review community guidelines and safety features

2. **Interface Deep Dive (10 minutes):**
   - **Stage Area:** Where your program runs and displays output
   - **Sprite List:** Characters and objects in your program
   - **Block Palette:** All programming commands organized by category
   - **Scripts Area:** Where you build programs by connecting blocks
   - **Costumes/Sounds Tabs:** Customizing visual and audio elements

**MIT App Inventor Setup (15 minutes)**
1. **Account Access (5 minutes):**
   - Navigate to appinventor.mit.edu
   - Sign in with Google account (school or personal)
   - Accept terms of service and review getting started guide
   - Explore project gallery for inspiration

2. **Interface Overview (10 minutes):**
   - **Designer View:** Visual interface creation with drag-and-drop components
   - **Blocks View:** Program logic using visual programming blocks
   - **Mobile Connection:** Phone companion app or emulator setup
   - **Project Management:** Save, export, share, and collaborate options

**Visual Programming Best Practices (5 minutes)**
- Emphasize visual programming's power and professional legitimacy
- Show examples of professional applications built with visual programming
- Address any perceptions that visual programming is "less serious" than text-based
- Highlight the focus on computational thinking without syntax barriers

#### Game Development Track Setup (35 minutes)
**Teacher Live Setup Process:**

**Godot Engine Installation (15 minutes)**
1. **Download and Install (8 minutes):**
   - Navigate to godotengine.org
   - Select appropriate version for operating system
   - Check system requirements and compatibility
   - Complete installation with default settings

2. **Project Manager Overview (7 minutes):**
   - Create new project with appropriate name and location
   - Import existing projects and explore project templates
   - Understand project organization and file structure
   - Configure version control and backup settings

**Godot Interface Deep Dive (15 minutes)**
1. **Editor Layout (8 minutes):**
   - **Scene Dock:** Hierarchical structure of game objects
   - **FileSystem:** Project files and asset organization
   - **Inspector:** Properties and settings for selected objects
   - **Main Editor:** Visual scene editing and script development

2. **Script Development Environment (7 minutes):**
   - **Script Editor:** Syntax highlighting, error detection, debugging tools
   - **Documentation Access:** Built-in help system and online resources
   - **Version Control:** Git integration and collaborative development features
   - **Testing Tools:** Play project, debug mode, and performance monitoring

**Professional Development Practices (5 minutes)**
- Connect Godot to industry-standard game development workflows
- Highlight transferable skills to other programming environments
- Discuss how game development teaches fundamental CS concepts
- Show examples of successful games built by students and professionals

### We Do: First Program Creation (30 minutes)
**Guided Programming Experience**

*Parallel track instruction with similar learning objectives*

#### Visual Programming Track: Interactive Greeting Program (30 minutes)
**Building Together Step-by-Step**

**Program Planning (5 minutes):**
- Define program goal: Create personalized greeting with user choices
- Identify required elements: sprites, variables, user input, conditionals
- Plan user experience flow and interface design

**Collaborative Building Process (20 minutes):**

**Step 1: Basic Setup (5 minutes)**
```
Create new Scratch project
Choose or draw a character sprite
Set up stage background
Test basic sprite movement
```

**Step 2: User Interaction (8 minutes)**
```
Add "When flag clicked" event
Use "Ask and wait" block for user's name
Store response in variable called "userName"
Use "Ask and wait" for user's favorite activity
Store response in variable called "activity"
```

**Step 3: Conditional Responses (7 minutes)**
```
Create if-then-else structure based on activity choice
Program different responses for different activities:
- If activity = "gaming" → Character says "Let's play!"
- If activity = "music" → Character plays a sound
- If activity = "sports" → Character does jumping animation
- Else → Character says "That sounds fun!"
```

**Testing and Refinement (5 minutes):**
- Run program and test all pathways
- Debug any issues with variable names or block connections
- Add creative enhancements (colors, sounds, animations)
- Share with partner for feedback and testing

#### Game Development Track: Character Controller Program (30 minutes)
**Building Together Step-by-Step**

**Program Planning (5 minutes):**
- Define program goal: Create controllable character with basic game mechanics
- Identify required elements: character node, input detection, movement physics
- Plan game feel and responsive controls

**Collaborative Building Process (20 minutes):**

**Step 1: Scene Setup (5 minutes)**
```gdscript
# Create new 2D scene
# Add CharacterBody2D node as main character
# Add Sprite2D as child for character visual
# Add CollisionShape2D for physics interaction
# Save scene with descriptive name
```

**Step 2: Basic Movement Script (8 minutes)**
```gdscript
extends CharacterBody2D

@export var speed = 200.0
var player_name = ""

func _ready():
    player_name = "Hero"  # Will improve this later
    print("Welcome to the game, " + player_name + "!")

func _physics_process(delta):
    # Get input direction from arrow keys
    var input_direction = Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
    
    # Apply movement
    velocity = input_direction * speed
    move_and_slide()
```

**Step 3: Enhanced Interaction (7 minutes)**
```gdscript
func _physics_process(delta):
    var input_direction = Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
    velocity = input_direction * speed
    move_and_slide()
    
    # Add feedback for movement
    if velocity.length() > 0:
        print(player_name + " is moving!")
    
    # Add action button interaction
    if Input.is_action_just_pressed("ui_accept"):
        print(player_name + " performed an action!")
```

**Testing and Refinement (5 minutes):**
- Run scene and test character movement in all directions
- Debug any movement issues or script errors
- Adjust speed and responsiveness for good game feel
- Add creative enhancements (sprite changes, particle effects)

### You Do: Personal Customization Project (10 minutes)
**Independent Practice and Creative Expression**

#### Individual Customization Challenge
**For Both Tracks: "Make It Your Own"**

**Visual Programming Track:**
- Add personal touches to your greeting program
- Include your favorite colors, sounds, or activities
- Create additional interaction options or responses
- Experiment with sprite costumes and stage backgrounds

**Game Development Track:**
- Customize your character's appearance and movement speed
- Add sound effects or visual feedback for movement
- Create simple obstacles or boundaries in the scene
- Experiment with different movement patterns or physics settings

**Self-Assessment Questions (for both tracks):**
1. What programming concepts am I using in my customized program?
2. How does this program demonstrate input, processing, and output?
3. What would I like to learn next to improve my program?
4. How confident do I feel about continuing in this track?

### Wrap-Up: Community Formation and Next Steps (5 minutes)
**"Your Programming Journey Continues"**

#### Track Communities Formation (3 minutes)
**Building Support Networks:**
- Visual Programming track students introduce themselves and share customizations
- Game Development track students form their community and demonstrate character controllers
- Exchange contact information for peer support and collaboration
- Plan informal collaboration and help-giving throughout Unit 2

#### Unit 2 Roadmap Preview (2 minutes)
**Looking Ahead:**
- **Lesson 12:** Variables and Data Types in Context - building on today's foundation
- **Lessons 13-17:** Core programming concepts through track-specific projects
- **Unit 2 Portfolio Integration:** All projects will enhance existing portfolios
- **Peer Learning:** Regular cross-track sharing and collaboration opportunities

**Excitement Building:**
"You've successfully set up your development environment and created your first program in your chosen track. Whether you're building interactive stories or games, you're ready to dive deep into the core concepts that every programmer needs to know!"

## Differentiation Strategies

### For Students With Setup Difficulties
- Provide step-by-step troubleshooting guides for common installation issues
- Have backup accounts and alternative access methods ready
- Pair struggling students with tech-savvy classmates for peer support
- Consider browser-based alternatives if local installation fails

### For Advanced Students
- Provide extension challenges that explore advanced features of their development environment
- Offer additional resources for independent exploration of programming concepts
- Encourage them to become peer mentors and technical support for classmates
- Show examples of sophisticated projects possible in their chosen track

### For Students With Accessibility Needs
- Ensure development environments work with assistive technologies
- Provide alternative input methods and interface adaptations as needed
- Consider individual accommodations for programming environment preferences
- Connect with accessibility features available in Scratch and Godot

## Assessment Strategy

### Formative Assessment
**Environment Setup Success:**
- Successful completion of development environment installation and configuration
- Ability to create, save, and run basic programs in chosen track
- Demonstration of understanding basic interface navigation and tool usage

### Programming Concept Understanding:**
- Explanation of how variables store and use information in their program
- Identification of input, processing, and output elements in their creation
- Connection of new programming language to concepts learned in Unit 1

## Homework/Extension Activities

### For All Students (Required)
**"Programming Environment Exploration":**
- Spend 30 minutes exploring your development environment's help resources and tutorials
- Create one additional small program using a programming concept not covered in class
- Research one professional application or game built using your track's tools
- Prepare to share one interesting discovery about your programming environment with the class

### For Students Wanting More Challenge
**"Advanced Feature Investigation":**
- Explore advanced features of your development environment (advanced blocks, complex nodes)
- Find and analyze a sophisticated project created by other users in your track
- Begin planning a more ambitious project that you'd like to create during Unit 2
- Research programming communities and resources for continued learning in your track

### For Students Needing More Practice
**"Foundation Strengthening":**
- Complete additional basic tutorials provided by your development environment
- Practice creating variations of today's program with different customizations
- Review Unit 1 programming concepts and connections to your new track
- Set up regular practice schedule with peer mentor or study group

## Materials for Next Lesson

### Teacher Preparation
- Examples of creative programs that demonstrate variables and data types in both tracks
- Debugging scenarios and common mistakes for guided practice
- Assessment rubrics for programming concept understanding and application

### Student Readiness
- Fully configured development environment with saved programs from today
- Basic familiarity with interface navigation and program creation workflow
- Enthusiasm for diving deeper into programming concepts and creative applications
- Track community connections established for peer support and collaboration

---

**🚀 Excellent! Your students are now equipped with professional development environments and have successfully created their first programs in their chosen tracks. They're ready to explore the fundamental programming concepts that will form the foundation of their computational thinking skills!**

**Tomorrow we'll dive into variables and data types, building on the foundation they've established today to create more sophisticated and interactive programs! 💻✨**