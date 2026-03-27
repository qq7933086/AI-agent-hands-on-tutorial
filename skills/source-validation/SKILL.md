---
name: source-validation
description: Validates source credibility, publication dates, and cross-references factual claims before including them in research reports. Use this skill whenever gathering information from web sources, news articles, reports, or any external content that will be cited in your output. Essential for research tasks, fact-checking, report writing, and any work where source reliability matters. Always use when the user asks for research, analysis, or information synthesis from multiple sources.
---

# Source Validation Skill

This skill helps you assess source credibility, verify publication dates, cross-reference claims, and build trustworthy, well-cited research outputs.

## When to Use This Skill

Use this skill when:
- Gathering information from web sources, news articles, or reports
- Creating research reports, briefings, or analyses that will be shared
- Working with topics where misinformation is common (politics, health, breaking news)
- The user needs citations or references for the information provided
- Combining information from multiple sources
- Fact-checking or verifying claims

## Why This Matters

Not all sources are created equal. A research report citing unreliable sources, outdated information, or unverified claims is worse than useless — it's actively misleading. By systematically validating every source, you ensure that your output is trustworthy, defensible, and useful. This skill is especially critical for current events, controversial topics, and high-stakes decisions where accuracy matters.

## Core Principles

### 1. Publication Date Verification

**Always check and record the publication date for every source you use.**

**Why date matters:**
- For current events: a 2-month-old source may be completely outdated
- For fast-moving topics: even a 1-week-old analysis can miss critical developments
- For temporal claims: "the current situation" from 2024 is not "current" in 2026
- For user trust: citing old sources as if they're current destroys credibility

**How to verify dates:**
1. **Look for explicit publication date:** Most articles have "Published: [date]" or "Last updated: [date]"
2. **Check article metadata:** HTML meta tags often contain publication dates even if not displayed
3. **Examine URL:** Some URLs include dates (e.g., `/2026/03/15/article`)
4. **Check references:** If an article cites very old sources, it's probably old too
5. **Look for temporal context clues:** Mentions of "this week", "yesterday", or specific dated events

**Date relevance rules:**

For **current events** (breaking news, ongoing situations):
- ✅ Sources from within the last 7-30 days are current
- ⚠️ Sources 1-3 months old may provide background but shouldn't be cited for "current status"
- ❌ Sources 6+ months old are historical context only

For **recent developments** (2026 topics when it's March 2026):
- ✅ Sources from the specified time period (e.g., Feb-March 2026 for a March event)
- ⚠️ Sources from the prior few months may provide relevant background
- ❌ Sources from 2025 or earlier are outdated unless used explicitly as historical context

For **general research** (stable topics):
- ✅ Sources from the last 1-2 years are usually fine
- ⚠️ Sources 3-5 years old may be dated depending on the field
- ❌ Sources 10+ years old should be used sparingly unless they're seminal works

**What to do:**
- **Include publication date in every citation:** "According to CSIS analysis (March 15, 2026)..."
- **Flag outdated sources:** "Historical context from 2024 analysis shows..."
- **Note when sources conflict on dates:** "Reuters reports March 17; AP reports March 18"

### 2. Authority Assessment

**Evaluate the credibility and expertise of every source before relying on it.**

**Three-tier authority system:**

**✅ Tier 1: Highly Authoritative**
- Established think tanks: CSIS, CFR, IISS, Carnegie, Brookings, RAND
- Major news agencies: Reuters, AP, AFP, BBC, Bloomberg (news division)
- Government officials and agencies: State Department, Pentagon, official statements
- Peer-reviewed academic journals: Foreign Affairs, International Security
- Subject-matter experts with credentials: professors, researchers, former officials in relevant domains

**When to use:** Primary sources for factual claims, analysis, and expert opinion

**⚠️ Tier 2: Moderately Authoritative**
- Reputable regional/national news outlets: The Guardian, NYT, Washington Post, WSJ
- Credentialed independent analysts with track record
- Industry publications in their domain: Defense News for military, Financial Times for economics
- University research centers and policy institutes
- Respectable international sources: Al Jazeera English, Deutsche Welle

**When to use:** Supporting sources, additional perspectives, detail on specific topics

**❌ Tier 3: Low Authority / Requires Verification**
- Unknown blogs, personal websites
- Social media posts (Twitter/X, Facebook, Reddit)
- Unverified or anonymous sources
- Tabloids and sensationalist outlets
- Sources with obvious commercial or political incentives
- Aggregators without original reporting

**When to use:** Can be cited *if* the claim is verified independently by Tier 1/2 sources, or if you're analyzing what "some sources claim" vs. "what's verified"

**How to assess authority:**

1. **Check the organization:**
   - Is it well-known in the relevant field?
   - Does it have a track record of accurate reporting/analysis?
   - Google "[organization name] + credibility" or "reliability" if uncertain

2. **Check the author:**
   - Does the author have relevant credentials (PhD in relevant field, former government role, years of coverage)?
   - Have they written other credible work on this topic?
   - Are they quoted or cited by Tier 1 sources?

3. **Check for bias/agenda:**
   - Does the source have a clear political, national, or commercial bias?
   - Note it, but don't automatically discard - just label the framing
   - Example: "Iranian state media reports X" vs. "Reuters reports Y" - both useful, different perspectives

4. **Check citations in the source itself:**
   - Does the source cite primary documents, official statements, or other credible sources?
   - Or does it cite anonymous sources, "sources say", or no sources at all?

**What to do:**
- **Prioritize Tier 1 sources** for key factual claims
- **Note source type in citations:** "According to CSIS (Tier 1 think tank)..." or "Regional outlet Gulf News reports..."
- **Flag questionable sources:** "Unverified social media reports claim... [we could not confirm this with Tier 1 sources]"

### 3. Claim Cross-Reference

**Never rely on a single source for important factual claims. Verify through independent corroboration.**

**What needs cross-referencing:**

**Must cross-reference:**
- Dates and timing of events ("incident occurred on March 15")
- Casualty figures or damage assessments
- Attribution of responsibility ("Iran said...", "US stated...")
- Direct quotes from officials or experts
- Specific policy announcements or decisions

**Good to cross-reference:**
- Expert predictions or forecasts
- Analytical conclusions
- Background/historical facts that are specific rather than widely known

**No need to cross-reference:**
- Widely known facts ("the US and Iran have had tensions since 1979")
- The source's own analysis or opinion (one expert's view doesn't need corroboration)
- Information that's already cited to an authoritative primary source

**How to cross-reference:**

1. **Find independent sources:**
   - Not: Reuters original report + AP report citing Reuters
   - Yes: Reuters independent reporting + AP independent reporting

2. **Check consistency:**
   - Do the sources agree on key facts (dates, numbers, quotes)?
   - If they disagree, which is more authoritative or has better sourcing?

3. **Handle discrepancies:**
   - **Minor differences:** "Reuters reports 'dozens' injured; AP reports '20-30 injured'" - both acceptable, note both
   - **Major conflicts:** "Source A says March 15; Source B says March 18" - investigate further, cite both, or flag as unclear
   - **Unverifiable claims:** "Only Source A reports this, no corroboration found" - label as unverified

**What to do:**
- **For critical claims:** Find at least 2 independent Tier 1/2 sources
- **Flag unverified claims:** "According to [source], [claim]. We could not independently verify this."
- **Note consensus:** "Multiple sources confirm that..."
- **Note discrepancies:** "Reports differ on timing: Reuters says X, AP says Y"

### 4. Bias Awareness

**Recognize and note source bias without necessarily discarding the source.**

**Common bias types:**

**National/Government Sources:**
- US State Department → US perspective
- Iranian state media → Iranian government perspective
- Israeli Defense Forces → Israeli military perspective
- **What to do:** Cite as "[country] sources report..." and include other national perspectives for balance

**Political/Ideological:**
- Some think tanks lean conservative/liberal
- Some outlets have editorial slants
- **What to do:** Use a mix of sources across the spectrum; note when a source has a known lean if relevant

**Commercial:**
- Industry-funded research may minimize risks
- Company press releases present best-case scenarios
- **What to do:** Verify claims with independent sources; note funding sources if relevant

**Regional:**
- Regional sources may emphasize local impacts
- May have more detail but less global context
- **What to do:** Balance regional detail with international perspective

**How to handle bias:**

1. **Include, don't exclude:** Biased sources still provide valuable perspective
2. **Note the framing:** "Iranian state media reports..." vs. "US officials state..."
3. **Seek balance:** If quoting US position, also seek Iranian/Israeli/international perspectives
4. **Separate facts from interpretation:** "Reuters reports [factual event]" vs. "Commentary from [org] interprets this as..."

**What to do:**
- **Explicit labeling:** "According to US officials..." "Iranian state media reports..."
- **Balanced sourcing:** Include multiple perspectives on controversial topics
- **Distinguish fact from spin:** "X happened [fact from multiple sources]. US officials interpret this as Y; Iranian sources interpret as Z."

### 5. Citation Standards

**Format all citations consistently and with sufficient information for the reader to assess the source.**

**Minimum citation requirements:**

1. **Source name/organization**
2. **Publication date** (critical!)
3. **Article/report title** (if available and relevant)
4. **Author** (if the author's credentials matter)

**Citation format examples:**

**News article:**
- "According to Reuters report (March 20, 2026), tensions escalated following..."

**Think tank analysis:**
- "CSIS analysis (March 15, 2026) suggests that..."
- Or with author: "Dr. Jane Smith of CSIS writes (March 15, 2026) that..."

**Government source:**
- "State Department spokesperson stated (March 18, 2026) that..."
- "Pentagon briefing (March 19, 2026) confirmed..."

**Expert opinion:**
- "Dr. John Doe, Middle East expert at Georgetown, told Foreign Policy (March 17, 2026) that..."

**When source authority matters:**
- "Tier 1 think tank CSIS reports (March 15, 2026)..."
- "Peer-reviewed analysis in Foreign Affairs (March 2026 issue)..."

**Unverified claims:**
- "Social media reports claim X, though this has not been confirmed by major news agencies."
- "According to unverified sources reported by [outlet], ... We could not independently confirm this claim."

### 6. Red Flags: What to Reject

**Some sources should not be used, period.**

❌ **Reject sources that:**

1. **Have no identifiable author or organization**
   - Anonymous blog posts, unsigned articles with no organizational attribution
   - Exception: Institutional publications that are unsigned (like "Reuters" or "AP" wire stories)

2. **Make extraordinary claims without evidence**
   - "Secret documents reveal..." with no documents shown
   - Dramatic claims not reported anywhere else
   - Conspiracy theories without credible sourcing

3. **Are clearly dated before the events they describe**
   - 2024 article claiming to describe March 2026 events (impossible)
   - Watch for republished/updated content with misleading dates

4. **Appear to be disinformation or propaganda**
   - Outlets known for spreading falsehoods
   - Content that seems designed to manipulate rather than inform
   - Note: State media (RT, Press TV, Xinhua) is biased but not necessarily "disinformation" - label it clearly and use with awareness

5. **Have clear undisclosed conflicts of interest**
   - Weapons manufacturer "analysis" on why more weapons are needed
   - Undisclosed sponsored content presented as journalism

6. **Are satirical or entertainment**
   - The Onion, Babylon Bee, etc. (obviously satire)
   - Opinion columns presented as news (use opinion carefully, label it)

**When in doubt:** Note the limitation and cite with caveats, or exclude entirely.

## Practical Workflow

**For each source you find:**

1. ✅ **Check publication date** → Include in citation
2. ✅ **Assess authority** (Tier 1/2/3) → Prioritize Tier 1 for key claims
3. ✅ **Note any bias** → Label perspective if relevant
4. ✅ **Cross-reference important claims** → Find 2+ independent sources for critical facts
5. ✅ **Format citation** → Source + date + context
6. ✅ **Screen for red flags** → Reject if clearly unreliable

**Example validation process:**

Found source: "US-Iran tensions escalate after March 15 incident - Analysis by Middle East Policy Institute (MEPI), March 18, 2026"

1. **Date:** March 18, 2026 ✅ (recent and relevant)
2. **Authority:** Check MEPI → not a major think tank, but has credentialed experts → Tier 2 ⚠️
3. **Claims:** "March 15 incident", "tensions escalate"
   - Cross-check: Reuters also reports March 15 incident ✅
   - AP confirms tensions escalated ✅
4. **Bias:** Check MEPI background → no obvious bias
5. **Citation:** "Middle East Policy Institute analysis (March 18, 2026) suggests..."
6. **Conclusion:** Use for analytical perspective, but verify factual claims against Tier 1

## Integration with Other Skills

**Works with Search Strategy Skill:**
- Search Strategy finds sources → Source Validation assesses them
- Both skills should prioritize recent, authoritative sources

**Works with Recency Awareness Skill:**
- Recency Awareness sets date requirements → Source Validation enforces them
- Both ensure temporal appropriateness of sources

## Quick Reference Checklist

Before citing a source, ask:

- [ ] Have I verified the publication date?
- [ ] Have I assessed the source's authority (Tier 1/2/3)?
- [ ] If making a factual claim, have I cross-referenced it?
- [ ] Have I noted any bias or perspective framing?
- [ ] Does the citation include source name and date?
- [ ] Are there any red flags that should disqualify this source?

If all checks pass → cite with confidence
If some checks fail → use with caveats or seek better sources
If red flags present → exclude entirely

---

**Remember:** Your research is only as good as your sources. Rigorous source validation isn't about being pedantic - it's about ensuring that what you deliver is trustworthy, accurate, and defensible. When users rely on your output for decisions, your validation process is what gives them confidence.
