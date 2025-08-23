# Lesson 02: CSS Styling Fundamentals - Making Websites Beautiful
**AP Computer Science Principles | Unit 1: Web Development & Digital Expression**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 1 
- **Unit:** Web Development & Digital Expression
- **Prerequisites:** Lesson 01 - HTML Foundations completed

## Learning Targets

### I am learning to...
1. **Understand** CSS as a styling language that controls visual presentation separate from HTML structure
2. **Analyze** how CSS selectors target HTML elements to apply consistent visual formatting
3. **Apply** CSS properties to transform plain HTML into visually appealing and accessible web pages

### Success Criteria - I can...
1. **Explain** the separation of concerns between HTML (structure) and CSS (presentation) with specific examples
2. **Write** CSS rules using proper syntax including selectors, properties, and values
3. **Style** my introduction webpage using colors, fonts, spacing, and layout to create an engaging user experience

## AP Big Ideas Connections

### Primary Focus
- **CRD-2.F:** Design a program and its user interface
  - *Connection:* CSS enables user-focused design that considers aesthetics and accessibility
- **CRD-2.B:** Explain how a program or code segment functions  
  - *Connection:* CSS rules function as instructions that browsers interpret to render visual designs

### Supporting Connections
- **CRD-1.A:** Explain how computing innovations are improved through collaboration
  - *Connection:* CSS enables designers and developers to work together effectively
- **IOC-1.A:** Explain beneficial and harmful effects of computing innovations
  - *Connection:* CSS can improve accessibility but can also create barriers for some users

## Materials Needed

### Technology
- Computers with completed HTML introduction pages from Lesson 01
- Access to Neocities.org for webpage hosting and editing
- Visual Studio Code or Neocities built-in editor
- Modern web browser with developer tools

### Resources
- CSS properties reference sheet (provided)
- Color palette tools (Coolors.co, Adobe Color)
- Web accessibility color contrast checkers
- Before/after website examples showing CSS impact

### Preparation
- Review student HTML pages from previous lesson
- Prepare dramatic CSS transformation examples for motivation
- Set up color theory visual aids and accessibility tools
- Test screen reader software for accessibility demonstration

## Lesson Structure (90 minutes)

### Warm-Up Activity (10 minutes)
**"HTML vs. CSS: What's the Difference?" Quick Review**

#### Part 1: Review Gallery (5 minutes)
**Display Student Work from Yesterday:**
1. Project several student HTML introduction pages (with permission)
2. Celebrate the structure and content creation
3. Ask: "What do you notice about how these pages look?"

**Expected Observations:**
- All pages look similar (basic browser styling)
- Content is clear but visually plain
- Structure is good but presentation could be improved

#### Part 2: The CSS Transformation (5 minutes)
**Show Before/After Examples:**
1. Display the same HTML content in two browser windows
2. One window: Plain HTML with no CSS
3. Second window: Same content with beautiful CSS styling

**Discussion Prompts:**
- "What differences do you notice?"
- "Which version would you prefer to read? Why?"
- "How do you think this transformation happened?"

**Key Teaching Point:** "HTML provides the structure and content. CSS provides the visual design and presentation. Today we'll learn to transform your pages!"

### I Do: Teacher Demonstration (20 minutes)
**"CSS Fundamentals: From Plain to Beautiful"**

#### Part 1: CSS Syntax and Connection (8 minutes)
**Live Coding Setup:**
- Open yesterday's class HTML page
- Create a new CSS file or add `<style>` section in `<head>`
- Demonstrate linking CSS to HTML

**Basic CSS Syntax Explanation:**
```css
/* CSS Syntax: selector { property: value; } */
h1 {
    color: blue;
    font-size: 36px;
}

p {
    color: darkgray;
    font-family: Arial, sans-serif;
}
```

**Narration While Coding:**
- "CSS uses 'selectors' to target HTML elements"
- "Then we specify 'properties' and 'values' to change appearance"
- "Semicolons end each property, curly braces contain all properties for a selector"
- "Comments use /* */ to explain our code"

#### Part 2: Fundamental CSS Properties (12 minutes)
**Demonstrate Key Properties with Live Changes:**

**Typography:**
```css
h1 {
    font-family: "Arial", sans-serif;
    font-size: 2.5em;
    font-weight: bold;
    color: #2c3e50;
}

p {
    font-family: Georgia, serif;
    font-size: 1.1em;
    line-height: 1.6;
    color: #34495e;
}
```

**Colors and Backgrounds:**
```css
body {
    background-color: #ecf0f1;
    color: #2c3e50;
}

h2 {
    color: #e74c3c;
    background-color: #f8f9fa;
    padding: 10px;
}
```

**Spacing and Layout:**
```css
body {
    margin: 0;
    padding: 20px;
    max-width: 800px;
}

h1, h2 {
    margin-bottom: 15px;
}

p {
    margin-bottom: 20px;
}
```

**Teaching Strategies During Demonstration:**
- **Show immediate results:** Refresh browser after each change
- **Explain color choices:** "This blue is professional but friendly"
- **Connect to accessibility:** "Good contrast helps everyone read our content"
- **Use relatable analogies:** "CSS is like choosing clothes for our HTML body"

### We Do: Guided Practice (25 minutes)
**"Let's Style Our Class Website Together"**

#### Setup and Navigation (5 minutes)
**Getting Everyone Ready:**
1. Students open their HTML introduction pages from yesterday
2. Help students access CSS editing (Neocities built-in or separate file)
3. Ensure everyone can see changes by refreshing browser

#### Collaborative Styling Session (20 minutes)
**Build CSS Together with Student Input:**

**Teacher Facilitates, Students Decide:**
"Let's make our class website look amazing! What colors should we use?"

**Step 1: Typography (5 minutes)**
```css
/* Students suggest font choices and sizes */
body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
}

h1 {
    font-size: 2.5em;
    color: #2c3e50;  /* Students vote on colors */
    text-align: center;
}

h2 {
    font-size: 1.8em;
    color: #3498db;
    border-bottom: 2px solid #3498db;
}
```

**Step 2: Colors and Backgrounds (5 minutes)**
```css
/* Students choose color scheme */
body {
    background-color: #f8f9fa;
    color: #333333;
    margin: 0;
    padding: 20px;
}

ul {
    background-color: #e8f4f8;
    padding: 20px;
    border-left: 4px solid #3498db;
}
```

**Step 3: Spacing and Layout (5 minutes)**
```css
/* Improve readability and organization */
body {
    max-width: 800px;
    margin: 0 auto; /* Center the content */
}

h1, h2 {
    margin-bottom: 20px;
}

p {
    margin-bottom: 15px;
}

li {
    margin-bottom: 8px;
}
```

**Step 4: Fun Touches (5 minutes)**
```css
/* Students suggest creative additions */
h1 {
    text-shadow: 2px 2px 4px #cccccc;
}

h2:hover {
    color: #e74c3c;
    transition: color 0.3s ease;
}
```

**Engagement Strategies During We Do:**
- **"What color should we try next?"** - Student choice drives decisions
- **"Does this look better or worse?"** - Immediate feedback and iteration
- **"Who has an idea for making this more interesting?"** - Encourage creativity
- **Show accessibility tools:** Use color contrast checkers to ensure readability

### Break (5 minutes)
**Physical Movement and Mental Reset**
- Stand up and stretch
- Walk around to see other students' screens
- Grab water or snacks
- Prepare for independent creative work

### You Do: Independent Practice (20 minutes)
**"Transform Your Introduction Page with CSS"**

#### Assignment Instructions
**Style your HTML introduction page with CSS:**

**Required Styling Elements:**
1. **Typography:** Change fonts and sizes for headings and paragraphs
2. **Colors:** Apply colors to text and backgrounds (minimum 3 different colors)
3. **Spacing:** Add margins and padding to improve readability
4. **Layout:** Center or constrain content width for better presentation
5. **Accessibility:** Ensure good color contrast for all text

#### Minimum Requirements Checklist:
- [ ] **Body styling:** Font family, background color, margins/padding
- [ ] **Heading styles:** Different colors/sizes for h1, h2, etc.
- [ ] **Paragraph styling:** Readable font, appropriate line spacing
- [ ] **List styling:** Improved appearance for ul/ol and li elements
- [ ] **Color contrast:** All text remains readable on chosen backgrounds

#### Creative Challenge Options:
**For students who complete requirements early:**
- Add hover effects to headings or links
- Experiment with text shadows or other visual effects  
- Create a subtle border or accent elements
- Try different font combinations from Google Fonts

#### Example CSS Structure:
```css
/* Students can use this as starting template */
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    color: #333;
    max-width: 700px;
    margin: 0 auto;
    padding: 20px;
}

h1 {
    color: #2c3e50;
    text-align: center;
    font-size: 2.5em;
}

h2 {
    color: #3498db;
    border-bottom: 2px solid #3498db;
    padding-bottom: 5px;
}

/* Students add their own creative touches */
```

### Teacher Support During Independent Work
**Circulate and Provide Just-in-Time Help:**

**Common Issues and Solutions:**
- **"My CSS isn't working!"** → Check syntax (semicolons, curly braces), ensure CSS is linked to HTML
- **"The colors look weird!"** → Show color picker tools, discuss web-safe colors
- **"I don't know what looks good!"** → Encourage experimentation, show examples of good design
- **"My text is hard to read!"** → Introduce color contrast checkers, explain accessibility

**Encouraging Phrases:**
- "Great color choice! How does it make you feel?"
- "I love how you're experimenting - that's how designers work!"
- "Try changing one thing at a time so you can see what each property does."
- "Your page is looking more professional already!"

#### Differentiation During Independent Work

**For Advanced Students:**
- Introduce CSS Grid or Flexbox for layout
- Show how to import Google Fonts
- Demonstrate CSS animations or transitions
- Encourage research into advanced properties

**For Struggling Students:**
- Provide CSS template with comments explaining each property
- Work one-on-one to ensure basic syntax is correct
- Focus on completing one property at a time
- Use color picker tools to help with color selection

**For Students with Visual Impairments:**
- Emphasize accessibility tools and high contrast options
- Discuss how screen readers interact with CSS
- Connect to universal design principles
- Show how good CSS benefits everyone

### Wrap-Up & Assessment (10 minutes)
**"CSS Transformation Showcase"**

#### Mini Showcase (6 minutes)
**Celebrating Student Creativity:**
1. Ask 4-5 volunteers to briefly show their styled pages
2. Have presenters explain one CSS choice they made and why
3. Audience gives positive feedback using "I like how you..."

**Presentation Prompts for Students:**
- "Show us your page and tell us about one color or font choice you made"
- "What was challenging about styling your page?"
- "What are you most proud of in your design?"

#### Reflection and Preview (4 minutes)
**Processing the Learning:**

**Quick Discussion Questions:**
1. **"How did CSS change your webpage experience?"**
   - *Expected:* Made it more personal, professional, engaging
2. **"What's the relationship between HTML and CSS?"**
   - *Expected:* HTML is structure, CSS is presentation/styling
3. **"Why might web developers separate content from styling?"**
   - *Expected:* Easier to maintain, update, collaborate

**Preview Tomorrow:**
"Tomorrow we'll add JavaScript to make our pages interactive - buttons that respond, content that changes, and pages that react to user input!"

## Assessment

### Formative Assessment (During Class)
**Observation and Participation Rubric:**
- [ ] **Understanding:** Student demonstrates grasp of CSS syntax and selector concept
- [ ] **Application:** Student successfully applies multiple CSS properties to their page
- [ ] **Creativity:** Student makes thoughtful design choices beyond minimum requirements
- [ ] **Collaboration:** Student participates constructively in guided practice
- [ ] **Problem-solving:** Student attempts to debug CSS issues systematically

### Summative Assessment (End of Class)
**Styled Introduction Page Requirements Rubric:**

**4 - Exemplary Styling (Exceeds Expectations):**
- Creative and cohesive visual design with excellent color harmony
- Proper CSS syntax throughout with well-organized code
- Excellent accessibility with high contrast and readable fonts
- Additional creative elements (hover effects, shadows, etc.)
- Page demonstrates strong understanding of design principles

**3 - Proficient Styling (Meets Expectations):**
- Attractive visual design with appropriate color choices
- Correct CSS syntax with all required elements styled
- Good accessibility with readable color combinations
- All minimum requirements met effectively
- Page shows clear improvement from original HTML version

**2 - Developing Styling (Approaching Expectations):**
- Basic styling applied but limited creativity or cohesion
- CSS syntax mostly correct with minor errors
- Adequate accessibility but could be improved
- Most requirements met but execution needs refinement
- Page shows some improvement but lacks polish

**1 - Beginning Styling (Below Expectations):**
- Minimal styling applied with little visual improvement
- CSS syntax errors prevent proper rendering
- Poor accessibility with contrast or readability issues
- Several requirements missing or incorrectly implemented
- Page shows minimal change from original HTML

### Quick Assessment Activity
**"One Change Challenge" (3 minutes):**

**Instructions:**
"Make one more change to your CSS that you think improves your page. Then turn to a partner and explain what you changed and why."

**Teacher Listening For:**
- Understanding of cause-and-effect in CSS
- Design thinking and intentional choices  
- Appropriate use of CSS vocabulary
- Confidence in experimenting with code

## Homework/Extension Activities

### For All Students (Optional)
**"CSS Detective Work":**
- Visit 3 websites you use regularly (social media, news, entertainment)
- Try to identify CSS properties you learned today (colors, fonts, spacing)
- Write 2-3 sentences about how CSS makes those sites more effective

### For Students Wanting More Challenge
**"Advanced Styling Exploration":**
- Research and try 2 CSS properties we didn't cover in class
- Add them to your introduction page with comments explaining what they do
- Look up "CSS flexbox" or "CSS grid" and try one layout technique

### For Students Needing More Practice  
**"CSS Property Practice":**
- Use provided CSS reference sheet to review all properties from today
- Make small changes to your page and observe the results
- Practice CSS syntax by writing 5 new CSS rules (even if you don't use them)

## Next Lesson Preview
**"Tomorrow: JavaScript - Making Websites Interactive!"**

**Exciting Preview:**
- Show example of button that changes content when clicked
- Demonstrate form that responds to user input
- "HTML is structure, CSS is style, JavaScript is behavior and interaction"

**What Students Will Learn:**
- Variables to store information
- Functions to organize code actions
- Event handling to respond to user clicks and input
- DOM manipulation to change page content dynamically

## Materials for Next Lesson

### Teacher Preparation
- JavaScript examples showing immediate user interaction
- Variable and function concept analogies
- Debugging tools and common error messages
- Connection between JavaScript and AP Programming concepts

### Student Continuation
- Completed and styled HTML introduction page
- Understanding of HTML structure and CSS styling relationship
- Readiness to add interactive elements to their pages

## Extended Learning Opportunities

### Cross-Curricular Connections
**Art/Design:**
- Color theory principles and web design
- Typography choices and readability
- Visual hierarchy and information design

**English/Language Arts:**
- Content organization and clear communication
- Audience consideration in design choices
- Technical writing through CSS comments

**Math:**
- Proportional relationships in sizing (em, %, px)
- Geometric concepts in layout and spacing
- Data visualization through styling

### Career Connections
**Web Design Careers:**
- User Experience (UX) Designer
- User Interface (UI) Designer  
- Front-End Developer
- Visual Designer

**Industry Guest Speaker Ideas:**
- Local web design professionals
- Marketing professionals who use web design
- Small business owners who manage their own websites
- Recent graduates working in tech companies

### Accessibility Deep Dive
**Extended Discussion Topics:**
- How CSS can improve or hinder accessibility
- Screen reader interaction with styled content
- Color blindness considerations in design
- Universal design principles for inclusive web development

## Professional Reflection for Teachers

### What to Observe During This Lesson
- **Student engagement:** Are students excited about visual transformation?
- **Technical understanding:** Do students grasp CSS syntax and selector concepts?
- **Design thinking:** Are students making intentional aesthetic choices?
- **Problem-solving:** How do students approach CSS debugging?

### Common Student Misconceptions
- **"CSS is just decoration"** → Emphasize accessibility and user experience impact
- **"There's one right way to style"** → Encourage experimentation and personal expression  
- **"CSS is easier than HTML"** → Address debugging complexity while maintaining confidence
- **"Good design is just personal opinion"** → Introduce objective usability principles

### Adjustments for Future Teaching
**If students struggle with:**
- **CSS syntax:** More practice with structure before creative freedom
- **Color choices:** Provide curated color palette options
- **Design principles:** Mini-lessons on contrast, hierarchy, and readability
- **Connecting CSS to HTML:** More visual diagrams showing relationship

**If students excel quickly:**
- Advanced CSS properties and techniques
- Introduction to responsive design principles
- CSS animation and interactive effects
- Design critique and peer feedback protocols

---

**Congratulations! Your students have now experienced the powerful transformation that CSS brings to web development. They've moved from functional HTML to beautiful, accessible web pages that reflect their personal creativity and technical skills. 🎨✨**

**The foundation is set for tomorrow's exciting addition: JavaScript interactivity that will bring their pages to life!**
