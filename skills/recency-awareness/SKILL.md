---
name: recency-awareness
description: Helps planning agents detect when research topics require current information and set explicit temporal constraints for the research process. Use this skill whenever creating research plans, especially for topics involving recent events, current developments, breaking news, ongoing situations, or any query with temporal markers like "latest", "current", "recent", specific dates (e.g., "March 2026"), or "what's happening now". Essential for ensuring downstream research agents gather appropriately recent sources.
---

# Recency Awareness Skill

This skill helps you recognize when a research topic is time-sensitive and communicate explicit temporal requirements to downstream research agents.

## When to Use This Skill

Use this skill when:
- Creating research plans or defining research tasks
- The user's query includes temporal markers ("latest", "current", "recent", "now", specific dates)
- The topic involves breaking news, ongoing events, or fast-moving situations
- The user asks "what's happening" rather than "what happened historically"
- You're planning research on topics that change frequently (politics, tech, markets, conflicts)
- Historical context exists but current state is the primary focus

## Why This Matters

Without explicit temporal guidance, research agents default to general searches that return a mix of old and new information. For current events, this means researchers might cite 2024 analysis for March 2026 events, or worse, not realize the sources are outdated. By detecting temporal requirements upfront and communicating them clearly in the research plan, you ensure all downstream work operates with the right time frame.

**The planning agent's role:** You're not doing the research - you're setting the guardrails. Your job is to recognize "this needs current info" and tell the research team exactly what "current" means for this task.

## Core Principles

### 1. Temporal Signal Detection

**Recognize when recency is critical by looking for explicit and implicit signals.**

**Explicit temporal signals:**

These are obvious markers that the user wants current information:

- **Specific recent dates:** "March 2026", "this month", "this week", "today"
- **Temporal qualifiers:** "latest", "current", "recent", "now", "up-to-date"
- **Present/ongoing tense:** "what is happening", "current status", "ongoing"
- **Comparative to now:** "since [recent date]", "from [month] to now"

**Examples:**
- ✅ "March 2026 US-Iran-Israel escalation" → Clear date signal
- ✅ "Latest developments in AI agent frameworks" → "Latest" signals recency
- ✅ "What is happening with the conflict" → Present tense signals current state
- ✅ "Stock market trends since January 2026" → Recent timeframe specified

**Implicit temporal signals:**

These suggest recency even without explicit markers:

- **Event type words:** "escalation", "crisis", "breaking", "developing", "emerging", "unfolding"
- **Dynamic topics:** Politics, conflicts, markets, technology trends, health outbreaks
- **Contrast with history:** "What's different now compared to..."
- **Forward-looking:** "predictions", "what's next", "where is this going"

**Examples:**
- ✅ "US-Iran-Israel escalation: what's next" → "Escalation" + "what's next" suggests ongoing situation
- ✅ "AI agent production deployments" → Fast-moving field, likely wants current state
- ✅ "Expert predictions for the conflict" → Predictions require current baseline

**Non-temporal signals:**

These suggest historical or general research, not current-events focus:

- ❌ "History of US-Iran relations" → Historical scope
- ❌ "How do neural networks work" → Stable technical knowledge
- ❌ "Analysis of the 2020 election" → Specific past event
- ❌ "Background on Middle East conflicts" → General background

**What to do:**
- **Scan the user's query** for temporal markers (explicit or implicit)
- **Consider the topic type:** Is this inherently time-sensitive?
- **Check the verbs:** "is happening" vs "happened" changes everything
- **When in doubt, ask yourself:** Would a 6-month-old source adequately answer this query?

### 2. Setting Explicit Temporal Requirements

**Once you've detected that recency matters, communicate specific requirements in the research plan.**

**Bad (vague):**
- "Find recent information about..."
- "Look for current sources"
- "Get the latest on..."

**Why it's bad:** "Recent" and "current" are ambiguous. Recent to whom? Current as of when? Researchers will interpret differently.

**Good (explicit):**
- "All sources must be dated February-March 2026 or later"
- "Prioritize sources from the last 30 days for breaking developments"
- "Historical sources (pre-2026) may be used for background context only, not for current status"

**Why it's good:** No ambiguity. Researchers know exactly what date range to search within and what counts as acceptable.

**How to set requirements:**

**For breaking news / very recent events:**
```
RECENCY REQUIREMENT:
- This research concerns events from [specific date range, e.g., March 10-20, 2026]
- Primary sources must be dated within this window or immediately after
- Sources more than 1 month old should not be used for "current status" claims
- If using older sources for context, label them explicitly as background
```

**For ongoing situations:**
```
RECENCY REQUIREMENT:
- This is an ongoing, fast-moving situation as of March 2026
- All analysis and status descriptions must be from March 2026 or the last 2-4 weeks
- Older sources may provide historical background but should not be cited for current state
- Researchers must verify publication dates on all sources
```

**For recent trend analysis:**
```
RECENCY REQUIREMENT:
- This research examines developments from [timeframe, e.g., 2025-2026]
- Sources should primarily be from this period
- For "current state" or "latest" claims, use sources from the last 2-3 months
- Older seminal works may be cited for foundational concepts
```

**Include in the plan:**
1. **Date window:** What range of publication dates is acceptable?
2. **Primary vs background:** Can older sources be used? For what purpose?
3. **Verification instruction:** Tell researchers to check dates explicitly
4. **Decay warning:** Note when older analysis might be outdated

### 3. Distinguishing Current State from Historical Context

**Help researchers understand when to prioritize recency vs when to include background.**

**Current state questions** (recency critical):
- "What is the current situation?"
- "What happened in March 2026?"
- "What are experts saying now?"
- "What's the latest development?"

**For these:** Recent sources only. Older sources are outdated.

**Historical context questions** (recency less critical):
- "What's the background of this conflict?"
- "How did we get here?"
- "What are the long-term causes?"

**For these:** Older sources are appropriate, but label them as historical.

**Mixed questions** (need both):
- "March 2026 escalation: timeline and predictions"
- "Current AI agent landscape: evolution and state-of-the-art"

**For these:** Recent sources for current state, older sources for background - but distinguish clearly.

**What to include in your plan:**

```
RESEARCH SCOPE:
1. Current Status (March 2026):
   - What events occurred in March 2026
   - What is the situation as of [today's date]
   - Sources: March 2026 only

2. Expert Analysis (predictions, assessments):
   - What do experts predict will happen next
   - How are analysts interpreting recent events
   - Sources: March 2026, must reflect knowledge of recent developments

3. Background Context (optional, if needed):
   - Historical tensions leading to this moment
   - Long-term trajectories
   - Sources: Can be older, but must be labeled as "historical context"

IMPORTANT: Do not mix historical and current analysis. Make clear which is which.
```

### 4. Temporal Decay Warnings

**Alert researchers when older analysis may be invalidated by recent events.**

**Why this matters:**
- A 2025 "prediction" about 2026 might be wrong now that 2026 has arrived
- Pre-escalation analysis doesn't account for post-escalation dynamics
- Old forecasts should be compared to actual outcomes, not cited as current wisdom

**What to flag:**

**Predictions vs reality:**
```
NOTE: Many sources from 2025 predicted X would happen in 2026.
Researchers should:
1. Find current sources that assess whether those predictions came true
2. Not cite old predictions as if they're current analysis
3. Compare prediction with outcome where relevant
```

**Pre-event vs post-event analysis:**
```
NOTE: Analysis from before March 15, 2026 does not account for the events of that date.
- Pre-March 15 sources may explain conditions leading to the escalation
- Post-March 15 sources analyze the escalation itself and its aftermath
- Researchers should not use pre-March 15 analysis to describe post-March 15 situations
```

**Rapidly evolving fields:**
```
NOTE: AI agent frameworks are evolving rapidly in 2026.
- Sources from Q1 2026 are current
- Sources from 2025 may be outdated (frameworks, best practices change quickly)
- Researchers should prioritize the most recent sources available
```

### 5. Communicating Requirements to Researchers

**Make your temporal requirements prominent and unambiguous in the research plan.**

**Plan structure template:**

```
RESEARCH TASK: [Topic]

TEMPORAL REQUIREMENTS: [This section should be prominent and early in the plan]
- Date range: [specific dates or relative timeframe]
- Primary source requirement: [what dates count as current]
- Background source usage: [when older sources are OK]
- Verification: Researchers must check publication date on every source
- Decay warning: [Any specific guidance about outdated analysis]

RESEARCH QUESTIONS:
1. [Question 1] - [requires current sources / allows background sources]
2. [Question 2] - [requires current sources / allows background sources]
...

APPROACH:
[How to conduct the research, including temporal search strategies]

DELIVERABLES:
- All sources must include publication dates in citations
- Distinguish between current analysis and historical context
```

**Key points:**
- **Put temporal requirements at the top** - don't bury them
- **Be specific about dates** - "February-March 2026", not "recent"
- **Tell researchers what to do** - "check publication dates", "prioritize last 30 days"
- **Give examples if helpful** - "Reuters March 20, 2026 is current; Reuters January 2025 is outdated"

## Practical Examples

### Example 1: Breaking Current Event

**User query:** "March 2026 US-Iran-Israel escalation: what happened, what's next, who's reporting what"

**Your temporal assessment:**
- Explicit signals: "March 2026" (specific recent month)
- Implicit signals: "escalation" (ongoing event), "what's next" (forward-looking)
- Topic type: Geopolitics, fast-moving, high stakes
- **Conclusion:** Recency is CRITICAL. Only March 2026 sources are relevant for current status.

**Temporal requirements to set:**

```
TEMPORAL REQUIREMENTS:
This research concerns events occurring in March 2026 (current month).

Date Requirements:
- Primary sources: Must be dated March 2026 or late February 2026
- Sources from January 2026 or earlier are OUTDATED for current status
- Older sources may be used only for historical background, and must be labeled as such

Specific Instructions:
- Check publication date on EVERY source before using it
- For "what happened": Only use sources from March 2026
- For "what's next" (predictions): Only use expert analysis from March 2026 that accounts for recent events
- For "who's reporting": Sample sources from March 2026 to show current media coverage

TEMPORAL DECAY WARNING:
Analysis from before March 2026 does not account for the March events.
Do not cite pre-March predictions or assessments as if they describe the current situation.
```

### Example 2: Recent Trend Analysis

**User query:** "Latest developments in AI agent frameworks and production deployments"

**Your temporal assessment:**
- Explicit signals: "Latest" (temporal qualifier)
- Implicit signals: "developments" (ongoing), AI agents (fast-moving field)
- Topic type: Technology trends, evolves quickly
- **Conclusion:** Recency is important. Last 3-6 months most relevant.

**Temporal requirements to set:**

```
TEMPORAL REQUIREMENTS:
This research examines the current state of AI agent frameworks (as of March 2026).

Date Requirements:
- Primary sources: Prefer sources from Q1 2026 (Jan-March 2026)
- Sources from Q3-Q4 2025 are acceptable for recent context
- Sources from before 2025 may be cited for foundational frameworks but should not be used to describe "current state"

Specific Instructions:
- AI/tech field moves fast - prioritize newest sources
- For "production deployments", find 2025-2026 case studies
- For "latest frameworks", search for releases and updates from last 6 months
- Older papers may be cited for established techniques but label them clearly

Note: A 2024 source saying "GPT-4 is state-of-the-art" is outdated.
```

### Example 3: Historical Topic (No Recency Requirement)

**User query:** "Background on US-Iran relations since 1979"

**Your temporal assessment:**
- Explicit signals: "since 1979" (historical timeframe)
- Implicit signals: "background" (context, not current events)
- Topic type: Historical analysis
- **Conclusion:** Recency is NOT critical. Scholarly, authoritative sources matter more than publication date.

**Temporal requirements to set:**

```
TEMPORAL REQUIREMENTS:
This research covers historical background (1979-present).

Date Requirements:
- Sources from any period are acceptable if they're authoritative
- Recent scholarly works (2020s) may provide good synthesis
- Contemporary sources from each era may be valuable for primary perspectives

Specific Instructions:
- Prioritize authoritative historical analysis (academic books, think tank retrospectives)
- Publication date is less important than authority and comprehensiveness
- If citing current events (2026), note that these are ongoing and not yet "history"

Note: This is a historical research task, not a current-events monitoring task.
```

## Integration with Other Skills

**Works with Search Strategy Skill:**
- You (Planning Agent with Recency Awareness) set temporal requirements
- Research Agent (with Search Strategy) executes temporal queries based on your requirements
- Your "sources must be from March 2026" becomes their "March 2026" in every search query

**Works with Source Validation Skill:**
- You set date requirements
- Source Validation enforces them by checking publication dates
- Both ensure temporal appropriateness

## Common Mistakes to Avoid

❌ **Vague temporal language**
- Bad: "Find recent sources"
- Fix: "Sources must be from March 2026"

❌ **No temporal requirement for current events**
- Bad: Research plan has no date guidance for "March 2026 escalation"
- Fix: Explicit date window at top of plan

❌ **Conflating historical and current questions**
- Bad: Treating "background on conflict" and "current status" as the same
- Fix: Separate research questions with different temporal requirements for each

❌ **Assuming researchers will figure it out**
- Bad: "The topic is current, so they'll know to use recent sources"
- Fix: Explicit instructions in the plan

❌ **Not warning about temporal decay**
- Bad: No mention that pre-event analysis is outdated
- Fix: "Note: Sources from before March 15 don't account for the March 15 incident"

## Quick Decision Tree

**Step 1:** Does the query have temporal markers?
- Explicit dates (March 2026, this month)? → YES, recency critical
- "Latest", "current", "recent", "now"? → YES, recency critical
- Present tense ("what is happening")? → YES, recency critical
- Implicit event words ("escalation", "breaking")? → YES, likely recency critical
- None of the above? → Continue to Step 2

**Step 2:** Is the topic inherently time-sensitive?
- Breaking news, ongoing conflict, market moves? → YES, recency critical
- Fast-moving tech field? → YES, recency important
- Stable technical knowledge, historical topic? → NO, recency not critical

**Step 3:** Set requirements based on conclusion
- If recency critical → Explicit date window, verification instructions, decay warnings
- If recency important → Prefer recent but allow some older with context
- If recency not critical → Focus on authority over date

---

**Remember:** Your job as the planning agent is to recognize when "current" matters and tell the research team exactly what "current" means. Explicit temporal requirements prevent wasted effort, missed information, and outdated analysis. When in doubt, err on the side of specificity - it's better to be clear than to assume researchers will infer your intent.
