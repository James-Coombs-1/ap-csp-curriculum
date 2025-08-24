# Lesson 06: Portfolio Project Planning - Bringing It All Together
**AP Computer Science Principles | Unit 1: Web Development & Digital Expression**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 3
- **Unit:** Web Development & Digital Expression
- **Prerequisites:** Lessons 01-05 (Complete web development toolkit mastered)

## Learning Targets

### I am learning to...
1. **Understand** project planning as an essential skill for creating complex, multi-feature web applications
2. **Analyze** how to integrate multiple web technologies (HTML, CSS, JavaScript, APIs, Forms) into cohesive user experiences
3. **Design** a comprehensive portfolio website that demonstrates technical mastery while serving authentic personal or professional purposes

### Success Criteria - I can...
1. **Create** a detailed project plan with timeline, features, and technical requirements for a portfolio website
2. **Integrate** design thinking principles with technical constraints to plan user-centered web experiences
3. **Develop** a project specification that balances personal creativity with demonstration of all Unit 1 programming concepts

## AP Big Ideas Connections

### Primary Focus - Integration Across All Big Ideas
This lesson synthesizes learning from all previous Unit 1 lessons and connects to broader AP concepts:

- **CRD-2.E:** Develop a program using a development process
  - *Connection:* Portfolio projects require iterative design and systematic development planning
- **CRD-2.F:** Design a program and its user interface
  - *Connection:* Portfolio websites must balance technical functionality with user experience design
- **AAP-2.A:** Express algorithms using natural language, diagrams, and pseudocode
  - *Connection:* Project planning involves describing complex processes before implementation

### Supporting Connections
- **IOC-1.A:** Explain how computing innovations can have beneficial and harmful effects
  - *Connection:* Personal websites impact digital identity and online presence
- **CRD-1.A:** Explain how computing innovations are improved through collaboration
  - *Connection:* Portfolio development benefits from peer feedback and iterative improvement

## Materials Needed

### Technology
- Computers with all student work from Lessons 01-05 accessible
- Access to Neocities accounts and previous website versions
- Internet access for design inspiration research
- Project planning and wireframing tools (digital or paper)

### Resources
- Portfolio website examples from previous students (with permission)
- Professional web developer portfolio galleries for inspiration
- Project planning templates and timeline tools
- Design thinking worksheets and user experience guides

### Preparation
- Curate inspiring but achievable portfolio examples that demonstrate Unit 1 concepts
- Set up project planning templates that guide students through comprehensive planning
- Prepare peer feedback protocols and collaboration structures
- Create assessment rubrics that value both technical implementation and creative expression

## Why Portfolio Projects Matter: Real-World Context

### **Portfolios Are Professional Necessities:**
- **College Applications:** Demonstrates initiative, creativity, and technical skills
- **Job Applications:** Shows practical abilities and personal projects beyond coursework
- **Creative Fields:** Essential for artists, designers, writers, and content creators
- **Professional Networking:** Provides shareable URL for social media profiles and business cards

### **Web Development Career Preparation:**
- **Technical Documentation:** Ability to explain and showcase programming work
- **User Experience Design:** Understanding how people interact with websites and applications
- **Project Management:** Planning, timeline creation, and feature prioritization
- **Professional Presentation:** Communicating technical concepts to diverse audiences

### **Personal Empowerment Through Technology:**
- **Digital Identity Control:** Creating authentic online presence rather than relying only on social media
- **Creative Expression:** Using technology as medium for artistic and personal communication
- **Problem-Solving Documentation:** Showcasing ability to identify problems and create solutions
- **Community Impact:** Sharing knowledge, resources, and perspectives with broader audiences

## Lesson Structure (90 minutes)

### Warm-Up Activity (15 minutes)
**"Portfolio Purpose and Audience Analysis"**

#### Part 1: Portfolio Gallery Walk (10 minutes)
**Curated Showcase:**
Display 4-5 outstanding portfolio websites (mix of student and professional examples)

**For Each Portfolio, Students Analyze:**
- "Who do you think this website is designed for?"
- "What does this person want visitors to know about them?"
- "What technical features make this site engaging and professional?"
- "How does this site balance personal creativity with professional presentation?"

**Examples to Include:**
- **Creative Student:** Art-focused portfolio with interactive galleries
- **STEM Student:** Projects and achievements with technical explanations
- **Professional Developer:** Clean, minimal design highlighting work experience
- **Community-Focused:** Local volunteer work and social impact projects

#### Part 2: Purpose and Audience Definition (5 minutes)
**Individual Reflection:**
Students complete quick self-assessment:
- "Who do I want to visit my portfolio website?" (Family, friends, college admissions, future employers, creative collaborators)
- "What impression do I want to make?" (Creative, professional, friendly, knowledgeable, community-minded)
- "What story do I want my website to tell about who I am and what I care about?"

**Key Teaching Point:**
"Great portfolios aren't just about showing off technical skills - they're about connecting authentically with people who share your interests and values."

### I Do: Teacher Demonstration (20 minutes)
**"From Scattered Projects to Cohesive Portfolio: A Complete Redesign Process"**

#### Part 1: Analyzing Current Work (8 minutes)

**Teacher Models Self-Assessment:**
"Let me look at what I've built so far and see how it could become a powerful portfolio."

**Current Projects Review:**
```
What I Have Built (Unit 1 Work):
✓ Personal introduction page with HTML/CSS
✓ Interactive JavaScript features (buttons, user input)
✓ API integration showing real-time data
✓ Contact form collecting visitor feedback

Technical Skills Demonstrated:
✓ HTML semantic structure and accessibility
✓ CSS styling and responsive design principles  
✓ JavaScript variables, functions, and event handling
✓ API integration and asynchronous programming
✓ Form processing and input validation
✓ User experience design and interface creation
```

**Gap Analysis:**
"My individual lessons work well, but they don't tell a cohesive story. I need to connect them with consistent design, clear navigation, and unified purpose."

#### Part 2: Portfolio Integration Strategy (12 minutes)

**Live Planning - Portfolio Architecture:**
```
PORTFOLIO WEBSITE STRUCTURE:

Homepage: "Welcome to My Digital World"
├── Hero section with brief intro and personality
├── Navigation to all major sections  
├── Featured project showcase with rotating highlights
└── Quick access to contact information

About Me: "My Story and Interests" 
├── Expanded personal narrative from Lesson 1
├── Interactive timeline of interests and goals
├── Fun facts API integration for engaging content
└── Photo gallery or personal media

My Projects: "Things I've Built and Learned"
├── Showcase of all Unit 1 technical work
├── Each project with description, tech used, lessons learned
├── Interactive demos embedded directly in portfolio
└── Links to live versions and source code

Get In Touch: "Let's Connect"
├── Enhanced contact form from Lesson 5
├── Social media and professional links
├── Visitor feedback and website guestbook
└── Professional contact information for opportunities

Resources & Blog: "Things I Want to Share" (Optional)
├── Helpful links and tools I've discovered
├── Tutorials or guides I've created
├── Reflection on learning computer science
└── Updates on current projects and interests
```

**Teaching Narration:**
- "Notice how each section builds on work you've already completed"
- "The goal is integration and storytelling, not starting over from scratch"
- "Professional portfolios show both technical skills AND personality"
- "Every page should have clear purpose and connect to your overall message"

**Technical Integration Planning:**
```javascript
// Example: Unified JavaScript for enhanced user experience
let portfolioData = {
    currentProject: 0,
    visitorCount: 0,
    featuredContent: [
        {title: "Interactive Weather App", tech: "API Integration", link: "weather.html"},
        {title: "Personal Contact Form", tech: "Form Processing", link: "contact.html"},
        {title: "Creative CSS Animations", tech: "Advanced Styling", link: "gallery.html"}
    ]
};

// Rotate featured projects on homepage
function rotateFeaturedProject() {
    portfolioData.currentProject = (portfolioData.currentProject + 1) % portfolioData.featuredContent.length;
    updateFeaturedDisplay();
}

// Track and display visitor engagement
function welcomeVisitor() {
    portfolioData.visitorCount++;
    displayPersonalizedWelcome();
}
```

**Key Teaching Points:**
- "JavaScript can create continuity across multiple pages"
- "Data structures help organize complex information"
- "User experience flows should be intuitive and engaging"
- "Professional portfolios balance automation with personal touch"

### We Do: Guided Practice (25 minutes)
**"Let's Plan a Portfolio Together"**

#### Setup and Collaborative Planning (10 minutes)
**Class Chooses a Fictional Persona:**
"Let's create a portfolio plan for 'Alex Chen', a student interested in environmental science and creative technology."

**Collaborative Persona Development:**
- **Interests:** Climate change, digital art, coding for social good
- **Goals:** College admission for environmental engineering, summer internship at environmental nonprofit
- **Audience:** College admissions officers, environmental organizations, peers interested in science
- **Personality:** Thoughtful, creative, community-minded, technically curious

#### Portfolio Planning Session (15 minutes)
**Build Comprehensive Plan Together:**

**Homepage Strategy (Students Contribute Ideas):**
```html
<!-- Students suggest content and features -->
<header class="hero-section">
    <h1>Alex Chen - Technology for Environmental Change</h1>
    <p class="mission-statement">Using code and creativity to build a more sustainable future</p>
    <div class="current-focus">
        <!-- API integration showing current environmental data -->
        <div id="local-air-quality">Air Quality: <span id="aqi-data">Loading...</span></div>
        <div id="climate-tip">Daily Action: <span id="green-tip">Loading...</span></div>
    </div>
</header>

<section class="featured-projects">
    <h2>Current Projects</h2>
    <!-- Rotating showcase of best work -->
    <div id="project-spotlight">
        <!-- JavaScript rotates through portfolio pieces -->
    </div>
</section>
```

**Project Showcase Planning:**
Students help design how Alex would present Unit 1 work:

1. **"Carbon Footprint Calculator"** (Interactive form + API data)
   - Form collecting daily activities and transportation
   - API integration for environmental impact calculations
   - Personalized suggestions for carbon reduction

2. **"Local Environmental Resources"** (API integration + mapping)
   - Real-time data about local air quality, weather patterns
   - Interactive map of nearby recycling centers and green spaces
   - Community event listings for environmental activism

3. **"Green Living Blog"** (Content management + user interaction)
   - Personal reflections on environmental learning
   - Interactive comment system for visitor engagement
   - Resource sharing and educational content creation

**Technical Architecture (Class Designs Together):**
```javascript
// Unified portfolio functionality
let alexPortfolio = {
    environmentalData: {
        airQuality: null,
        greenTips: [],
        carbonFootprint: 0
    },
    
    projects: [
        {
            name: "Carbon Calculator",
            tech: ["HTML Forms", "JavaScript", "Environmental APIs"],
            impact: "Helps users understand personal environmental impact",
            demoLink: "carbon-calc.html"
        }
        // ... more projects
    ],
    
    updateEnvironmentalData: function() {
        // Fetch current environmental information
        // Display personalized content based on location/season
    }
};
```

**Teaching Strategies During We Do:**
- **Students drive creative decisions:** "What would make Alex's portfolio unique and authentic?"
- **Connect to technical requirements:** "How would Alex use APIs to support their environmental focus?"
- **Emphasize integration:** "How do these projects work together to tell Alex's story?"
- **Consider user experience:** "What would college admissions officers want to see?"

### Break (5 minutes)
**Mental Reset and Inspiration**
- Look at additional portfolio examples for diverse inspiration
- Discuss with neighbors about personal portfolio ideas
- Prepare for intensive individual planning work

### You Do: Independent Practice (20 minutes)
**"Design Your Personal Portfolio Website Plan"**

#### Assignment Instructions
**Create a comprehensive plan for your Unit 1 capstone portfolio website:**

**Required Planning Elements:**
1. **Portfolio Purpose Statement** - Who is your audience and what impression do you want to make?
2. **Site Architecture** - What pages/sections will you include and how do they connect?
3. **Content Integration Plan** - How will you showcase your Unit 1 work (HTML, CSS, JavaScript, APIs, Forms)?
4. **Technical Feature List** - What interactive elements will engage visitors and demonstrate your skills?
5. **Design Vision** - What visual style and user experience will represent your personality?
6. **Implementation Timeline** - What will you complete in each of the next 3 lessons?

#### Portfolio Planning Template:
```
PERSONAL PORTFOLIO WEBSITE PLAN

Portfolio Purpose & Audience:
My portfolio is designed for: ________________________________
The main impression I want to create: ______________________
My unique value proposition: _____________________________

Site Architecture:
□ Homepage: ___________________________________________
□ About/Personal: _____________________________________ 
□ Projects/Work: ______________________________________
□ Contact/Connect: ____________________________________
□ Additional Sections: _________________________________

Content Integration (Unit 1 Work):
□ HTML/CSS Foundation: How will you showcase design skills?
□ JavaScript Interactivity: What dynamic features will you include?
□ API Integration: What external data will enhance your site?
□ Form Processing: How will visitors interact and provide input?
□ Creative Elements: What makes your portfolio uniquely yours?

Technical Features List:
□ Navigation system and user flow design
□ Interactive project demonstrations  
□ Personalized user experiences
□ Professional contact and networking tools
□ Performance optimization and mobile responsiveness

Design Vision:
Visual Style: __________________________________________
Color Palette: _________________________________________ 
Typography Choices: ____________________________________
User Experience Goals: _________________________________

Implementation Timeline:
Week 1 (Next lesson): __________________________________
Week 2 (Following lesson): ______________________________
Week 3 (Final lesson): _________________________________
```

#### Portfolio Concept Examples to Spark Ideas:

**STEM/Technology Focus:**
- Showcase programming projects with interactive demos
- Include technical blog posts and learning reflections
- Feature calculator tools, data visualizations, or educational resources
- Connect to internship opportunities and college programs

**Creative/Arts Focus:**
- Digital art gallery with interactive features
- Creative writing samples with engaging presentation
- Music, video, or multimedia project showcases  
- Portfolio targeting art schools, creative programs, or artistic collaborations

**Community/Service Focus:**
- Document volunteer work and social impact projects
- Resource sharing for community organizations
- Interactive tools that help solve local problems
- Connect with nonprofit opportunities and civic engagement

**Academic/Research Focus:**  
- Research project documentation and presentation
- Educational resources for other students
- Academic achievement showcases with context and reflection
- Connect to scholarship opportunities and academic programs

**Entrepreneurial/Business Focus:**
- Document business ideas and startup concepts
- Market research tools and customer feedback systems
- Professional networking and mentorship connections
- Connect to business competitions and entrepreneurship programs

### Teacher Support During Independent Work
**Individual Conferences and Strategic Guidance:**

**Common Planning Challenges and Responses:**
- **"I don't know what makes me unique!"** → "What problems do you care about solving? What do friends come to you for help with?"
- **"My work isn't impressive enough!"** → "Employers and colleges want to see growth and learning process, not perfection."
- **"I have too many ideas!"** → "Let's prioritize features that best demonstrate your Unit 1 learning and serve your target audience."
- **"I don't know who my audience is!"** → "Think about opportunities you want in the next 2-3 years - internships, colleges, creative collaborations."

**Strategic Planning Questions:**
1. "What story do you want your portfolio to tell about your growth this semester?"
2. "Which of your Unit 1 projects are you most proud of and why?"
3. "What would make someone remember your portfolio after visiting 10 others?"
4. "How can your technical skills serve your personal interests and values?"
5. "What would success look like for your portfolio - what responses would you want from visitors?"

**Encouraging Innovation:**
- "I love how this portfolio concept connects your technical skills with your passion for [student interest]!"
- "Your integration plan shows sophisticated thinking about user experience and technical implementation!"
- "This portfolio would definitely make you stand out in a crowd while staying authentic to who you are!"
- "Your timeline shows realistic planning - that's exactly how professional developers approach complex projects!"

#### Differentiation Strategies

**For Advanced Students:**
- Encourage advanced technical features like database integration or complex animations
- Challenge them to create tools that could actually help their community or target audience
- Connect them with professional mentors who can provide feedback on portfolio concepts
- Suggest documentation of their learning process for other students

**For Students Needing More Structure:**
- Provide additional examples of successful but simple portfolios
- Help them narrow focus to 3-4 core strengths rather than trying to showcase everything
- Work together to create very specific, achievable technical goals
- Emphasize that authentic, well-executed simple portfolios are better than complex, incomplete ones

**For Students Lacking Confidence:**
- Review their Unit 1 work to help them see their significant growth and achievements
- Connect them with peer mentors who can share their own planning process
- Emphasize that portfolios are about learning journey, not comparing to others
- Help them identify unique perspectives or experiences that add value to their story

### Wrap-Up & Assessment (5 minutes)
**"Portfolio Vision Sharing"**

#### Quick Vision Presentations (4 minutes)
**Portfolio Concept Sharing:**
1. Ask 4-5 volunteers to share their portfolio concept in 30 seconds each
2. Focus on purpose, audience, and one unique technical feature they're excited about
3. Class provides encouraging feedback and connects to shared interests

**Presentation Format:**
"My portfolio will be for [audience] and will help me [purpose]. The coolest technical feature will be [specific innovation]."

#### Anticipation and Next Steps (1 minute)
**Looking Forward:**
- "Tomorrow we start building these amazing portfolio visions into reality!"
- "Your planning shows incredible creativity and sophisticated technical thinking"
- "Remember: great portfolios evolve - tomorrow we'll start with your strongest ideas and build from there"

## Assessment

### Formative Assessment (During Class)
**Portfolio Planning Process Checklist:**
- [ ] **Strategic Thinking:** Student articulates clear purpose and target audience for portfolio
- [ ] **Technical Integration:** Student plans meaningful incorporation of all Unit 1 concepts
- [ ] **Creative Vision:** Student balances personal expression with professional presentation
- [ ] **Project Management:** Student creates realistic timeline and implementation strategy
- [ ] **User Experience Focus:** Student considers visitor needs and engagement strategies

### Summative Assessment (End of Class)
**Portfolio Planning Document Rubric:**

**4 - Exemplary Portfolio Planning (Exceeds Expectations):**
- Compelling, well-defined purpose with clear understanding of target audience and professional goals
- Sophisticated technical integration plan that meaningfully incorporates all Unit 1 concepts
- Creative vision that authentically represents student personality while maintaining professional appeal
- Detailed, realistic implementation timeline with specific milestones and contingency planning
- Evidence of strategic thinking about user experience, navigation, and visitor engagement

**3 - Proficient Portfolio Planning (Meets Expectations):**
- Clear portfolio purpose with appropriate audience identification and goal articulation
- Solid technical integration plan addressing all required Unit 1 concepts appropriately
- Good balance of personal creativity and professional presentation in design vision
- Reasonable implementation timeline with specific goals for each development phase
- Demonstrates understanding of portfolio best practices and user experience principles

**2 - Developing Portfolio Planning (Approaching Expectations):**
- Basic portfolio purpose identified but could be more specific or well-defined
- Technical integration plan addresses most requirements but needs development
- Some creative vision present but balance between personal and professional could be improved
- Implementation timeline exists but may be unrealistic or lack specific milestones
- Shows understanding of portfolio concepts but planning needs refinement

**1 - Beginning Portfolio Planning (Below Expectations):**
- Unclear or inappropriate portfolio purpose without clear audience or goal identification
- Technical integration plan missing significant elements or shows confusion about requirements
- Limited creative vision or poor balance between personal expression and professional needs
- Unrealistic or incomplete implementation timeline without specific planning
- Limited understanding of portfolio development and strategic planning concepts

### Individual Conference Notes
**Teacher Documentation for Each Student:**
- **Portfolio Concept:** How authentic and achievable is their vision?
- **Technical Ambition:** Does their plan appropriately challenge their skill level?
- **Timeline Realism:** Will they be able to complete their planned features?
- **Support Needs:** What specific help will they need during implementation?
- **Growth Opportunities:** How can this project stretch their learning?

## Homework/Extension Activities

### For All Students (Required)
**"Portfolio Research and Refinement":**
- Find 3 additional portfolio websites (professional or student) that inspire your approach
- Create a mood board or design inspiration collection for your visual style
- Write a one-paragraph "elevator pitch" describing your portfolio concept
- Begin gathering content (photos, project descriptions, personal statement drafts)

### For Students Wanting More Challenge
**"Advanced Portfolio Strategy":**
- Research portfolio best practices for your intended career field or college major
- Create detailed user personas for your target audiences
- Develop comprehensive content strategy including blogging or resource creation
- Begin learning advanced web technologies that could enhance your portfolio

### For Students Needing More Support
**"Portfolio Foundation Building":**
- Focus on organizing and improving your best work from Unit 1
- Create simple sketches or wireframes of your main page layouts
- Write brief descriptions of each project you want to showcase
- Meet with teacher or peer mentor to refine and simplify your plan

## Next Lesson Preview
**"Tomorrow: Portfolio Development Sprint 1 - Foundation and Structure"**

**What Students Will Do:**
- Set up portfolio website structure and navigation system
- Begin implementing their planned design with HTML and CSS foundation
- Integrate their strongest Unit 1 work into portfolio context
- Test and refine user experience with peer feedback

**What Students Will Learn:**
- Advanced HTML semantic structure for complex, multi-page websites
- CSS layout techniques for professional portfolio presentation
- JavaScript navigation and user experience enhancement
- Systematic approach to integrating multiple web technologies

## Materials for Next Lesson

### Teacher Preparation
- Individual student portfolio plans reviewed for feasibility and support needs
- Development environment setup for complex, multi-page website creation
- Peer feedback protocols and collaboration structures for portfolio development
- Advanced HTML/CSS resources and troubleshooting guides

### Student Readiness
- Completed portfolio plan with clear vision and implementation strategy
- Organized Unit 1 work ready for integration into portfolio context
- Design inspiration and content materials prepared for implementation
- Enthusiasm for creating showcase-quality web development project

---

**🎯 Outstanding! Your students have now planned comprehensive portfolio projects that will showcase their Unit 1 mastery while serving authentic personal and professional purposes. They're ready to transform from individual lesson completers to integrated web developers creating cohesive, powerful digital portfolios!**

**The next three lessons will guide them through systematic portfolio development, culminating in professional-quality websites they can proudly share with colleges, employers, and their communities! 🌟💼**