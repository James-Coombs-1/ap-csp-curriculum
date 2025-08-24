# Lesson 08: Portfolio Development Sprint 2 - Content Integration and Interactivity
**AP Computer Science Principles | Unit 1: Web Development & Digital Expression**

## Lesson Overview
- **Duration:** 90 minutes (A/B Block)
- **Week:** 4
- **Unit:** Web Development & Digital Expression
- **Prerequisites:** Lesson 07 (Complete portfolio foundation with working navigation required)

## Learning Targets

### I am learning to...
1. **Understand** how to integrate multiple web development projects into a cohesive, professional portfolio narrative
2. **Analyze** effective strategies for presenting technical work to diverse audiences (peers, educators, employers, colleges)
3. **Create** interactive portfolio features that demonstrate programming mastery while engaging visitors meaningfully

### Success Criteria - I can...
1. **Integrate** all Unit 1 projects (HTML/CSS pages, JavaScript features, API integrations, forms) into professional portfolio context
2. **Implement** interactive demonstrations and dynamic content that showcase technical capabilities effectively
3. **Present** programming work with clear explanations that communicate learning journey and technical growth

## AP Big Ideas Connections

### Primary Focus - Demonstrating Mastery Across All Big Ideas
This lesson requires integration and demonstration of learning from all AP CSP Big Ideas:

- **CRD-1.A:** Explain how computing innovations are improved through collaboration
  - *Connection:* Portfolio development incorporates peer feedback and iterative improvement
- **DAT-2.D:** Extract information from data using a program
  - *Connection:* Portfolio projects demonstrate data processing and API integration skills
- **AAP-3.B:** Explain how procedural abstraction manages complexity
  - *Connection:* JavaScript functions and code organization in portfolio demonstrate abstraction principles

### Supporting Connections
- **IOC-1.A:** Explain beneficial and harmful effects of computing innovations
  - *Connection:* Portfolio reflection includes impact analysis of created projects
- **CSN-1.B:** Explain how the Internet works
  - *Connection:* Portfolio hosting and API integrations demonstrate network understanding

## Materials Needed

### Technology
- Computers with completed portfolio foundations from Lesson 07
- Access to all student Unit 1 work (individual projects and files)
- Image editing tools for screenshots and project documentation
- Testing devices or browser developer tools for cross-device validation

### Resources
- Project presentation examples and templates
- Technical writing guides for developer portfolios
- Interactive demonstration tools and techniques
- Professional portfolio galleries for content inspiration

### Preparation
- Review each student's Unit 1 work to understand their integration needs
- Prepare examples of effective technical project presentation
- Set up peer testing protocols and feedback structures
- Create quality assurance checklists for integrated portfolio functionality

## The Integration Challenge: From Projects to Portfolio

### **Transforming Individual Work into Cohesive Story**
Students must transition from:
- **Separate lesson assignments** → **Integrated professional demonstration**
- **Learning exercises** → **Showcase of capabilities and growth**
- **Technical functionality** → **User-focused presentation and explanation**
- **Individual features** → **Comprehensive web development portfolio**

### **Professional Presentation Standards**
- **Context and Purpose:** Each project serves the overall portfolio narrative
- **Technical Documentation:** Clear explanations of what was built and how
- **User Experience:** Visitors can easily understand and interact with demonstrations
- **Growth Story:** Portfolio shows progression from beginner to capable developer

## Lesson Structure (90 minutes)

### Warm-Up Activity (10 minutes)
**"From Assignments to Achievements: Content Strategy"**

#### Project Inventory and Narrative Planning (10 minutes)
**Individual Assessment and Story Development:**

Students review their Unit 1 work and complete portfolio integration planning:

**Project Inventory Checklist:**
```
UNIT 1 PROJECTS TO INTEGRATE:

Lesson 1 - HTML Foundations:
□ Personal introduction page (✓ Have files / ✗ Need to recreate)
□ Status: [Working perfectly / Needs updates / Missing files]
□ Portfolio Integration: [How will this fit into About section?]

Lesson 2 - CSS Styling:
□ Styled personal webpage (✓ Have files / ✗ Need to recreate)
□ Status: [Working perfectly / Needs updates / Missing files]
□ Portfolio Integration: [Design elements to carry forward?]

Lesson 3 - JavaScript Fundamentals:
□ Interactive features and user input (✓ Have files / ✗ Need to recreate)
□ Status: [Working perfectly / Needs updates / Missing files]  
□ Portfolio Integration: [Which features demonstrate best skills?]

Lesson 4 - APIs and External Data:
□ API integration projects (✓ Have files / ✗ Need to recreate)
□ Status: [Working perfectly / Needs updates / Missing files]
□ Portfolio Integration: [How to showcase dynamic data skills?]

Lesson 5 - Forms and User Input:
□ Interactive forms and validation (✓ Have files / ✗ Need to recreate)
□ Status: [Working perfectly / Needs updates / Missing files]
□ Portfolio Integration: [Contact form + project demonstrations?]
```

**Portfolio Narrative Development:**
Students write 2-3 sentences for each project answering:
- "What does this project demonstrate about my programming abilities?"
- "How does this project connect to my personal interests or goals?"
- "What would I want a college admissions officer or employer to understand about this work?"

### I Do: Teacher Demonstration (25 minutes)
**"Creating Compelling Project Presentations"**

#### Part 1: Project Integration Strategy (12 minutes)

**Live Integration - Weather App Example:**

**Before Integration (Assignment Context):**
Simple weather app showing current conditions using API integration.

**After Integration (Portfolio Context):**
```html
<!-- projects.html - Professional Project Presentation -->
<article class="project-showcase">
    <div class="project-header">
        <h2>Local Weather Dashboard</h2>
        <div class="project-tags">
            <span class="tag">JavaScript</span>
            <span class="tag">API Integration</span>
            <span class="tag">Responsive Design</span>
            <span class="tag">User Experience</span>
        </div>
    </div>
    
    <div class="project-content">
        <div class="project-demo">
            <!-- Live working demo embedded -->
            <iframe src="projects/weather-app/index.html" 
                    title="Weather App Demo"
                    class="project-iframe">
            </iframe>
            <div class="demo-controls">
                <button onclick="refreshDemo('weather-app')">Try Different City</button>
                <a href="projects/weather-app/index.html" target="_blank">Open Full Demo</a>
            </div>
        </div>
        
        <div class="project-description">
            <h3>What I Built</h3>
            <p>This weather dashboard connects to real-time meteorological data to help users plan their day. I developed it to solve a personal problem - I bike to school and need reliable weather information that's faster than checking multiple apps.</p>
            
            <h3>Technical Implementation</h3>
            <ul>
                <li><strong>API Integration:</strong> Fetches live data from OpenWeatherMap API</li>
                <li><strong>Error Handling:</strong> Gracefully manages network failures and invalid responses</li>
                <li><strong>User Input:</strong> Allows location customization with form validation</li>
                <li><strong>Responsive Design:</strong> Works on desktop, tablet, and mobile devices</li>
            </ul>
            
            <h3>What I Learned</h3>
            <p>This project taught me how web applications connect to external services and handle unpredictable data. I learned to plan for edge cases like network failures and invalid user input. Most importantly, I discovered how programming can solve real problems I face every day.</p>
            
            <h3>Future Improvements</h3>
            <p>I'd like to add weather forecasting, save user location preferences, and include more detailed meteorological data for outdoor activity planning.</p>
        </div>
    </div>
    
    <div class="project-links">
        <a href="projects/weather-app/index.html" class="btn-primary" target="_blank">View Live Demo</a>
        <a href="#contact" class="btn-secondary">Ask About This Project</a>
    </div>
</article>
```

**Teaching Points About Professional Presentation:**
- "Context explains why you built something, not just what you built"
- "Technical details demonstrate specific skills to employers and educators"
- "Learning reflections show growth mindset and self-awareness"
- "Future improvements indicate ongoing curiosity and development goals"

#### Part 2: Interactive Portfolio Features (13 minutes)

**Live Coding - Dynamic Project Showcase:**
```javascript
// portfolio.js - Interactive Portfolio Functionality
class PortfolioManager {
    constructor() {
        this.projects = [
            {
                id: 'weather-app',
                title: 'Local Weather Dashboard',
                tech: ['JavaScript', 'APIs', 'Responsive Design'],
                category: 'web-apps',
                featured: true,
                demoUrl: 'projects/weather-app/index.html',
                description: 'Real-time weather data with user customization'
            },
            {
                id: 'contact-form',
                title: 'Interactive Contact System',
                tech: ['HTML Forms', 'JavaScript Validation', 'UX Design'],
                category: 'user-interface',
                featured: true,
                demoUrl: 'projects/contact-form/index.html',
                description: 'Professional contact form with smart validation'
            }
            // ... more projects
        ];
        
        this.currentFilter = 'all';
        this.init();
    }
    
    init() {
        this.renderProjects();
        this.setupFilters();
        this.setupInteractivity();
    }
    
    renderProjects(filter = 'all') {
        const projectGrid = document.getElementById('project-grid');
        const filteredProjects = filter === 'all' 
            ? this.projects 
            : this.projects.filter(project => project.category === filter);
        
        projectGrid.innerHTML = filteredProjects.map(project => `
            <div class="project-card" data-project="${project.id}">
                <div class="project-preview">
                    <iframe src="${project.demoUrl}" 
                            title="${project.title} Preview"
                            class="project-thumbnail">
                    </iframe>
                    <div class="project-overlay">
                        <button class="demo-btn" onclick="portfolio.openDemo('${project.id}')">
                            View Demo
                        </button>
                    </div>
                </div>
                <div class="project-info">
                    <h3>${project.title}</h3>
                    <p>${project.description}</p>
                    <div class="project-tech">
                        ${project.tech.map(tech => `<span class="tech-tag">${tech}</span>`).join('')}
                    </div>
                </div>
            </div>
        `).join('');
    }
    
    openDemo(projectId) {
        const project = this.projects.find(p => p.id === projectId);
        if (project) {
            // Create modal or new window for full demo
            this.createDemoModal(project);
        }
    }
    
    createDemoModal(project) {
        const modal = document.createElement('div');
        modal.className = 'demo-modal';
        modal.innerHTML = `
            <div class="modal-content">
                <div class="modal-header">
                    <h2>${project.title} - Live Demo</h2>
                    <button class="close-modal">&times;</button>
                </div>
                <div class="modal-body">
                    <iframe src="${project.demoUrl}" 
                            title="${project.title} Full Demo"
                            class="full-demo-iframe">
                    </iframe>
                </div>
                <div class="modal-actions">
                    <a href="${project.demoUrl}" target="_blank" class="btn-primary">Open in New Tab</a>
                    <button class="close-modal btn-secondary">Close Demo</button>
                </div>
            </div>
        `;
        
        document.body.appendChild(modal);
        
        // Close modal functionality
        modal.querySelectorAll('.close-modal').forEach(btn => {
            btn.addEventListener('click', () => {
                document.body.removeChild(modal);
            });
        });
    }
}

// Initialize portfolio when page loads
const portfolio = new PortfolioManager();
```

**Key Teaching Points:**
- "Interactive portfolios engage visitors and demonstrate advanced programming skills"
- "Object-oriented JavaScript shows understanding of code organization and abstraction"
- "Professional portfolios provide multiple ways to explore and understand your work"
- "Technical demonstrations should be accessible to both technical and non-technical audiences"

### We Do: Guided Practice (25 minutes)
**"Let's Integrate Projects Together"**

#### Setup and Content Organization (10 minutes)
**Collaborative Integration Strategy:**

Students work alongside teacher to integrate their strongest Unit 1 project into portfolio context:

**Project Selection and Preparation:**
1. Each student chooses their best or most complete Unit 1 project
2. Class discusses integration strategy: embedded demos vs. linked projects
3. Students adapt project presentation following demonstrated model
4. Peer feedback on project descriptions and technical explanations

**Integration Planning Session:**
- Students create project folders within portfolio structure
- Class develops consistent naming conventions and file organization
- Students write project descriptions using professional template
- Peer review of project explanations for clarity and completeness

#### Live Integration Implementation (15 minutes)
**Build Project Showcases Together:**

**HTML Project Presentation (Students Customize):**
```html
<!-- Each student adapts this template for their chosen project -->
<article class="project-showcase" id="student-project-1">
    <div class="project-header">
        <h2>[Student Project Title]</h2>
        <div class="project-tags">
            <!-- Students identify their technical skills demonstrated -->
            <span class="tag">[Primary Technology]</span>
            <span class="tag">[Secondary Feature]</span>
            <span class="tag">[Design Element]</span>
        </div>
    </div>
    
    <div class="project-content">
        <div class="project-demo">
            <!-- Student embeds their working project -->
            <div class="demo-container">
                [Working project demonstration or screenshot]
            </div>
            <div class="demo-controls">
                <button onclick="refreshStudentDemo()">Try It Out</button>
                <a href="[project-link]" target="_blank">View Full Project</a>
            </div>
        </div>
        
        <div class="project-description">
            <h3>Project Purpose</h3>
            <p>[Student explains why they built this