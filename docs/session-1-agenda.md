# Session 1: Foundations + Setup

**Date**: Wednesday, December 3, 2025
**Duration**: 2 hours
**What to Bring**: Your laptop with setup complete, 3-5 sample customer emails, writing samples for brand voice

---

## What You'll Learn

By the end of this session, you will:
- Understand the complete AI-powered email system you're building
- See Hattie B's working demo (what "really good" looks like)
- Learn the Fisk Method and TOAST Method for agent development
- Set up your Gemini File Search knowledge base
- Understand agentic RAG (when to use KB vs. tools)
- Know how to personalize your agents
- Have clear homework to prepare for building in Session 3

---

## Session Outline

### Part 1: Foundation (0:00-0:20)

**Tech Stack & Methodology** (10 min)
- Our tools: Claude Sonnet 4.5, Gemini Flash 2.5, N8N, The Stacks UI
- Fisk Method: 8-phase framework for personalizing agents
- TOAST Method: Continuous improvement mindset
- You architect, AI executes (the Orchestrator approach)

**Hattie B's Demo** (10 min)
- See the complete system in action
- Watch how emails flow through 7 agents
- Understand the "why" before we dive into the "how"

---

### Part 2: Knowledge Base Setup (0:20-1:05)

**Setup Check** (5 min)
Quick verification you're ready for hands-on work.

**What is RAG?** (10 min)
- Retrieval-Augmented Generation explained
- Static KB vs. Dynamic Tools
- Decision framework: What goes where?
- Agentic RAG: How agents use both KB and tools together

**Hands-On: Gemini File Search** (30 min)
- Launch The Stacks UI (`npx serve .` in `tools/kb-manager/`)
- Create your first knowledge base store
- Upload 3-5 business documents
- Test search queries
- Understand how your agents will use this

---

### Part 3: Content Strategy (1:05-1:40)

**The 5 Essential Documents** (15 min)
1. FAQ.md - Your top customer questions
2. Policies.md - Returns, shipping, guarantees
3. Catalog.md - Products/services overview
4. Company-Info.md - Hours, locations, contact
5. Brand-Voice.md - How you communicate

Plus: Website scraping options (optional, extracurricular)

**Personalizing Your Agents** (20 min)
- The 3 agents you'll customize: Sugar, Hatch, Holler
- Echo brand voice demo (live)
- Meta-prompting techniques
- Escalation triggers: When to flag for human review

---

### Part 4: Wrap-Up (1:40-2:00)

**Q&A + Setup Verification** (20 min)
- Open questions
- Troubleshoot any issues
- Clear homework checklist
- Preview Session 3 (building workshop)

---

## Your Homework (Before Session 3)

Complete these tasks before Wednesday, December 10:

### 1. Create Your Knowledge Base Content
Create 5 documents about your business:
- [ ] `faq.md` - 10-20 common customer questions with answers
- [ ] `policies.md` - Returns, shipping, guarantees, key terms
- [ ] `catalog.md` - Products/services with key features
- [ ] `company-info.md` - Hours, locations, contact methods, team
- [ ] `brand-voice.md` - Run Echo workflow with your writing samples

### 2. Upload to Gemini File Search
- [ ] Upload all 5 documents via The Stacks UI
- [ ] Test queries to verify content is searchable
- [ ] Save your Store ID for Session 3

### 3. Customize Your Agents
- [ ] Personalize Sugar prompt using YGM template + your brand voice
- [ ] List 10 escalation triggers (topics needing human review)
- [ ] Examples: refunds, complaints, legal questions, media inquiries

### 4. Prep for Testing
- [ ] Collect 3 sample customer emails from your business
- [ ] These will be used for end-to-end testing in Session 3

---

## What to Expect

**This Session Is About**:
- Understanding the system architecture
- Getting your knowledge base set up
- Learning the concepts (RAG, agents, HITL)
- Planning your content

**This Session Is NOT**:
- Building workflows in N8N (that's Session 3)
- Coding or technical implementation
- Perfect customization (rough drafts are fine)

**If You Get Stuck**:
- Claude Code can help with most tasks
- Session 2 (Friday, Dec 5) is Office Hours for troubleshooting
- Ask questions during or after the session

---

## Prerequisites

Before this session, make sure you have:
- [ ] VS Code + Claude Code extension installed
- [ ] GitHub CLI configured (`gh auth login`)
- [ ] Student repo cloned locally
- [ ] N8N Cloud account (Starter tier)
- [ ] Gemini API key from Google AI Studio
- [ ] Slack workspace for testing (can create during session if needed)
- [ ] 3-5 writing samples for brand voice analysis
- [ ] 3-5 business documents for initial KB upload

See [SETUP.md](../SETUP.md) for detailed instructions.

---

## Common Questions

**"I don't have much content yet - is that OK?"**
Yes! Start with what you have. Even 1-2 documents work. You can always add more later.

**"My business is different from a restaurant - will this still work?"**
Absolutely. The Hattie B's demo is just a reference. The system works for any business that handles customer emails.

**"I'm not technical - can I keep up?"**
Yes. This course is designed for non-technical entrepreneurs. Claude Code does the technical work. You provide the business knowledge and direction.

**"What if I can't finish all the homework?"**
Do what you can. Prioritize: (1) Get documents uploaded to KB, (2) Basic Sugar customization. We'll iterate together in Session 3.

**"How much time should I budget for homework?"**
Most students spend 4-6 hours creating the 5 documents and customizing prompts. Spread it across the week.

---

## Key Concepts to Remember

**Agentic RAG**: Your agents use both a static knowledge base (Gemini File Search) AND dynamic tools (Exa web search, Toast POS, etc.). Intelligence is in orchestration.

**Agent v1/v2 Pattern**: Sugar v1 and Sugar v2 have the same system instructions. The difference is the user prompt at the workflow level. v1 writes first draft, v2 revises based on feedback.

**Fisk Method**: 8-phase framework for systematically personalizing agent system instructions.

**TOAST Method**: 5-phase mindset for continuous improvement via observational evals ("it doesn't sound right" → iterate).

**Escalation != Off-Ramp**: When an agent flags something for escalation, it doesn't stop the workflow. It highlights it in Slack so you pay extra attention before approving.

---

## Resources

- [Architecture Overview](./architecture-overview.md) - Complete system diagram
- [The Stacks UI Guide](../tools/kb-manager/README.md) - KB management
- [Website Scraping Guide](./website-scraping-guide.md) - Optional content gathering
- [Brand Voice Guide](./brand-voice-guide.md) - Echo workflow walkthrough
- [Setup Troubleshooting](./troubleshooting-quick-ref.md) - Common issues

---

## Next Steps

**Session 2 (Friday, Dec 5)**: Office Hours
- Bring your questions and blockers
- Get help with homework
- One-on-one troubleshooting

**Session 3 (Wednesday, Dec 10)**: Building Workshop
- Import workflows to N8N with Claude Code's help
- Connect your KB and credentials
- Test end-to-end with your sample emails
- Iterate based on "it doesn't sound right"

---

*Questions? Ask during the session or bring them to Office Hours on Friday.*
