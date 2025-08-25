# How to Use the Technical Design Document Template
## Implementation Guide Based on Big Tech Best Practices

This guide explains how to effectively use the Technical Design Document template, incorporating proven practices from Google, Microsoft, Amazon, Meta, Apple, and Netflix.

---

## When to Create a Technical Design Document

### **Create a TDD when:**
- The change requires more than 2 weeks of engineering work
- The problem has multiple solutions and the optimal choice isn't apparent
- The design involves non-trivial changes between software components
- You're building something new or making significant architectural changes
- Multiple teams need to collaborate on the implementation
- You need senior engineering input on design decisions

### **Don't create a TDD when:**
- The solution is obvious and straightforward
- It's a simple bug fix or minor feature addition
- The document would be just an "implementation manual" without trade-offs
- You're in rapid prototyping mode (though prototypes can inform the TDD later)

---

## Writing Process (Based on Google's Approach)

### **Step 1: Start with Context and Background**
- Write this section first to clarify your own thinking
- Focus on objective facts, not opinions
- Assume some prior knowledge but link to detailed information
- Keep it succinct but comprehensive

### **Step 2: Define Goals and Non-Goals**
- Non-goals are NOT negated goals ("system shouldn't crash")
- Non-goals are things that could reasonably be goals but are explicitly out of scope
- Example: "ACID compliance" might be a non-goal for a specific database design

### **Step 3: Research and Iterate**
- Build prototypes when necessary to validate your approach
- Alternate between writing the doc and doing research
- Test your assumptions with code or proof-of-concepts

### **Step 4: Document Design Decisions and Trade-offs**
- This is the MOST IMPORTANT section (Google's emphasis)
- Focus on why you made specific decisions
- Explain what you considered and why you rejected alternatives
- Show your reasoning process

### **Step 5: Write the Executive Summary Last**
- You can't summarize research you haven't done yet
- This should be understandable by non-technical stakeholders

---

## Key Principles from Big Tech Companies

### **Google's Philosophy**
- **Focus on trade-offs:** Document why you chose solution A over solution B
- **Informal but structured:** Don't be overly rigid, adapt to your project
- **Emphasize alternatives:** Show what you considered and why you rejected it
- **Length matters:** 10-20 pages for large projects, 1-3 pages for smaller ones

### **Amazon's 6-Pager Approach**
- **Be data-driven:** Use specific numbers, not vague terms like "many customers"
- **Avoid weasel words:** Don't use "better," "improved" without quantification
- **Start with the problem:** Always begin with the customer problem
- **Structured narrative:** No bullet points in the main narrative

### **Microsoft's PRD Elements**
- **Executive Summary:** High-level overview for all stakeholders
- **Competitive Analysis:** Understanding the landscape
- **Clear assumptions:** Document what you're assuming to be true
- **Success metrics:** Define how you'll measure success

### **Netflix's Documentation Philosophy**
- **Start with the problem, not the solution**
- **Use real production examples:** Don't rely on toy examples
- **Include failure scenarios:** Document what can go wrong and how to handle it
- **Progressive disclosure:** Layer information for different skill levels

---

## Section-by-Section Guidance

### **1. Executive Summary**
- Write this in business language, not just technical jargon
- Include the problem, solution, and impact in 3-5 sentences
- Make it standalone - executives might only read this section

### **2. Context and Background**
- **Business Context:** Why does this matter to the business?
- **Technical Context:** What's the current state of the world?
- **Problem Statement:** Be specific and objective

### **3. Goals and Non-Goals**
- **Goals:** What you're trying to achieve
- **Non-Goals:** What you're explicitly NOT doing (this is crucial)
- **Success Metrics:** How will you know if you succeeded?

### **4. Requirements**
- **Functional:** What the system must do
- **Non-Functional:** Performance, scalability, security, etc.
- **Be specific:** "Response time < 100ms" not "fast response"

### **5. High-Level Design**
- Start with diagrams - visuals are crucial
- System context diagram showing how this fits in the larger ecosystem
- Keep high-level, save details for later sections

### **6. Detailed Design**
- Break down major components and their responsibilities
- Show interfaces between components
- Include data models and storage decisions
- Document API designs if applicable

### **7. Trade-offs and Design Decisions**
- **This is the heart of your document**
- For each major decision, document:
  - What options you considered
  - What you chose
  - Why you made that choice
  - What trade-offs you accepted

### **8. Alternatives Considered**
- Show other approaches you evaluated
- Explain why you didn't choose them
- This demonstrates thorough thinking

### **9. Cross-Cutting Concerns**
- Security, observability, privacy, performance
- Don't leave these as afterthoughts
- Address them early in the design process

---

## Review and Feedback Process

### **Google's Review Approach**
1. **Rapid iteration phase:** Share with close collaborators first
2. **Wider team review:** Get broader input
3. **Formal review meetings:** For complex or high-stakes projects
4. **Update during implementation:** Keep the doc current as you build

### **Best Practices for Reviews**
- Share the document at the start of meetings, read together for 15 minutes
- Focus review comments on trade-offs and decisions, not formatting
- Seek diverse perspectives, especially from different disciplines
- Don't let perfect be the enemy of good - docs should be "good enough"

---

## Tools and Collaboration

### **Recommended Tools**
- **Google Docs:** Best for collaborative writing and commenting
- **Confluence:** Good for enterprise teams with complex workflows
- **Notion:** Great for structured documents with databases
- **GitHub/GitLab:** Good for version control but harder for collaboration
- **Figma/Lucidchart:** For diagrams and system architecture visuals

### **Collaboration Tips**
- Use commenting features extensively during review
- Track changes and decisions in the document
- Keep a change log or version history
- Set up clear ownership and approval processes

---

## Common Pitfalls to Avoid

### **Don't:**
- Write implementation manuals without trade-offs
- Copy-paste formal interface definitions (they get outdated)
- Include too much code or pseudo-code
- Make it too long (over 20 pages for most projects)
- Write it after implementation (defeats the purpose)
- Leave it unmaintained after shipping

### **Do:**
- Focus on design decisions and reasoning
- Use prototypes to validate assumptions
- Keep it current during implementation
- Make it accessible to your target audience
- Include diagrams and visuals
- Document what you learned afterward

---

## Adapting the Template

### **For Different Project Types:**
- **Greenfield projects:** More focus on architecture and technology choices
- **Legacy system changes:** More emphasis on constraints and integration
- **API/Library design:** Heavy focus on interfaces and backward compatibility
- **Data projects:** Emphasize data models, privacy, and compliance

### **For Different Company Cultures:**
- **Startup:** Shorter, more agile, focus on MVP and iteration
- **Enterprise:** More formal, compliance-focused, detailed approval process
- **Open source:** Public-facing, community input, clear contribution guidelines

---

## Measuring Success

### **Signs of a Good TDD:**
- New team members can understand the system design
- Senior engineers provide meaningful feedback
- Implementation proceeds smoothly with fewer surprises
- The document serves as useful reference during maintenance
- Design decisions are clear and well-justified

### **Signs You Need to Improve:**
- Reviewers ask basic questions about scope or approach
- Implementation requires significant design changes
- Team members bypass the document and ask direct questions
- The document becomes outdated quickly
- Stakeholders can't understand the business impact

---

## Maintenance and Evolution

### **During Implementation:**
- Update the document as you learn new information
- Add amendments or new sections rather than rewriting everything
- Link to related implementation details or new documents

### **After Shipping:**
- Review your document 6-12 months later
- Document what you got right and wrong
- Use these insights to improve future design docs
- Keep key architectural decisions but archive implementation details

---

*Remember: The goal isn't to create perfect documentation, but to facilitate better decision-making, knowledge sharing, and consensus building across your team and organization.*