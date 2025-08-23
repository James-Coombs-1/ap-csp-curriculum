# Lesson 01: HTML Foundations - Introduction to Web Development
**AP Computer Science Principles | Unit 1: Web Development & Digital Expression**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 1
- **Unit:** Web Development & Digital Expression
- **Prerequisites:** None - designed for complete beginners

## Learning Targets

### I am learning to...
1. **Understand** HTML as a markup language for structuring web content and connecting to AP Big Idea: Creative Development
2. **Analyze** how web browsers interpret HTML code to create visual displays for users
3. **Create** my first functional webpage using semantic HTML elements and proper document structure

### Success Criteria - I can...
1. **Explain** the difference between markup languages and programming languages with 80% accuracy
2. **Identify** essential HTML document structure elements (doctype, html, head, body) in any webpage
3. **Build** a complete HTML document with proper semantics that validates and displays correctly in browsers

## AP Big Ideas Connections

### Primary Focus
- **CRD-2.A:** Describe the purpose of a computing innovation
  - *Connection:* Websites are computing innovations that solve communication and information sharing problems
- **CRD-2.B:** Explain how a program or code segment functions
  - *Connection:* HTML code segments create structured content that browsers interpret and display

### Supporting Connections
- **IOC-1.A:** Explain how an effect of a computing innovation can be both beneficial and harmful
  - *Connection:* Introduction to how websites impact society, economy, and culture

## Materials Needed

### Technology
- Computers with internet access
- Modern web browser (Chrome, Firefox, Safari)
- Access to Neocities.org (free web hosting platform)
- Visual Studio Code or similar text editor

### Resources
- HTML element reference sheet (provided)
- Sample webpage examples for analysis
- Validation tools (W3C HTML Validator)

### Preparation
- Create teacher Neocities account for demonstration
- Test school internet access to all required websites
- Prepare example HTML files for live coding
- Set up projection system for live demonstrations

## Lesson Structure (90 minutes)

### Warm-Up Activity (10 minutes)
**"What Makes a Good Website?" Discussion**

**Teacher Instructions:**
1. Display 3-4 different websites on the projector (mix of good and poor examples)
2. Ask students to identify what makes each site effective or ineffective
3. Guide discussion toward structure, organization, and clarity

**Discussion Prompts:**
- "What do you notice about how information is organized?"
- "Which site would be easiest to navigate? Why?"
- "What elements do all websites seem to have in common?"

**Expected Outcomes:**
- Students begin thinking about information structure
- Introduction to concepts of headers, navigation, content areas
- Connection to upcoming HTML structural elements

### I Do: Teacher Demonstration (20 minutes)
**"Building Our First Webpage Together"**

#### Part 1: Introduction to HTML (8 minutes)
**Live Coding Setup:**
- Open Visual Studio Code with blank document
- Explain HTML as "markup language" vs "programming language"
- Demonstrate browser interpretation by showing raw HTML vs rendered page

**Key Teaching Points:**
```html
<!-- Explain each element as you type -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
</head>
<body>
    <h1>Welcome to Computer Science!</h1>
    <p>This is my first webpage.</p>
</body>
</html>
```

**Narration While Coding:**
- "HTML uses 'tags' to tell the browser how to structure content"
- "Every tag has an opening `<tag>` and closing `</tag>`"
- "The browser reads this code and creates what we see on screen"

#### Part 2: Document Structure Deep Dive (12 minutes)
**Explain Each Section:**

**Document Declaration:**
```html
<!DOCTYPE html>
```
- "Tells browser this is an HTML5 document"
- "Like a label on a file folder"

**HTML Root Element:**
```html
<html lang="en">
```
- "Contains everything else"
- "Language attribute helps screen readers and translation tools"

**Head Section:**
```html
<head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
</head>
```
- "Information about the page, not displayed content"
- "Title appears in browser tab"
- "Charset ensures proper character display"

**Body Section:**
```html
<body>
    <h1>Welcome to Computer Science!</h1>
    <p>This is my first webpage.</p>
</body>
```
- "All visible content goes here"
- "Headings and paragraphs are basic building blocks"

### We Do: Guided Practice (25 minutes)
**"Let's Build Together" - Collaborative HTML Creation**

#### Setup (5 minutes)
**Getting Started on Neocities:**
1. Navigate to neocities.org as a class
2. Walk through account creation process
3. Explain free hosting concept and why we're using this platform
4. Demonstrate accessing the HTML editor

#### Collaborative Building (20 minutes)
**Create Class Website Together:**

**Teacher Facilitates, Students Contribute:**
"What should we put on our class website? Let's build it together!"

**Example Structure (built with student input):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mr./Ms. [Name]'s Computer Science Class</title>
</head>
<body>
    <!-- Students suggest content for each section -->
    <h1>Welcome to Our Computer Science Adventure!</h1>
    
    <h2>About This Class</h2>
    <p>We are learning to create amazing things with code!</p>
    
    <h2>What We're Learning</h2>
    <p>HTML, CSS, JavaScript, and how to solve problems with code.</p>
    
    <h2>Our Goals</h2>
    <ul>
        <li>Create our own websites</li>
        <li>Learn to think like programmers</li>
        <li>Have fun building cool stuff!</li>
    </ul>
    
    <h2>Meet the Students</h2>
    <p>We are a diverse group of creative problem-solvers!</p>
</body>
</html>
```

**Teaching Strategies During We Do:**
- **Ask for student input:** "What should our heading say?"
- **Explain choices:** "Why might we use an h2 instead of h1 here?"
- **Encourage participation:** "Who has an idea for our list?"
- **Show immediate results:** Refresh browser to see changes

### Break (5 minutes)
**Physical Movement and Reset**
- Stand and stretch
- Optional: quick energizer activity
- Bathroom breaks
- Prepare for independent work

### You Do: Independent Practice (20 minutes)
**"Create Your Personal Introduction Page"**

#### Assignment Instructions
**Create your own HTML page with:**

**Required Elements:**
1. **Proper document structure** (DOCTYPE, html, head, body)
2. **Meaningful page title** in the head section
3. **Main heading (h1)** with your name or creative title
4. **At least 3 paragraphs** introducing yourself
5. **One subheading (h2 or h3)** organizing your content
6. **One list** (ordered or unordered) showing interests, goals, or favorites

**Content Suggestions:**
- Your name and something interesting about you
- Why you're taking this computer science class
- Your interests, hobbies, or favorite things
- Goals for this class or future plans
- Anything else you'd like to share appropriately

#### Example Structure (Student Choice):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>[Student Name] - Introduction</title>
</head>
<body
