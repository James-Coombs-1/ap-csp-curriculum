# Track Sampling Week: Informed Choice for Programming Paths
**AP Computer Science Principles | Unit 1-2 Bridge Week**

## Week Overview
- **Timing:** Week 10 (End of Unit 1, Before Unit 2 Track Selection)
- **Duration:** 2 blocks (180 minutes total) of hands-on programming exploration
- **Purpose:** Students experience both Track A and Track B before making informed choice
- **Outcome:** Confident track selection based on personal experience, not assumptions

## Track Sampling Philosophy

### **Informed Choice > Guesswork**
Rather than asking students to choose their programming path based on descriptions, they experience both approaches firsthand and make decisions based on:
- **Personal interest and engagement** with each programming style
- **Learning style compatibility** with visual vs. text-based programming
- **Creative expression preferences** (apps/stories vs. games/simulations)
- **Confidence and comfort level** with different programming environments

### **"Try Before You Decide" Benefits**
- **Reduces anxiety** about unknown programming approaches
- **Builds on success** from Unit 1 web development foundation
- **Connects to interests** discovered through hands-on experience
- **Prevents regret** from uninformed track selection
- **Increases engagement** when students choose based on genuine preference

---

## Day 1 (Block 1): Track A Exploration - Visual Programming Sampler
**Duration:** 90 minutes

### Learning Targets
Students will experience visual programming through Scratch and understand how block-based coding enables focus on logic and creativity without syntax barriers.

### Session Structure (90 minutes)

#### Opening: Programming Path Preview (10 minutes)
**"Two Paths to the Same Destination"**

**Visual Comparison:**
- Show same programming concept (loops) in both Scratch blocks and text code
- Emphasize: "Both teach identical programming concepts - different tools, same thinking"
- Preview: "Today you'll try visual programming; tomorrow, game development"

**Track A Quick Overview:**
- **Visual Programming:** Drag-and-drop blocks instead of typing code
- **Focus:** Logic and creativity without syntax concerns
- **Applications:** Interactive stories, educational apps, mobile applications
- **AP Preparation:** Same concepts, visual expression

#### Activity 1: Scratch Quick Start Challenge (30 minutes)
**"Make Something Amazing in 30 Minutes"**

**Challenge Options (Students Choose):**
1. **Animation Creator:** Make sprites move, dance, and interact
2. **Story Builder:** Create interactive story with choices and outcomes
3. **Game Prototype:** Simple reaction game or maze navigation
4. **Art Generator:** Use code to create visual art and patterns

**Guided Discovery Format:**
- **5 minutes:** Scratch interface tour and basic block explanation
- **20 minutes:** Hands-on exploration with peer collaboration encouraged
- **5 minutes:** Quick gallery walk to see everyone's creations

**Teacher Support Style:**
- Minimal direct instruction - encourage exploration
- Peer tutoring and discovery learning emphasized
- Focus on "what happens if I try this?" experimentation
- Celebrate unique approaches and creative solutions

#### Activity 2: App Development Simulation (25 minutes)
**"Design an App for Your School"**

**Challenge:** Create interactive prototype addressing real school problem

**Example Problems Students Might Choose:**
- Lost and found tracker
- Study group organizer
- Cafeteria menu with reviews
- Club meeting coordinator
- Homework reminder system

**Scratch Implementation:**
```scratch
// Example: Study Group Organizer
When [green flag] clicked
ask [What subject do you need help with?] and wait
set [subject] to (answer)
ask [What's your available time?] and wait  
set [time] to (answer)
say (join [Looking for study partners for ] (subject)) for (2) seconds
say (join [Available: ] (time)) for (2) seconds
```

**Development Process:**
- **10 minutes:** Problem identification and app planning
- **10 minutes:** Scratch prototype creation
- **5 minutes:** Peer testing and feedback

#### Activity 3: Visual Programming Reflection (20 minutes)
**"Track A Experience Analysis"**

**Small Group Reflection (10 minutes):**
Students discuss in groups of 3-4:
- What felt natural vs. challenging about visual programming?
- How did block-based coding affect your ability to focus on logic?
- What types of projects excited you most in this environment?
- How confident did you feel experimenting and trying new approaches?

**Individual Reflection Survey (10 minutes):**
```
Track A Experience Survey:

Engagement Level (1-5 scale):
□ How interested were you in the visual programming activities?
□ How comfortable did you feel learning through exploration?
□ How excited are you about the potential projects you could create?

Learning Style Fit (1-5 scale):
□ Did visual blocks help you understand programming concepts?
□ Did you prefer dragging blocks vs. typing code?
□ Did the immediate visual feedback enhance your learning?

Creative Expression (1-5 scale):  
□ Did you feel creative freedom in the visual environment?
□ Were you able to express your ideas effectively?
□ Did you enjoy the types of projects possible with visual programming?

Confidence Indicators:
□ I felt comfortable experimenting with new blocks
□ I was able to debug problems effectively
□ I could help classmates with their projects
□ I want to learn more about visual programming
```

#### Wrap-Up Preview (5 minutes)
**"Tomorrow: Game Development Track B"**
- "You've experienced visual programming - tomorrow you'll try professional game development"
- "Keep track of how both experiences feel - you'll choose based on what works best for you"
- "No wrong choice - both paths teach the same AP concepts through different creative expressions"

---

## Day 2 (Block 2): Track B Exploration - Game Development Sampler  
**Duration:** 90 minutes

### Learning Targets
Students will experience game development through Godot engine and understand how professional development tools enable complex, creative project development.

### Session Structure (90 minutes)

#### Opening: Game Development Preview (10 minutes)
**"Professional Tools for Creative Projects"**

**Track B Overview:**
- **Game Development:** Professional game engine with scripting language
- **Focus:** Complex project development with visual and code integration
- **Applications:** 2D games, simulations, interactive experiences
- **AP Preparation:** Advanced programming concepts through engaging projects

**Demo Motivation:**
- Show impressive student game projects from previous years
- Emphasize: "You'll create games people actually want to play"
- Connection: "Same programming logic as yesterday, different creative outlet"

#### Activity 1: Godot Quick Game Creation (35 minutes)
**"Build a Playable Game in 35 Minutes"**

**Rapid Development Challenge:**
Students create simple but complete games using provided templates

**Game Options (Students Choose):**
1. **Collector Game:** Player moves around collecting items
2. **Dodge Game:** Avoid falling objects, survive as long as possible  
3. **Maze Runner:** Navigate through obstacles to reach goal
4. **Reaction Game:** Click targets as they appear, track score

**Template-Assisted Development:**
```gdscript
# Collector Game Template (Students customize)
extends CharacterBody2D

var speed = 200
var score = 0

func _physics_process(delta):
    var direction = Input.get_vector("ui_left", "ui_right", "ui_up", "ui_down")
    velocity = direction * speed
    move_and_slide()

func collect_item():
    score += 1
    print("Score: " + str(score))
```

**Development Process:**
- **5 minutes:** Godot interface orientation and template explanation
- **25 minutes:** Hands-on game creation with customization
- **5 minutes:** Playtesting session with peer feedback

**Support Philosophy:**
- Templates eliminate syntax barriers while preserving learning
- Focus on game design and mechanics rather than language details
- Encourage artistic customization and personal creative touches

#### Activity 2: Game Design Workshop (25 minutes)
**"Design Your Dream Game Project"**

**Planning Exercise:**
Students design game projects they'd want to build over 10 weeks

**Design Template:**
```
My Game Design Concept:

Game Title: _________________________________
Genre: _____________________________________
Player Goal: _______________________________
Main Character: ____________________________
Key Game Mechanics:
1. ________________________________________
2. ________________________________________  
3. ________________________________________

What makes this game fun and unique?
____________________________________________

What programming concepts would this require?
□ Character movement    □ Collision detection
□ Score tracking       □ Multiple levels
□ Sound effects       □ Animations
□ User interface      □ Save/load system
```

**Peer Collaboration:**
- **15 minutes:** Individual game concept development
- **10 minutes:** Partner sharing and feedback exchange

#### Activity 3: Professional Development Exposure (15 minutes)
**"Real Game Development Process"**

**Industry Connection Activity:**
Students explore how professional game development works

**Brief Exploration:**
- Game development career paths and roles
- How indie developers create and publish games
- Game engines used by professional studios
- Student game development success stories

**Tools and Platforms Overview:**
- Godot as professional, open-source game engine
- Steam, itch.io, mobile app stores for game distribution
- Game development communities and collaboration

#### Track B Experience Reflection (5 minutes)
**Rapid Assessment Survey:**
```
Track B Experience - Quick Check:

Circle your response:
1. Game development felt: Natural / Challenging but good / Overwhelming
2. Working with code + visuals was: Exciting / Okay / Difficult  
3. The projects possible seem: Very appealing / Somewhat interesting / Not for me
4. My confidence level was: High / Growing / Low but curious
5. I want to learn more about: Definitely / Maybe / Probably not

Most exciting aspect of game development:
□ Creating characters and worlds
□ Programming game logic and mechanics
□ Designing user experiences  
□ Building complete, playable projects
□ Working with professional development tools
```

---

## Day 3 (Final 30 Minutes): Informed Track Selection

### Track Choice Decision Process
**"Choose Your Programming Adventure"**

#### Individual Reflection and Decision (15 minutes)
**Personal Choice Worksheet:**

```
Track Selection Decision Guide:

Reflecting on Both Experiences:

Track A (Visual Programming) felt:
Most engaging aspect: ________________________
Most challenging aspect: ____________________
Confidence level (1-5): ____________________

Track B (Game Development) felt:  
Most engaging aspect: ________________________
Most challenging aspect: ____________________
Confidence level (1-5): ____________________

Learning Style Preference:
□ I prefer visual blocks that eliminate syntax concerns
□ I prefer professional tools even with more complexity
□ I'm equally comfortable with both approaches

Creative Interest Priority:
□ Educational apps, interactive stories, mobile development
□ Games, simulations, entertainment applications
□ I'm excited about projects in both areas

Final Decision:
I choose Track _____ because:
_____________________________________________
_____________________________________________

Backup Plan: If my first choice doesn't work out, I would be happy to try Track _____ because I learned _____________ about my learning style and interests.
```

#### Track Selection and Grouping (10 minutes)
**Confident Choice Making:**
- Students submit choice forms privately to teacher
- No peer pressure or group influence on individual decisions  
- Teacher notes any students who seem uncertain for individual conferences

#### Celebration and Preview (5 minutes)
**"Both Paths Lead to Success"**
- Emphasize that both tracks prepare equally well for AP Performance Task
- Celebrate diversity of interests and learning approaches in classroom
- Preview exciting projects ahead for both tracks
- Remind students that track choice doesn't limit future computer science opportunities

---

## Assessment and Data Collection

### **No Grades - Pure Exploration and Choice**

### Teacher Observation Data
**Track A Indicators:**
- Students who thrived with visual programming interface
- High engagement with creative, story-based projects  
- Preference for logic focus without syntax concerns
- Interest in mobile apps and educational applications

**Track B Indicators:**
- Students excited by professional development environment
- High engagement with game mechanics and interactive systems
- Comfort with increased complexity for richer project possibilities
- Interest in entertainment applications and technical challenges

### Choice Distribution Analysis
**Healthy Class Balance:**
- **Ideal:** Roughly even split between tracks (within 60-40 range)
- **If heavily skewed:** Consider individual conferences to ensure informed choice
- **Flexibility:** Allow track changes in first week if needed

### Student Confidence Tracking
**Red Flags for Additional Support:**
- Low confidence in both tracks (may need extra scaffolding)
- High anxiety about programming regardless of approach
- Difficulty engaging with hands-on exploration activities  
- Social factors influencing choice more than personal preference

---

## Materials and Setup

### Technology Requirements
- **Scratch access** for all students (scratch.mit.edu)
- **Godot installation** on classroom computers  
- **Template files** prepared for rapid game development
- **Backup activities** for technology issues

### Physical Classroom Setup
- **Flexible seating** for collaboration and exploration
- **Multiple computer stations** for peer programming  
- **Presentation area** for showcasing student work
- **Quiet reflection space** for individual decision making

### Assessment Materials
- **Reflection surveys** (digital or paper)
- **Track choice forms** for private submission
- **Teacher observation sheets** for noting student preferences
- **Parent communication** materials explaining track structure

---

## Connecting to Track Implementation

### Week 11 Transition
**Seamless Track Beginning:**
- Students enter Unit 2 with informed choice and excitement
- Track A students have Scratch confidence from sampling experience  
- Track B students understand Godot interface and game development