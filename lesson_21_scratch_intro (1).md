# Lesson 21: Introduction to Visual Programming with Scratch
**AP Computer Science Principles | Unit 2: Programming Structures - Track A**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 11
- **Unit:** Programming Structures & Computational Thinking - Track A (Visual Programming)
- **Prerequisites:** Completed Unit 1 (Web Development), Track selection completed

## Learning Targets

### I am learning to...
1. **Understand** visual programming as an approach to creating algorithms without text-based syntax barriers
2. **Analyze** how Scratch programming blocks represent fundamental programming concepts like variables, loops, and conditionals
3. **Create** my first interactive Scratch program using sprites, events, and basic programming structures

### Success Criteria - I can...
1. **Navigate** the Scratch interface confidently and explain the purpose of sprites, stage, and blocks palette
2. **Build** a functional Scratch program with user interaction using event blocks and motion commands
3. **Connect** Scratch programming concepts to AP Computer Science Principles Big Ideas and real-world applications

## AP Big Ideas Connections

### Primary Focus
- **AAP-2.A:** Express an algorithm that uses sequencing without using a programming language
  - *Connection:* Scratch blocks represent algorithmic sequences visually before text-based coding
- **AAP-2.B:** Represent a step-by-step algorithmic process using sequential code statements
  - *Connection:* Scratch scripts demonstrate sequential execution of programming instructions
- **CRD-2.A:** Describe the purpose of a computing innovation
  - *Connection:* Interactive Scratch programs solve problems and provide entertainment

### Supporting Connections
- **AAP-1.A:** Represent a value with a variable
  - *Connection:* Scratch variables store and manipulate data visually
- **CRD-1.A:** Explain how computing innovations are improved through collaboration
  - *Connection:* Scratch community sharing and remixing demonstrates collaborative development

## Materials Needed

### Technology
- Computers with reliable internet access
- Modern web browsers for accessing scratch.mit.edu
- Scratch accounts for all students (using school email addresses)
- Projection system for live demonstration

### Resources
- Scratch interface guide handout
- Programming concepts vocabulary sheet
- Example Scratch projects for inspiration
- Troubleshooting reference for common issues

### Preparation
- Create teacher Scratch account and sample projects
- Test school network access to Scratch website
- Prepare gallery of inspiring student-appropriate Scratch projects
- Set up accounts or account creation process for students

## Why Track A? Visual Programming Benefits

### Pedagogical Advantages
**Removes Syntax Barriers:** Students focus on logic and problem-solving without worrying about spelling, punctuation, or syntax errors that can frustrate beginners in text-based programming.

**Immediate Visual Feedback:** Changes in code produce immediate visual results, making cause-and-effect relationships clear and debugging more intuitive.

**Supports Different Learning Styles:** Visual, kinesthetic, and logical learners all find entry points into programming concepts through Scratch's multimedia approach.

**Builds Confidence:** Success comes quickly, building students' confidence that they CAN program and think computationally.

### Connection to AP Goals
**Same Concepts, Different Expression:** Students learn identical programming concepts (variables, loops, conditionals, procedures) but express them visually rather than textually.

**Computational Thinking Focus:** Without syntax concerns, students concentrate on algorithm design, problem decomposition, and logical reasoning - core AP computational thinking practices.

**Performance Task Preparation:** Visual programming builds the logical foundation needed for the AP Performance Task, which students can complete in any programming language.

## Lesson Structure (90 minutes)

### Warm-Up Activity (10 minutes)
**"Algorithm Challenge: Getting Dressed"**

#### Human Algorithm Practice (10 minutes)
**Setup:**
1. Ask for student volunteer to be "robot" (stands at front of room)
2. Challenge class to give step-by-step instructions for putting on a jacket
3. "Robot" follows instructions literally (common result: hilarity when steps are unclear!)

**Example Sequence:**
- Student: "Put on the jacket"
- Teacher (as robot): *Stands still* "I don't understand 'put on'"
- Students: "Pick up the jacket"
- Teacher: "Which hand? Where do I grab it? Which way should it face?"

**Teaching Points:**
- "Computers need very specific, step-by-step instructions"
- "We call these step-by-step instructions 'algorithms'"
- "Today we'll learn to give instructions to computers using Scratch"
- "Visual programming helps us focus on clear thinking rather than spelling"

**Connection to Programming:**
"Every program you'll ever write is just giving step-by-step instructions to a computer. Today we'll use pictures instead of text to make those instructions clear."

### I Do: Teacher Demonstration (25 minutes)
**"Welcome to Scratch: Programming with Pictures"**

#### Part 1: Interface Tour (8 minutes)
**Guided Interface Exploration:**

**Stage Area (top right):**
- "This is where our programs come to life"
- "Like a theater stage where sprites perform"
- "480 x 360 pixels, with coordinate system (-240 to 240, -180 to 180)"

**Sprites Pane (bottom right):**
- "Sprites are the characters and objects in our programs"
- "Every project starts with Scratch Cat sprite"
- "We can add, delete, and customize sprites"

**Blocks Palette (left side):**
- "These are our programming instructions, organized by color"
- Motion (blue), Looks (purple), Sound (pink), Events (yellow)
- Control (orange), Sensing (light blue), Operators (green), Variables (red)

**Scripts Area (center):**
- "Where we drag and connect blocks to create programs"
- "Scripts run from top to bottom"
- "Multiple scripts can run at the same time"

#### Part 2: First Program Creation (17 minutes)
**Live Coding: "Scratch Cat Says Hello"**

**Step 1: Event-Driven Programming (5 minutes)**
```scratch
// Drag these blocks and narrate process
When [green flag] clicked
say [Hello! Welcome to Computer Science!] for (2) seconds
```

**Teaching Narration:**
- "Programs need a trigger - we use 'when green flag clicked'"
- "This is called 'event-driven programming' - something happens when an event occurs"
- "The 'say' block makes our sprite communicate with users"

**Test the program:** Click green flag, celebrate that it works!

**Step 2: Adding Movement (6 minutes)**
```scratch
When [green flag] clicked
say [Hello! Welcome to Computer Science!] for (2) seconds
move (100) steps
turn clockwise (90) degrees
move (100) steps
```

**Teaching Points:**
- "Programs execute sequentially - one instruction after another"
- "We can combine different types of blocks to create complex behaviors"
- "The sprite follows our algorithm exactly"

**Step 3: Adding Interaction (6 minutes)**
```scratch
When [green flag] clicked
say [Hello! Welcome to Computer Science!] for (2) seconds
move (100) steps
turn clockwise (90) degrees
move (100) steps
ask [What is your name?] and wait
say [Nice to meet you] for (2) seconds
```

**Key Concepts Emphasized:**
- **Sequence:** Instructions happen in order
- **Input:** Programs can get information from users
- **Output:** Programs can display information to users
- **Events:** Programs respond to user actions

### We Do: Guided Practice (25 minutes)
**"Let's Build Together: Interactive Scratch Cat"**

#### Setup and Account Access (10 minutes)
**Getting Everyone Started:**
1. Navigate to scratch.mit.edu as a class
2. Guide students through account creation or login process
3. Help students create new project titled "My First Scratch Program"
4. Ensure everyone can see the interface and drag blocks

**Troubleshooting Support:**
- Check internet connectivity issues
- Help with account creation problems
- Assist with browser compatibility
- Ensure everyone reaches the programming interface

#### Collaborative Programming (15 minutes)
**Build Program Together with Student Input:**

**Teacher Facilitates, Students Contribute Ideas:**
"Let's create a program where Scratch Cat introduces our class! What should we make Scratch Cat do?"

**Suggested Collaborative Script:**
```scratch
// Build this together with student suggestions
When [green flag] clicked
say [Welcome to our Computer Science class!] for (3) seconds
ask [What grade are you in?] and wait
say [join [Cool! I love ] [answer]] for (2) seconds
glide (2) secs to x: (pick random (-200) to (200)) y: (pick random (-150) to (150))
say [Let's learn programming together!] for (2) seconds
```

**Teaching Strategies During Guided Practice:**
- **Ask for student input:** "What should Scratch Cat say next?"
- **Explain block choices:** "Why might we use 'glide' instead of 'move'?"
- **Encourage experimentation:** "What happens if we change this number?"
- **Show debugging:** Demonstrate fixing mistakes and trying different approaches

**Concepts Reinforced:**
- **Variables:** The "answer" block stores user input
- **Random numbers:** Programs can make unpredictable choices
- **Coordinates:** Understanding x/y positioning on stage
- **Timing:** Controlling how long actions take

### Break (5 minutes)
**Movement and Mental Reset**
- Stand up and stretch
- Walk around to see other students' progress
- Brief bathroom break
- Prepare for independent creative work

### You Do: Independent Practice (20 minutes)
**"Create Your Personal Scratch Introduction"**

#### Assignment Instructions
**Create a Scratch program that introduces you to others:**

**Required Programming Elements:**
1. **Event trigger:** Program starts when green flag is clicked
2. **Sprite communication:** At least 3 different "say" or "ask" blocks
3. **User interaction:** At least 1 "ask and wait" block that gets user input
4. **Movement:** Sprite moves around the stage (at least 2 movement blocks)
5. **Sequencing:** Logical order that makes sense to users

#### Creative Content Suggestions:
**Your Scratch program could:**
- Introduce yourself and ask the user questions about themselves
- Share your favorite hobbies and ask about theirs
- Tell a joke or riddle and get the user's response
- Give a tour of your favorite places (sprite moves to different locations)
- Play a simple guessing game with the user

#### Example Program Structure:
```scratch
When [green flag] clicked
say [Hi! I'm [Your Name]'s programming assistant!] for (2) seconds
ask [What's your name?] and wait
say [join [Nice to meet you, ] [answer]] for (2) seconds
say [I'm going to tell you about my creator!] for (2) seconds
glide (1) secs to x: (-100) y: (50)
say [They love [your hobby]!] for (2) seconds
glide (1) secs to x: (100) y: (-50)
ask [What's your favorite subject in school?] and wait
say [join [That's cool! ] [answer] [ sounds interesting!]] for (3) seconds
say [Thanks for chatting with me!] for (2) seconds
```

#### Differentiation Strategies

**For Advanced Students:**
- Add sound effects or music to your program
- Use costume changes to make sprite more expressive
- Try backdrop changes to create different scenes
- Experiment with different sprites beyond Scratch Cat

**For Students Needing More Support:**
- Start with provided template and modify content
- Work with partner to brainstorm ideas and test programs
- Focus on completing basic requirements before adding extras
- Use visual aids to plan program sequence before coding

**For English Language Learners:**
- Allow use of native language in sprite dialogue
- Provide vocabulary support for Scratch block names
- Partner with bilingual classmate for collaboration
- Focus on programming logic over English language perfection

### Teacher Support During Independent Work
**Circulate and Provide Just-in-Time Help:**

**Common Issues and Solutions:**
- **"My sprite isn't moving!"** → Check that movement blocks are connected to event block
- **"The program doesn't start!"** → Verify green flag event block is at the top
- **"My sprite disappeared!"** → Use "go to x: 0 y: 0" block to bring sprite back to center
- **"I don't know what to make it say!"** → Encourage personal interests, provide conversation starters

**Encouraging Phrases:**
- "I love how your sprite is moving around the stage!"
- "Great job getting user input - that makes your program interactive!"
- "Try changing that number and see what happens!"
- "Your program tells a story - that's excellent algorithm design!"

### Wrap-Up & Reflection (5 minutes)
**"Sharing Our First Scratch Creations"**

#### Quick Showcase (3 minutes)
**Celebrating Student Programs:**
1. Ask 3-4 volunteers to run their programs for the class
2. Have audience notice one thing they liked about each program
3. Encourage presenters to explain one choice they made

**Showcase Questions:**
- "What does your program do?"
- "What was your favorite part to create?"
- "What would you like to add next time?"

#### Reflection and Connection (2 minutes)
**Processing the Learning:**

**Quick Discussion:**
- **"How was programming with blocks different from what you expected?"**
- **"What programming concepts did you use today?"** (sequence, input, output, events)
- **"How is Scratch similar to the HTML and CSS we learned before?"**

**Key Connections to Emphasize:**
- "You created algorithms - step-by-step instructions for solving problems"
- "Your programs demonstrated computational thinking - breaking down problems into steps"
- "Visual programming uses the same concepts as text programming, just expressed differently"
- "These same ideas will help you with the AP Performance Task later this year"

## Assessment

### Formative Assessment (During Class)
**Participation and Understanding Checklist:**
- [ ] Student successfully navigates Scratch interface
- [ ] Student creates functional program with required elements
- [ ] Student demonstrates understanding of block connections and sequencing
- [ ] Student experiments with different blocks and observes results
- [ ] Student seeks help appropriately and helps others when possible

### Summative Assessment (End of Class)
**Personal Scratch Introduction Program Rubric:**

**4 - Exemplary Programming (Exceeds Expectations):**
- Creative and engaging program that clearly introduces student
- All required elements present plus additional creative features
- Excellent use of Scratch blocks with smooth, logical flow
- Evidence of experimentation and iteration in program design
- Program demonstrates strong grasp of sequencing and user interaction

**3 - Proficient Programming (Meets Expectations):**
- Clear and appropriate introduction program with personal touches
- All required programming elements present and functional
- Good use of Scratch blocks with logical sequence
- Program runs smoothly with appropriate user interaction
- Demonstrates solid understanding of basic programming concepts

**2 - Developing Programming (Approaching Expectations):**
- Basic introduction program with minimal personalization
- Most required elements present but may have minor functionality issues
- Adequate use of Scratch blocks but sequence could be improved
- Program runs but user interaction may be limited
- Shows understanding of concepts but needs more practice

**1 - Beginning Programming (Below Expectations):**
- Minimal program with limited introduction content
- Missing several required programming elements
- Poor use of Scratch blocks with functionality problems
- Program may not run properly or lacks user interaction
- Limited understanding of programming concepts evident

### Exit Ticket Assessment
**Quick Learning Check (2 minutes):**

**Complete these sentences:**
1. **Today I learned that programming with Scratch is...**
2. **One thing I want to improve in my next Scratch program is...**
3. **The most challenging part of visual programming was...**

**Teacher Use of Exit Tickets:**
- Identify students who need additional support with interface
- Plan tomorrow's lesson based on confidence levels and interests
- Note misconceptions that need addressing in future lessons

## Homework/Extension Activities

### For All Students (Optional)
**"Scratch Exploration":**
- Explore the Scratch community website and try 3 different projects made by other students
- Think about what makes some programs more engaging than others
- Write 2-3 sentences about ideas you might want to try in future programs

### For Students Wanting More Challenge
**"Advanced Scratch Features":**
- Research and try using sound blocks to add audio to your program
- Experiment with costume changes to make your sprite more expressive
- Try creating a simple animation using the "repeat" block
- Look up Scratch tutorials for features we didn't cover today

### For Students Needing More Practice
**"Scratch Fundamentals Review":**
- Practice dragging and connecting different types of blocks
- Try modifying the numbers in your program and observe what changes
- Create a simple program with just movement blocks to practice sprite control

## Next Lesson Preview
**"Tomorrow: Variables and Data in Scratch"**

**Exciting Preview:**
- Show Scratch program that remembers user's name throughout interaction
- Demonstrate score keeping in a simple game
- "Variables let programs remember information and make decisions based on data"

**What Students Will Learn:**
- Creating and using variables to store information
- Connecting variables to user input and program output
- Understanding how programs use data to make decisions
- Building more sophisticated interactive experiences

## Materials for Next Lesson

### Teacher Preparation
- Scratch programs demonstrating variable usage in different contexts
- Examples showing score keeping, name storage, and user preferences
- Connection between Scratch variables and AP Data abstraction concepts
- Troubleshooting guide for common variable-related issues

### Student Readiness
- Comfort with basic Scratch interface and block manipulation
- Understanding of program sequencing and user interaction
- Completed introduction program to build upon
- Enthusiasm for making programs more sophisticated and personalized

## Cross-Curricular Connections

### Mathematics
**Coordinate System:** Scratch stage uses x/y coordinates, reinforcing graphing concepts
**Random Numbers:** Programs use mathematical randomness for unpredictable behaviors
**Logical Sequences:** Programming reinforces step-by-step problem-solving approaches

### Language Arts
**Storytelling:** Scratch programs can tell interactive stories with user choices
**Communication:** Programs must communicate clearly with users through text and actions
**Creative Writing:** Students express personality and interests through program content

### Art and Design
**Visual Design:** Sprite selection and stage design involve aesthetic choices
**Animation Principles:** Movement and timing create visual appeal and user engagement
**User Experience:** Good programs consider how users will interact with content

## Professional Development Notes for Teachers

### Teaching Visual Programming Effectively

**Key Pedagogical Strategies:**
- **Model thinking process:** Narrate your problem-solving approach while live coding
- **Encourage experimentation:** "What happens if we change this?" mindset
- **Celebrate debugging:** Frame errors as information rather than failure
- **Connect to real programming:** Regularly connect Scratch concepts to professional programming

**Common Student Misconceptions:**
- **"Scratch isn't 'real' programming"** → Emphasize that concepts transfer to all languages
- **"Visual programming is easier"** → Acknowledge that logic and problem-solving are still challenging
- **"Blocks limit creativity"** → Show examples of sophisticated Scratch programs and games

### Assessment in Visual Programming

**Focus on Computational Thinking:**
- Problem decomposition and algorithm design
- Pattern recognition and abstraction
- Testing and debugging systematic approaches
- Creative problem-solving and iteration

**Document Learning Growth:**
- Screenshot programs at different stages of development
- Collect student reflections on problem-solving processes
- Note collaboration and peer learning moments
- Track progression from simple to complex program structures

---

**Congratulations! Your Track A students have taken their first steps into the world of programming logic and computational thinking. Through Scratch's visual approach, they've experienced the joy of creating interactive programs while building the foundational concepts they'll need for more advanced programming and the AP Performance Task. 🚀**

**Next up: Variables and data management - the building blocks of sophisticated programming logic!**