# Lesson 03: JavaScript Foundations - Variables and Simple Interactions
**AP Computer Science Principles | Unit 1: Web Development & Digital Expression (Beginner-Optimized)**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 2
- **Unit:** Web Development & Digital Expression
- **Prerequisites:** Lessons 01-02 (HTML, CSS) + CS Discovery Week completed

## Learning Targets

### I am learning to...
1. **Understand** JavaScript as a programming language that adds behavior to web pages using variables and simple functions
2. **Analyze** how variables store information that programs can remember and use for personalization
3. **Create** basic interactive web pages using JavaScript variables, user input, and simple display changes

### Success Criteria - I can...
1. **Explain** what variables are and give examples of how they store information in programs with proper terminology
2. **Create** JavaScript variables that store different types of information (text, numbers, true/false)
3. **Build** a simple interactive webpage that uses variables to remember and display user information

## Beginner-Friendly Approach

### **Building on Discovery Week Experience**
Students already understand:
- **Algorithms** are step-by-step instructions (from human algorithm activities)
- **Variables** store information (from binary number games)
- **Debugging** is normal problem-solving (from logic puzzles)
- **Programming is creative** and collaborative

### **Gentle JavaScript Introduction Philosophy**
- **Start with concepts they know:** Variables work like labeled boxes
- **Use familiar contexts:** Web pages they can see and share
- **Build confidence first:** Success before complexity
- **Connect to prior learning:** "This is like what we did in Discovery Week, but with code"

## AP Big Ideas Connections

### Primary Focus
- **AAP-1.A:** Represent a value with a variable
  - *Connection:* JavaScript variables store different data types just like human memory
- **AAP-2.B:** Represent a step-by-step algorithmic process using sequential code statements
  - *Connection:* JavaScript functions execute instructions in order like human algorithms
- **CRD-2.C:** Identify input(s) to a program
  - *Connection:* Programs get information from users through prompts and interactions

### Supporting Connections
- **CRD-2.D:** Identify output(s) produced by a program
  - *Connection:* JavaScript displays results on web pages for users to see

## Materials Needed

### Technology
- Computers with completed HTML/CSS pages from Lessons 01-02
- Web browsers with developer console access (for debugging)
- Visual Studio Code or Neocities editor
- Simple text editor for code practice

### Resources
- **Variable concept visual aids** (boxes, labels, storage metaphors)
- **JavaScript syntax reference sheet** (simplified for beginners)
- **"Debugging is normal" growth mindset posters**
- **Success celebration materials** (progress tracking, achievement recognition)

### Preparation
- Review Discovery Week observations about student confidence levels
- Prepare extra scaffolding materials for anxious students
- Set up debugging examples that show mistakes are learning opportunities
- Plan individual check-ins for students who need extra support

## Lesson Structure (90 minutes)

### Warm-Up Activity (10 minutes)
**"Variables in Real Life" Connection Game**

#### Part 1: Physical Variable Review (5 minutes)
**Callback to Discovery Week:**
- "Remember our human variables from Discovery Week?"
- Ask 3 volunteers to be variables again: "StudentName," "FavoriteColor," "EnergyLevel"
- Class assigns values, changes them, uses them in sentences

**Example Interaction:**
- "StudentName, your value is Maria"
- "FavoriteColor, your value is purple"  
- "EnergyLevel, your value is excited"
- "Now let's make a sentence: [StudentName] loves the color [FavoriteColor] and feels [EnergyLevel] about learning!"

#### Part 2: Connect to JavaScript (5 minutes)
**Bridge to Digital Variables:**
- "JavaScript variables work exactly the same way - they're labeled containers that store information"
- "Today we'll learn to create digital variables that remember information about our website visitors"
- "The thinking is the same as Discovery Week - we're just writing it in code now"

### I Do: Teacher Demonstration (25 minutes)
**"My First JavaScript Variables - Step by Step"**

#### Part 1: Simple Variables and Alerts (12 minutes)

**Ultra-Beginner Start:**
```javascript
// Start with the simplest possible example
var myName = "Ms. Johnson";
alert("Hello from " + myName);
```

**Live Coding with Narration:**
- "First, I create a variable called 'myName' and store my name in it"
- "The word 'var' tells JavaScript 'I'm making a new variable'"
- "The equals sign stores information in the variable"
- "The alert shows a message with my stored information"

**Immediate Test:**
- Save file, refresh browser, see alert
- "It works! We just created our first JavaScript variable!"

**Build Gradually:**
```javascript
// Add more variables step by step
var myName = "Ms. Johnson";
var mySubject = "Computer Science";
var todaysDate = "Monday";

alert("Hello! I'm " + myName);
alert("I teach " + mySubject);  
alert("Today is " + todaysDate);
```

**Key Teaching Points:**
- "Variables are like labeled boxes that store information"
- "We can combine text with variables using the + sign"
- "Each variable remembers its information until we change it"

#### Part 2: User Input with Prompts (13 minutes)

**Interactive Variables:**
```javascript
// Now let's get information FROM the user
var visitorName = prompt("What's your name?");
alert("Nice to meet you, " + visitorName + "!");

var visitorAge = prompt("How old are you?");
alert("Wow, " + visitorAge + " is a great age!");

var visitorHobby = prompt("What's your favorite hobby?");
alert(visitorName + " likes " + visitorHobby + " - that's awesome!");
```

**Teaching Narration:**
- "The 'prompt' command asks the user a question and stores their answer"
- "Now our variables contain personalized information about each visitor"
- "Notice how we can use multiple variables together to create custom messages"

**Live Demo:**
- Run the code and interact with prompts
- Show how different answers create different results
- "This is personalization - the program adapts to each user!"

**Connection to Discovery Week:**
"Remember how we gave step-by-step instructions to make a sandwich? This is the same thinking - step-by-step instructions for getting and using information!"

### We Do: Guided Practice (25 minutes)
**"Let's Build a Personal Greeting Page Together"**

#### Setup and Planning (10 minutes)
**Collaborative Design:**
1. Students suggest what personal information would make a website more welcoming
2. Class votes on 3-4 pieces of information to collect from visitors
3. Together, plan the structure of our greeting program

**Example Student Suggestions:**
- Name, favorite color, dream vacation, favorite food, grade level, pets, etc.

**Chosen Information (Student-Driven):**
- Visitor's name
- Favorite color  
- Something that makes them happy
- What they want to learn in this class

#### Implementation Session (15 minutes)
**Build Together Step by Step:**

```javascript
// Step 1: Create our variables (students suggest names)
var visitorName;
var favoriteColor;  
var happyThing;
var learningGoal;

// Step 2: Get information from visitor (students suggest questions)
visitorName = prompt("Hi! What's your name?");
favoriteColor = prompt("What's your favorite color?");
happyThing = prompt("What's one thing that always makes you smile?");
learningGoal = prompt("What do you hope to learn in computer science class?");

// Step 3: Create personalized messages (students help write)
alert("Welcome, " + visitorName + "!");
alert("I love that your favorite color is " + favoriteColor + "!");
alert("It's wonderful that " + happyThing + " makes you happy!");
alert("I'm excited to help you learn about " + learningGoal + "!");

// Step 4: Create final welcome message
alert("Thanks for visiting, " + visitorName + "! This page is now personalized just for you!");
```

**Teaching Strategies During We Do:**
- **Students drive content:** "What question should we ask about hobbies?"
- **Explain every step:** "Why do we create the variables first before storing information?"
- **Test immediately:** Run code after each addition
- **Celebrate discoveries:** "Great idea! That question will give us interesting information!"

### Break (5 minutes)
**Movement and Confidence Building**
- Stand up and stretch
- Quick partner sharing: "What's one thing you understand about variables?"
- Mental preparation for independent practice

### You Do: Independent Practice (20 minutes)
**"Create Your Personal Variable Story"**

#### Assignment Instructions
**Build a JavaScript program that uses variables to create a personalized experience:**

**Required Elements (Gentle Requirements):**
1. **At least 3 variables** with meaningful names
2. **User input** using prompt() to get information from visitors
3. **Personalized output** using alert() to display custom messages
4. **Text combination** using + to join variables with other text
5. **Logical flow** that makes sense to someone using your program

#### Beginner-Friendly Project Ideas:

**Ultra-Beginner Level:**
```javascript
// Simple introduction collector
var userName = prompt("What's your name?");
var userAge = prompt("What's your age?");
alert("Hello " + userName + "! Being " + userAge + " is awesome!");
```

**Comfortable Beginner Level:**
```javascript
// Personal profile builder
var name = prompt("Your name?");
var school = prompt("What school do you go to?");
var subject = prompt("What's your favorite subject?");
var future = prompt("What do you want to be when you grow up?");

alert("Meet " + name + "!");
alert(name + " goes to " + school);
alert("Their favorite subject is " + subject);  
alert("Someday " + name + " wants to be " + future);
alert("Thanks for sharing, " + name + "!");
```

**Confident Beginner Level:**
```javascript
// Dream vacation planner
var travelerName = prompt("What's your name?");
var dreamPlace = prompt("Where would you love to visit?");
var activity = prompt("What would you do there?");
var companion = prompt("Who would you travel with?");
var duration = prompt("How many days would you stay?");

alert("✈️ " + travelerName + "'s Dream Vacation ✈️");
alert("Destination: " + dreamPlace);
alert("Main activity: " + activity);
alert("Travel buddy: " + companion);
alert("Trip length: " + duration + " amazing days!");
alert("Start saving up, " + travelerName + " - this trip will be incredible!");
```

### Teacher Support During Independent Work
**Extra Scaffolding for True Beginners:**

**Common Beginner Issues and Gentle Solutions:**
- **"I don't know what to write!"** → "What's something interesting about yourself? Let's ask visitors about that!"
- **"My code doesn't work!"** → "Let's check together - programming is like debugging puzzles from Discovery Week!"
- **"This is too hard!"** → "You're learning something completely new - that feels hard at first! Let's start with just one variable."
- **"I don't understand variables!"** → "Remember our human variables? This is the same idea - a container with a label that holds information."

**Confidence-Building Support:**
- **Individual check-ins** with anxious students
- **Partner support** pairing confident students with those who need encouragement
- **Process celebration:** "Great job asking the user a question! Now let's see what happens when you store their answer."
- **Growth mindset reinforcement:** "You're figuring out how programmers think - this takes practice!"

#### Differentiation for All Beginner Levels

**For Anxious Beginners:**
- Provide template with blanks to fill in
- Work one-on-one to complete one variable successfully before adding more
- Focus on understanding concepts rather than typing speed
- Celebrate every small success: "You created a variable! That's real programming!"

**For Confident Beginners:**
- Encourage creative themes and interesting questions
- Show how to add more variables for richer personalization
- Connect to websites they use: "This is how your favorite apps remember your preferences!"
- Offer extension: "Can you make the messages different depending on what the user answers?"

**For Students with Some Experience:**
- Challenge them to help classmates without doing the work for them
- Encourage more complex text combinations and creative output
- Suggest using variables in mathematical calculations
- Preview: "Tomorrow we'll learn to put this information on the actual webpage instead of just alerts"

### Wrap-Up & Assessment (5 minutes)
**"Variable Victory Celebration"**

#### Quick Success Sharing (3 minutes)
**Showcase Beginner Achievements:**
1. Ask 3-4 volunteers to run their programs and show the personalization
2. Focus on celebrating the learning process: "What was challenging but you figured it out?"
3. Audience gives encouragement: "I liked how your program asked about..."

#### Confidence Building Reflection (2 minutes)
**Processing the Programming Success:**

**Quick Share (no pressure):**
- "One thing I'm proud of from today's programming..."
- "One thing that makes more sense now than it did an hour ago..."
- "One thing I want to try next time..."

**Key Confidence Messages:**
- "You all created real JavaScript programs that work!"
- "Variables are a fundamental programming concept you now understand!"
- "The thinking you used today is the same thinking professional programmers use!"
- "Tomorrow we'll put your variables to work on your actual web pages!"

## Assessment

### Formative Assessment (Pure Learning Focus)
**Beginner Progress Checklist - No Grades, Just Growth:**
- [ ] **Variable Understanding:** Student can explain variables as containers for information
- [ ] **Syntax Awareness:** Student recognizes basic JavaScript structure (var, =, prompt, alert)
- [ ] **Problem-Solving Approach:** Student attempts debugging with systematic thinking
- [ ] **Creative Application:** Student makes personal choices about program content
- [ ] **Collaboration:** Student seeks help appropriately and helps others when possible

### Confidence Assessment (More Important Than Technical)
**How Students Feel About Programming:**
- **Growth Mindset Evidence:** "I can learn this even though it's challenging"
- **Debugging Attitude:** "Errors give me information about what to fix"
- **Creative Ownership:** "I can make this program express my ideas"
- **Community Connection:** "I can learn from and help my classmates"

### **No Traditional Grades - Success Indicators:**
- **Attempted the assignment** with genuine effort
- **Asked questions** when confused rather than giving up
- **Helped classmates** or accepted help graciously
- **Showed growth** from start to finish of lesson
- **Expressed curiosity** about next steps or extensions

## Homework/Extension Activities

### For All Students (Gentle Encouragement)
**"Variables Around You":**
- Notice 3 apps or websites that seem to "remember" information about you
- Think about what variables those programs might use (your name, preferences, history)
- Write 2-3 sentences about how personalization makes those apps/sites more useful

### For Students Wanting More Practice
**"Variable Exploration":**
- Try changing the variable names in your program - do they still work?
- Add one more variable and question to make your program even more personalized
- Think of creative themes for variable programs (favorite foods, dream jobs, perfect day, etc.)

### For Students Who Need Confidence Building
**"Programming Success Reflection":**
- Write about one specific moment when something "clicked" for you today
- Identify one classmate who helped you learn something
- Think of one question you want to ask tomorrow to understand something better

## Next Lesson Preview
**"Tomorrow: Putting Variables on Your Webpage - Real Web Programming!"**

**Exciting Preview:**
- Take variables out of alert boxes and put them directly on web pages
- Learn how JavaScript changes HTML content dynamically
- Connect to the websites from Lessons 01-02 with personalized content

**What Students Will Learn:**
- Document.getElementById() to change webpage content
- Connecting JavaScript to HTML elements
- Creating truly interactive web pages that respond to user input
- The bridge between variables and visible web page changes

## Materials for Next Lesson

### Teacher Preparation
- Review which students need extra support with JavaScript syntax
- Prepare HTML templates that students can modify with JavaScript
- Plan individual conferences for students who struggled today
- Set up examples connecting variables to actual webpage elements

### Student Readiness
- Basic understanding that variables store information
- Experience with prompt() and alert() for user interaction
- Confidence that they can learn programming concepts
- Excitement about making their web pages more interactive

## Connection to Overall Curriculum

### **Building Toward Unit 2 Track Selection**
Today's experience with variables prepares students for:
- **Track A:** Scratch variables work exactly the same way
- **Track B:** Game development uses variables for player stats, scores, etc.
- **Both tracks:** Understanding that all programming involves storing and using information

### **Foundation for AP Performance Task**
Variable mastery is essential for:
- **Data abstraction** requirements in the Performance Task
- **Program functionality** that stores and processes information
- **User interaction** that creates personalized experiences
- **Professional programming practices** that will impress AP graders

---

**🌟 Success! Your absolute beginner students have now created their first real JavaScript programs using variables - the fundamental building block of all programming. They understand that programming is creative problem-solving, and they have the confidence to tackle more complex concepts.**

**Tomorrow they'll connect these variables to their actual web pages, creating truly dynamic and personalized websites! 🚀✨**