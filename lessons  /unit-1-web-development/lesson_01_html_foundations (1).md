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
<body>
    <h1>Hello! I'm [Student Name]</h1>
    
    <h2>About Me</h2>
    <p>I'm a [grade level] student who loves [interests]. I decided to take computer science because [reason].</p>
    
    <p>Some things you should know about me: [personal details appropriate for school].</p>
    
    <p>I'm excited to learn programming because [goals/interests].</p>
    
    <h2>My Favorite Things</h2>
    <ul>
        <li>Favorite subject: [subject]</li>
        <li>Favorite hobby: [hobby]</li>
        <li>Favorite app/website: [technology]</li>
        <li>Dream job: [career aspiration]</li>
    </ul>
</body>
</html>
```

#### Teacher Support During Independent Work
**Circulate and Provide Just-in-Time Help:**

**Common Issues and Responses:**
- **"My page is blank!"** → Check for missing closing tags, especially `</body>` and `</html>`
- **"The title doesn't show!"** → Ensure `<title>` is inside `<head>` section
- **"My list doesn't look right!"** → Verify `<li>` items are inside `<ul>` or `<ol>` container
- **"I don't know what to write!"** → Provide content prompts and encourage creativity

**Encouraging Phrases:**
- "Great start! I can see you understand the structure."
- "That's an interesting way to organize your content!"
- "Remember, there's no 'perfect' content - just make it yours."
- "What would you want someone to know about you?"

#### Differentiation Strategies
**For Advanced Students:**
- Add additional semantic elements like `<section>` or `<article>`
- Include contact information using appropriate formatting
- Research and add meta description for SEO practice

**For Struggling Students:**
- Provide template with blanks to fill in
- Work one-on-one to ensure basic structure is correct
- Focus on completing required elements before adding extras

**For English Language Learners:**
- Allow use of native language for content (HTML structure is the focus)
- Provide vocabulary support for HTML terms
- Partner with bilingual peer for content brainstorming

### Wrap-Up & Reflection (10 minutes)
**"Celebrating Our First Websites!"**

#### Gallery Walk (5 minutes)
**Sharing Student Work:**
1. Students save their work and step away from computers
2. Rotate around room viewing each other's introduction pages
3. Leave positive sticky note comments on desks
4. Return to own seats for discussion

**Gallery Walk Prompts:**
- "What did you learn about your classmates?"
- "What creative approaches did you notice?"
- "What HTML elements did others use effectively?"

#### Reflection Discussion (5 minutes)
**Whole Class Processing:**

**Discussion Questions:**
1. **"What surprised you about creating a webpage?"**
   - *Expected responses:* It was easier/harder than expected, immediate results were satisfying
2. **"What was challenging about HTML?"**
   - *Expected responses:* Remembering closing tags, structure organization
3. **"How is HTML similar to or different from what you expected programming to be?"**
   - *Expected responses:* More like organizing than calculating, visual results

**Key Takeaways to Emphasize:**
- "You all created functional websites in your first class - that's amazing!"
- "HTML is about structure and organization, like outlining an essay"
- "Every website you've ever visited started with HTML like this"
- "We'll add styling and interactivity in upcoming lessons"

## Assessment

### Formative Assessment (During Class)
**Observation Checklist:**
- [ ] Student successfully creates Neocities account
- [ ] Student demonstrates understanding of HTML tag structure
- [ ] Student participates appropriately in guided practice
- [ ] Student attempts independent work with reasonable effort
- [ ] Student seeks help when needed and offers help to others

### Summative Assessment (End of Class)
**Introduction Page Requirements Rubric:**

**4 - Exemplary (Exceeds Expectations):**
- Perfect HTML document structure with all required elements
- Creative and appropriate content that shows personality
- Additional HTML elements beyond requirements (semantic tags, etc.)
- Clean, organized code with proper indentation

**3 - Proficient (Meets Expectations):**
- Correct HTML document structure with all required elements
- Appropriate content that introduces student effectively
- All required elements present and functional
- Code is functional with minor formatting issues

**2 - Developing (Approaching Expectations):**
- HTML document structure mostly correct with minor errors
- Content is appropriate but may be minimal or unclear
- Most required elements present but may have issues
- Code functions but has organizational or syntax problems

**1 - Beginning (Below Expectations):**
- HTML document structure has significant errors
- Content is inappropriate, minimal, or unclear
- Missing several required elements
- Code has major functionality issues

### Exit Ticket
**Quick Check for Understanding (2 minutes):**

**On paper or digital form:**
1. **One thing I learned today:** _________________________
2. **One thing I'm still confused about:** _________________
3. **One thing I want to try tomorrow:** ___________________

**Teacher Use:**
- Identify concepts that need reteaching
- Plan individual support for struggling students
- Adjust pacing for next lesson based on understanding

## Homework/Extension
**Optional Practice (Not Required):**

### For All Students
- **Explore:** Look at 2-3 of your favorite websites and try to identify HTML elements we learned today
- **Reflect:** Write 2-3 sentences about how creating a webpage felt different from other school assignments

### For Students Wanting More Challenge
- **Research:** Look up 3 new HTML elements we didn't cover and try adding them to your page
- **Create:** Add more content to your introduction page using elements we learned

### For Students Needing More Practice
- **Review:** Use the HTML reference sheet to review elements we used today
- **Practice:** Create a simple HTML page about your favorite movie, book, or hobby

## Next Lesson Preview
**"Tomorrow we'll learn CSS - making our websites beautiful!"**

**Quick Preview:**
- Show example of same HTML content with and without CSS styling
- "HTML is the skeleton, CSS is the clothing and decoration"
- Students will add colors, fonts, and layouts to their introduction pages

## Materials for Next Lesson
**Teacher Preparation:**
- CSS examples showing dramatic before/after transformations
- Color theory basics and web-safe color resources
- CSS syntax practice exercises
- Connection between CSS selectors and HTML elements

**Student Needs:**
- Completed introduction page from today (saved on Neocities)
- Continued access to computers and internet
- Willingness to experiment with visual design

## Reflection for Teacher Growth

### What Went Well?
**After teaching, reflect on:**
- Which students seemed most engaged and why?
- What explanations were clearest for student understanding?
- How did the pacing work for the 90-minute block?
- What student questions revealed good thinking or confusion?

### What to Adjust?
**For future iterations:**
- Did students need more/less time for independent practice?
- Were there concepts that needed additional explanation?
- How could the gallery walk be improved for better sharing?
- What technology issues arose and how can they be prevented?

### Student Feedback to Collect
**In next lesson, ask:**
- "What from yesterday's HTML lesson is still unclear?"
- "What would have helped you learn better yesterday?"
- "What are you excited to learn next?"

## Additional Resources

### For Teachers
- **W3Schools HTML Tutorial:** Comprehensive reference with examples
- **MDN Web Docs:** Professional-level documentation and guides
- **Can I Use:** Browser compatibility checking for HTML elements
- **HTML Validator:** W3C tool for checking code correctness

### For Students
- **Codecademy HTML Course:** Interactive practice exercises
- **freeCodeCamp:** Project-based HTML learning
- **Khan Academy Intro to HTML:** Video-based lessons
- **HTML Dog:** Beginner-friendly tutorials and reference

### Extension Opportunities
- **Web Accessibility:** Introduction to screen readers and inclusive design
- **HTML History:** Evolution from HTML 1.0 to HTML5
- **Career Connections:** Web developer interviews or virtual field trips
- **Cross-Curricular:** HTML pages for other subject projects

## Standards Alignment

### AP Computer Science Principles Big Ideas
- **CRD-2:** Program design and development through webpage creation
- **IOC-1:** Computing innovations (websites) and their societal impact
- **DAT-1:** Data representation through HTML markup structure

### Computational Thinking Practices
1. **Computational Solution Design:** Planning webpage structure and content
2. **Algorithms and Program Development:** Systematic HTML document creation
3. **Abstraction:** Understanding HTML as abstraction layer over browser rendering
4. **Code Analysis:** Debugging HTML structure and validating syntax

### 21st Century Skills
- **Creativity:** Personal expression through webpage design and content
- **Communication:** Sharing personal information appropriately online  
- **Collaboration:** Peer feedback and shared learning experiences
- **Digital Citizenship:** Understanding website creation as form of publishing

---

**Welcome to the exciting world of web development! Today your students took their first steps into creating digital content that can be shared with the world. Every professional web developer started exactly where your students are now - with their first HTML page. 🌐**

**Next Up:** Lesson 02 - CSS Styling Fundamentals - Making Websites Beautiful!
