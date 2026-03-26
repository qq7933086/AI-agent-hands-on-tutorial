---
name: search-strategy
description: Guides research agents to formulate effective search queries with temporal filters and source diversification for fast-moving, current events research. Use this skill whenever researching recent developments, breaking news, current events, ongoing situations, or any time-sensitive topic that requires finding the most recent and relevant information. This skill is essential when the user asks about "latest", "current", "recent", "2026", specific recent dates, or trending topics.
---

# Search Strategy Skill

This skill helps you find the most current, relevant, and diverse information when researching fast-moving topics and current events.

## When to Use This Skill

Use this skill when:
- Researching recent events, breaking news, or developing situations
- The user specifies dates (e.g., "March 2026"), temporal qualifiers ("latest", "current", "recent"), or trending topics
- Information currency is critical (political events, tech developments, market changes)
- You need to distinguish between historical context and current status
- The topic evolves rapidly and older sources may be outdated

## Why This Matters

Generic search queries often return outdated information because they don't specify temporal constraints or source types. For current events, a query like "US Iran conflict" might return analysis from 2023-2024, completely missing recent March 2026 developments. By using temporal qualifiers, targeted source searches, and adaptive query refinement, you ensure that your research reflects the actual current state rather than historical patterns.

## Core Principles

### 1. Temporal Query Construction

**Include time markers in every search query** to ensure results are recent and relevant.

**Temporal qualifiers to use:**
- Specific dates: "March 2026", "March 15 2026", "week of March 10"
- Relative terms: "latest", "recent", "current", "this month", "this week"
- Range indicators: "since March 2026", "February-March 2026"

**Example transformations:**
- ❌ Generic: "US Iran Israel conflict"
- ✅ Time-aware: "US Iran Israel tensions March 2026"

**When to use date filters:**
- For breaking news: Limit to last 24-48 hours
- For ongoing situations: Limit to last 7-30 days
- For monthly topics: Limit to current or previous month

**Why this works:** Search engines and databases prioritize recency when temporal markers are present. Without them, you get a mix of old and new with no temporal ordering.

### 2. Progressive Query Refinement

Start with broad queries to understand the landscape, then narrow based on what you discover.

**Three-stage approach:**

**Stage 1 - Broad Overview:**
- Goal: Understand the current situation and identify key entities/events
- Example: "US Iran Israel tensions March 2026"
- What to look for: Recent headlines, key incidents, major players

**Stage 2 - Focused Investigation:**
- Goal: Deep-dive into specific incidents, statements, or developments
- Example: "US Iran [specific incident name] March 20 2026"
- What to look for: Detailed accounts, official statements, expert commentary

**Stage 3 - Expert Analysis:**
- Goal: Find authoritative interpretation and predictions
- Example: "CSIS analysis US Iran March 2026" or "[expert name] Iran assessment 2026"
- What to look for: Think tank reports, academic analysis, expert opinions

**Why this works:** Broad queries reveal the landscape; narrow queries get details. Jumping straight to narrow queries risks missing important context or searching for the wrong things.

### 3. Source Type Diversification

Different source types provide different perspectives and levels of authority. Target multiple types to build a comprehensive, well-sourced view.

**Source categories to search:**

**Think Tanks & Research Organizations:**
- Examples: CSIS, Council on Foreign Relations, IISS, Carnegie Endowment, Brookings
- Query format: "[org name] + [topic] + [date]"
- Why: Provide analytical depth, expert perspective, and contextual interpretation

**Government & Official Sources:**
- Examples: State Department, Pentagon, official statements, press briefings
- Query format: "[department/agency] + [topic] + 'statement' OR 'briefing' + [date]"
- Why: Primary sources for policy positions and official positions

**Major News Agencies:**
- Examples: Reuters, Associated Press, BBC, AFP, Bloomberg
- Query format: "[news org] + [topic] + [date]"
- Why: Breaking news, fact-based reporting, wide coverage

**Academic & Specialized Publications:**
- Examples: Foreign Affairs, Foreign Policy, International Security journals
- Query format: "[publication] + [topic] + [year]"
- Why: In-depth analysis, theoretical frameworks, peer review

**Regional & Local Sources:**
- Examples: Gulf News, Haaretz, Tehran Times (for regional perspectives)
- Query format: "[regional source] + [topic] + [date]"
- Why: Local context, perspectives not available in Western media

**Search strategy:**
Don't rely on generic web search alone. Explicitly search for each source type:
1. Start with news agencies for breaking developments
2. Check government sources for official positions
3. Search think tanks for analysis and predictions
4. Consult academic sources for theoretical context
5. Include regional sources for diverse perspectives

**Why this works:** Each source type has strengths. News is fast but shallow; think tanks are analytical but slower; government sources are authoritative but narrow. Combining them gives you speed, depth, authority, and perspective.

### 4. Adaptive Follow-up Searching

As you find information, let it guide your next searches. Good research is iterative.

**Trigger follow-up searches when you encounter:**

**Mentioned but unexplained incidents:**
- Finding: "Following the March 15 incident, tensions escalated..."
- Follow-up: Search specifically for "March 15 2026 US Iran incident" or "[incident name] March 15"

**Quoted experts or officials:**
- Finding: Article quotes "Dr. Jane Smith from RAND says..."
- Follow-up: Search for "Jane Smith RAND Iran analysis 2026" to find her full commentary

**Referenced reports or documents:**
- Finding: "According to the recent IISS assessment..."
- Follow-up: Search for "IISS Iran assessment 2026" to find the original report

**Conflicting information:**
- Finding: Source A says X happened on March 15; Source B says March 17
- Follow-up: Search for "US Iran [event] timeline March 2026" or check authoritative news agencies

**Incomplete data:**
- Finding: Article mentions "several casualties" without numbers
- Follow-up: Search for "[specific incident] casualties confirmed" from authoritative sources

**Why this works:** Initial searches won't answer everything. Following threads leads you to more specific, authoritative, or complete information. It's how journalists and researchers actually work.

## Practical Application

**For a research task about "March 2026 US-Iran-Israel escalation":**

**Step 1 - Establish current state (5 minutes):**
```
Query 1: "US Iran Israel tensions March 2026"
Query 2: "US Iran Israel latest developments March 2026"
Query 3: "US Iran Israel escalation March 2026 timeline"
```
Goal: Understand what happened and when

**Step 2 - Gather authoritative sources (10 minutes):**
```
Query 4: "Reuters US Iran March 2026"
Query 5: "AP Israel Iran March 2026"
Query 6: "CSIS Iran analysis March 2026"
Query 7: "State Department Iran statement March 2026"
```
Goal: Build source base with diverse types

**Step 3 - Deep-dive on specifics (10 minutes):**
```
Query 8: "[specific incident from Step 1] details"
Query 9: "[key expert quoted] full analysis"
Query 10: "[think tank] Iran assessment 2026"
```
Goal: Get depth on key developments

**Step 4 - Expert predictions (5 minutes):**
```
Query 11: "experts predict US Iran 2026"
Query 12: "[specific analyst] Iran forecast 2026"
```
Goal: Capture forward-looking analysis

## Common Mistakes to Avoid

❌ **Generic, timeless queries**
- Bad: "US Iran conflict"
- Why it fails: Returns mix of 2023-2025 content
- Fix: "US Iran tensions March 2026"

❌ **Accepting first-page results without date verification**
- Bad: Using a 2025 analysis for a March 2026 query
- Why it fails: Search engines don't perfectly filter by date; you must verify
- Fix: Check publication date on every source before using it

❌ **Single-source dependence**
- Bad: Finding one good article and stopping
- Why it fails: Misses other perspectives, can't cross-verify, may miss key info
- Fix: Always gather from multiple source types (news + think tank + government, minimum)

❌ **Rigid query formulas**
- Bad: Always using exact same query structure
- Why it fails: Different databases and search engines respond differently to phrasing
- Fix: Vary phrasing ("tensions" vs "escalation" vs "crisis"), try synonyms, reorder terms

❌ **Ignoring negative results**
- Bad: Not searching when initial queries return nothing
- Why it fails: Info might exist under different terms or in specialized databases
- Fix: Reformulate with synonyms, try specific source searches, broaden or narrow scope

## Integration with Other Skills

This skill works best in combination with:

**Source Validation Skill:**
- Search Strategy finds sources → Source Validation assesses their credibility
- Use temporal queries to find recent sources, then validate their authority and bias

**Recency Awareness Skill:**
- Recency Awareness sets the temporal requirements → Search Strategy executes them
- If the planning agent says "all sources must be from Feb-March 2026", your queries must include those temporal markers

## Quick Reference

**Building a good current-events query:**
1. Start with topic keywords
2. Add temporal qualifier (date, "latest", "recent")
3. Optionally add source type (Reuters, CSIS, State Department)
4. Optionally add outcome type ("analysis", "timeline", "statement")

**Template:** `[topic] + [temporal] + [optional: source] + [optional: type]`

**Examples:**
- "US Iran Israel tensions March 2026"
- "US Iran latest CSIS analysis"
- "State Department Iran statement March 20 2026"
- "Reuters Iran timeline March 2026"

---

**Remember:** The goal is not just to search, but to search *strategically* so you find information that is current, authoritative, diverse, and comprehensive. Generic queries return generic results. Targeted, adaptive, time-aware queries return exactly what you need.
