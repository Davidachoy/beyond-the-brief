# Beyond the Brief

**Research the questions you haven't thought to ask.**

Beyond the Brief is an AI research skill for understanding a decision before committing money or time. It turns “I want to do X” into an investigation of what that really involves, including hidden costs, practical difficulties, local requirements, and problems people often discover too late.

## The problem it solves

When entering an unfamiliar field, you usually know what you want to achieve but not everything you need to investigate. Your initial questions may cover the obvious benefits and first steps while missing maintenance, obligations, day-to-day work, failure modes, or the cost of changing your mind.

An AI answer can follow that same incomplete brief and still sound convincing. Beyond the Brief gives the assistant a repeatable method for expanding the questions, checking real sources, and explaining the uncertainties that matter to your decision.

For example, researching a rental property should go beyond purchase prices and advertised rent. Depending on the location, the research may also need to examine ownership restrictions, vacancy, unpaid rent, repairs, insurance, taxes, financing, management work, and selling costs. The same approach applies to starting a business, taking up an activity, or choosing a learning path.

## What the skill does

- Establishes the context that changes the answer, such as location, experience, budget, and timeframe.
- Expands the research to relevant questions you have not explicitly asked.
- Combines primary sources with firsthand experiences from local forums, communities, interviews, and accessible videos.
- Looks for both favorable outcomes and failures, including accounts from people who quit.
- Examines total costs, ongoing effort, dependencies, and consequences that emerge later.
- Distinguishes verified facts, personal experiences, calculations, assumptions, and inferences.
- Produces practical checks before acting, decision criteria, and a small next step that reduces uncertainty.
- Identifies what could not be covered and separates decision-blocking gaps from optional follow-up topics.

It adapts to the topic. A learning project needs prerequisites, practice time, feedback, and progress indicators; it does not automatically need an investment analysis.

## Requirements

This is an instruction-based skill: it does not run scripts, install packages, or add a search service.

Use it with an AI assistant that can load skills. Full research requires search and browsing tools provided by that assistant. Access to video content, transcripts, private communities, and paid sources depends on the tools and permissions available.

If a source cannot be accessed, the assistant should say so. Without browsing, the skill calls for a clearly labeled preliminary analysis and a verification plan rather than claiming that research has been completed.

## Install in Codex

From a local copy of this repository, copy the skill files into your personal skills directory:

```bash
mkdir -p "$HOME/.agents/skills/beyond-the-brief/agents"
cp SKILL.md "$HOME/.agents/skills/beyond-the-brief/SKILL.md"
cp agents/openai.yaml "$HOME/.agents/skills/beyond-the-brief/agents/openai.yaml"
```

These commands install the current version and replace those two files if an earlier version is already present. Keep a copy first if you have customized them.

Codex detects local skill changes automatically. If the skill does not appear, restart Codex. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for local discovery and configuration.

## How to use it

Invoke the skill with `$beyond-the-brief` and describe what you want to explore. Include your location when local rules or prices matter, along with any known budget, experience, timeframe, and constraints. You do not need to know all the right questions in advance.

### General starting prompt

```text
Use $beyond-the-brief to research [idea or activity] before I commit.

My context: [location, experience, resources, and timeframe, if known].

Help me understand what it really involves, including firsthand experiences,
hidden costs, common mistakes, and problems people tend to discover too late.
Show your sources, what I should verify before acting, and what remains uncertain.
```

### Buying a rental property

```text
Use $beyond-the-brief. I want to buy a property to rent out in [city, country].
I am a beginner and my approximate budget is [amount and currency].

Investigate the local requirements, rental demand, total costs, financing,
ongoing work, and firsthand experiences of landlords, including failures.
Explain which checks I should complete before considering a purchase.
```

### Starting a business

```text
Use $beyond-the-brief to research opening a small bakery in [city, country].
I have [experience] and [available resources].

Investigate permits, startup and operating costs, suppliers, daily workload,
customer demand, margins, and reasons similar businesses struggle or close.
Compare practical alternatives and identify the assumptions I need to test.
```

### Learning a new skill

```text
Use $beyond-the-brief to investigate learning photography from scratch.
I can spend [hours] per week and my goal is [outcome].

Research prerequisites, equipment trade-offs, realistic practice requirements,
common beginner mistakes, and ways to get useful feedback. Suggest a small
starting experiment before I spend heavily on equipment or courses.
```

The instructions are written in English, but the assistant should respond in your language. You can invoke the skill in Spanish or another language without translating your request.

## What to expect

The structure varies with the topic, but a useful report should explain:

1. What the idea involves and the conditions under which it may work.
2. Important findings with sources beside the claims.
3. Full costs and effort, where relevant.
4. Overlooked issues, warning signs, and how to check them.
5. Evidence for and against the idea, plus relevant alternatives.
6. A prioritized checklist with criteria for proceeding, pausing, or ruling out an option.
7. Unresolved questions, why they matter, and how to investigate them next.

## Scope and limits

Beyond the Brief supports research and preparation. It does not authorize purchases, registrations, publishing, contacting people, or executing your decision.

Anecdotes can reveal useful questions but do not establish how common an outcome is. Estimates depend on their assumptions, and a long report does not prove complete coverage. The skill should make those limits visible and specify when documents, inspections, or professional review are still needed.

The skill's file structure has been validated. Its research behavior has not yet been evaluated through an end-to-end real-world investigation.

## Repository contents

```text
beyond-the-brief/
├── SKILL.md              # Research workflow and discovery metadata
├── agents/
│   └── openai.yaml       # Display name and default invocation prompt
└── README.md             # Purpose, installation, and usage
```
