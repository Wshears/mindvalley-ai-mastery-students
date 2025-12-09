# Component Reference Card

**Quick reference for all 7 agents and their supporting tools**

---

## The 7 Agents at a Glance

| Agent | Role | AI Model | Session |
|-------|------|----------|---------|
| **CinnaMon** | Sentiment Analyzer | Claude Sonnet | 1 |
| **Librarian** | KB Searcher | Gemini 2.5 Flash | 2 |
| **Hatch** | Expert Analyst | Claude Sonnet | 2 |
| **Sugar** | Email Drafter | Claude Sonnet | 2 |
| **Bishop** | QA Reviewer | Claude Sonnet | 3 |
| **Router** | Decision Maker | Claude Sonnet | 3 |
| **Holler** | HITL Notifier | N8N + Slack | 3 |

---

## Agent Details

### CinnaMon - Sentiment Analysis

| Property | Value |
|----------|-------|
| **Named After** | The spice that "adds warmth and complexity" |
| **Job** | Detect emotional temperature of emails |
| **Outputs** | Emotion, urgency (1-5), themes, recommended tone |
| **Pipeline Position** | First agent - sets context for all others |

**Key Output:** Tells downstream agents whether customer is happy, frustrated, or angry.

---

### Librarian - Knowledge Retrieval

| Property | Value |
|----------|-------|
| **Named After** | Finds books but doesn't write essays |
| **Job** | Search your knowledge base for relevant info |
| **Model** | **MUST use Gemini** (File Search requirement) |
| **Outputs** | Retrieved chunks, confidence scores, gaps |

**Key Feature:** Knows all your document stores and picks the right ones to search.

---

### Hatch - Expert Agent

| Property | Value |
|----------|-------|
| **Named After** | Hatching ideas / incubating solutions |
| **Job** | Synthesize information, provide expertise |
| **Available Tools** | Librarian (KB), Research Agent (web search) |
| **Outputs** | Comprehensive answer, recommendations |

**Superpower:** Can search the web for current info (wait times, news, etc).

---

### Sugar - Email Drafter (You've Got Mail)

| Property | Value |
|----------|-------|
| **Named After** | "Sugar" as Southern term of endearment |
| **Job** | Write email responses in YOUR voice |
| **Customization** | **HIGH** - this is where your personality shines |
| **Outputs** | Draft email matching your brand voice |

**This is the agent you'll customize most.** Your writing samples train Sugar.

---

### Bishop - QA Agent

| Property | Value |
|----------|-------|
| **Named After** | Chess piece (strategic reviewer) |
| **Job** | Quality check before sending |
| **Checks** | Facts, completeness, tone, safety, brand voice |
| **Outputs** | SHIP / REVISE / ESCALATE |

**Verdicts:**
- **SHIP** → Send immediately
- **REVISE** → Needs fixes (loops back to Sugar)
- **ESCALATE** → Needs human judgment

---

### Router - Decision Maker

| Property | Value |
|----------|-------|
| **Named After** | Network router (directs traffic) |
| **Job** | Execute Bishop's verdict |
| **Pipeline Position** | Final decision point |
| **Outputs** | Route to Send or Holler |

---

### Holler - HITL Notifier

| Property | Value |
|----------|-------|
| **Named After** | Nashville "Holler and Swaller" toast |
| **Job** | Get human input when AI can't decide |
| **Integration** | Slack |
| **Outputs** | Formatted message with context + options |

**You reply in Slack:** "ship", "revise: [feedback]", or "custom: [your text]"

---

## Supporting Tools

| Tool | Purpose | Used By |
|------|---------|---------|
| **Gemini File Search** | Document storage + search | Librarian |
| **Research Agent** | Web search for current info | Hatch |
| **N8N Cloud** | Workflow automation | All |
| **Gmail** | Email trigger + send | Input/Output |
| **Slack** | Human notifications | Holler |
| **Google Sheets** | Audit trail | All workflows |

---

## Model Requirements

| Agent | Model | Why |
|-------|-------|-----|
| Most agents | Claude Sonnet | Best reasoning |
| **Librarian** | **Gemini** | File Search is Gemini-only |
| Holler | N8N native | Just formatting |

---

## What You Customize

| Agent | Level | What to Change |
|-------|-------|----------------|
| CinnaMon | Low | Rarely touched |
| Librarian | Low | Just store IDs |
| Hatch | Medium | Domain expertise |
| **Sugar** | **HIGH** | Your brand voice |
| Bishop | Medium | QA criteria |
| Router | Low | Routing rules |
| **Holler** | **HIGH** | Slack format, triggers |

---

*Print this. Reference it often. Know your team.*
