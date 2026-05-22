# Master documentation style guide
## Hackmamba Technical Writer Course — Complete resource reference

This document combines every rule, principle, and standard from the Hackmamba Technical Writer Course. Use it as your first reference before writing any documentation. If a situation isn't covered here, check the Google Developer Documentation Style Guide.

**Resource coverage:** 39 of 45 curriculum resources reviewed and incorporated. Six resources are YouTube videos or unavailable pages that could not be transcribed (noted below).

---

## Part 1: The four documentation principles

Every piece of documentation must meet all four principles before it's ready to publish.

**1. User-focused**
Write for what the user wants to do, not what the tool is. Every heading describes a user task or outcome, not a product feature.

Tool-focused (wrong): "Table Editor", "Metrics Tool"
User-focused (right): "Edit a table", "Count records in a file"

**2. Trustworthy**
Verify every claim against the live product before publishing. Don't write from memory. Perform every step you document. One error makes users question everything else, even the correct parts.

**3. Easy to understand**
Reduce how hard the reader has to think. Use plain language, active voice, second person, and short sentences. If a sentence is hard to write, it's hard to read.

**4. Easy to find**
Structure content around how users think and move through tasks, not around how the product is built. Organize by task intent, not by feature.

---

## Part 2: Quality rubric

The single scoring tool for self-review, peer review, and gate reviews.

| Criterion | 1 (Needs work) | 3 (Developing) | 5 (Production-ready) | Weight |
|---|---|---|---|---|
| Technical accuracy | Factual errors or untested code | Mostly accurate, minor gaps | Fully verified, all code tested | 25% |
| Clarity | Dense, jargon-heavy, passive voice | Generally clear, occasional issues | Plain language, scannable, concise | 20% |
| Structure | Disorganized or tool-focused | Logical, could improve flow | Task-focused, intuitive hierarchy | 20% |
| Usability | Cannot follow the steps | Followable with some guesswork | User completes task unaided | 15% |
| Style compliance | Ignores style guide | Follows most conventions | Fully compliant | 10% |
| Completeness | Missing critical sections | Main content, minor gaps | All sections present, thorough | 10% |

**Weighted score calculation:** multiply each score (1-5) by its weight percentage. Maximum is 5.00.

---

## Part 3: Six AI guardrails

Apply to every piece of content that involved AI assistance.

1. **Verify every claim.** No AI-generated technical statement goes to production without manual verification against the product, API, or codebase.
2. **Test every code sample.** Every code example must execute in the actual environment before publishing. Expected output must match what the reader will actually see.
3. **Own the voice.** AI drafts are raw material. Rewrite for voice, tone, and style compliance. Never publish AI output as-is.
4. **Disclose when uncertain.** If AI provides something you can't verify, flag it for technical review. Don't publish.
5. **No AI for final review.** AI can do pre-review checks. Final quality review is always human.
6. **Track AI-assisted sections.** Note which sections were AI-assisted so reviewers can evaluate your editorial judgment.

---

## Part 4: Writing style rules

### 4.1 Voice and person
- Write in second person throughout. Use "you" and "your." Never use "we," "let's," or "our" unless quoting a UI element.
- Write in active voice. The subject performs the action.
  - Wrong: "The token is stored in the .env file."
  - Right: "Store the token in the .env file."
- Write in present tense throughout. No future tense.
  - Wrong: "The script will return a JSON response."
  - Right: "The script returns a JSON response."

### 4.2 Sentence rules
- Maximum 25 words per sentence. Shorter is better.
- One main idea per sentence. Don't combine two actions or two concepts in one sentence.
- Vary sentence length. Mix short sentences (around 8 words) with longer ones (up to 25 words).
- Use contractions naturally. Write "you'll need to," "it's important," "don't forget." Don't use formal constructions like "do not" and "it is" unless surrounding sentences already use a contraction.
- Avoid "where" to connect clauses. Use "because," "since," or "so" instead.
  - Wrong: "Teams maintain duplicate codebases where maintenance costs double."
  - Right: "Teams maintain duplicate codebases, so maintenance costs double."
- Occasionally start sentences with "And" or "But" when it creates natural flow.
- Avoid nested clauses. When a simpler structure works, use it.
  - Nested (harder to read): "The API, which requires authentication, which you set up in the previous step, returns a JSON response."
  - Simpler: "The API requires authentication. Set it up in the previous step. It returns a JSON response."

### 4.3 If/then construction
Every "if" clause must include "then" in the predicate. No exceptions.
- Wrong: "If you need updates, use Option A."
- Right: "If you need updates, then use Option A."

### 4.4 May and might
- Use "may" for permission: "You may skip this step if you already have a token."
- Use "might" for possibility: "This might cause a build failure."

### 4.5 Em-dashes

Use em-dashes when they improve clarity, emphasis, or flow. Use them for a sharp break in thought, immediate clarification, or a parenthetical remark that would be clunkier with commas or periods. Don't use them automatically or because they appear frequently in AI-generated text.

**When to use an em-dash:**
- You want to add a quick clarification mid-sentence.
- You want a deliberate pause or break in thought.
- You want stronger emphasis than a comma or parentheses provides.

**When to skip the em-dash:**
- A period is cleaner.
- A comma is enough.
- A colon gives a clearer lead-in.
- The sentence reads more naturally without it.

**Examples:**
- Better with em-dash: "The issue is clear—missing permissions caused the failure."
- Better with a period: "The issue is clear. Missing permissions caused the failure."
- Better with a colon: "The issue is clear: missing permissions caused the failure."

All three are correct. Choose the one that reads best in context.

**The rule in plain terms:**
- Use em-dashes only when they improve clarity or emphasis.
- Don't use them automatically or because they are a common AI-writing pattern.
- Prefer periods, commas, or colons when they read more cleanly.
- Choose the punctuation that makes the sentence easiest to scan and understand.

### 4.6 Paragraph rules
- Keep paragraphs to two to three sentences for online documentation. Longer paragraphs create unnecessary cognitive load for readers who are scanning.
- Every heading must have at least one paragraph beneath it. Never stack headings.
- No paragraph should begin with a mechanical transition (see banned transitions list).

### 4.7 Heading rules
- Sentence case for all headings (H1 through H6). No title case.
- Every page has one H1 that states the topic clearly.
- Use H2 and H3 to break content into scannable sections.
- Never use bold text as a heading. Use proper heading markup.
- Never skip heading levels. Start with H2 on pages after H1.
- Naming conventions by content type:
  - How-to guides: bare infinitive ("Connect the device to the network")
  - Tutorials: bare infinitive ("Log your first request")
  - Get started: bare infinitive ("Get started" is the only permitted exception)
  - Concepts: noun phrase ("Alert types," "Architecture overview")
  - Reference: noun phrase ("GitHub Issues API reference")
- Minimise parentheses in headings.
- Every heading must be followed by a description paragraph before any list, table, or code block appears.

### 4.8 Lists and bullets
- Bullet lists for unordered information. Numbered lists for sequences.
- Every list needs at least two items.
- Format four or more related items as a list, not prose.
- Keep list items parallel in structure.
- Periods on full-sentence items. No periods on phrases or fragments.
- Mixed-structure items (definition label plus full sentences): use a period at the end, lowercase after the colon.
- Never use a numbered list for unordered information.

### 4.9 Steps
- Each step is one clear action. Never combine two actions in one step.
- If a step produces a visible result, describe it in the line immediately after the step. System responses are not steps. Don't number them.
  - Step: "Select **Save**."
  - Response (not a step): "The dashboard refreshes and displays your changes."
- Steps belong inside a numbered list under one procedure heading. Don't give each step its own H2 heading.
- Use "Select" for all UI interactions. Never use "click."
- Use the exact UI label when it's clear on its own: "Select **Save**."
- If the UI label would be repetitive or ambiguous in the sentence, add the control type: "button," "menu," "tab," or "link."
  - Avoid: "Select **Select**." — awkward without the control type
  - Better: "Select the **Select** button." or "Select the **Select** option."
- Note: this disambiguation pattern is a local style decision, not a Google style guide requirement. Google's guidance is to prioritize clarity and avoid awkward duplication, which usually means rewriting the sentence to be unambiguous.
- Use "Enter" for form fields. Never use "add" for form fields.

### 4.10 Code rules
- Specify the language after every code fence. Never leave a bare ```.
- Placeholders go in ALL CAPS: `HELICONE_API_KEY=YOUR-API-KEY`
- No $ before commands. The $ suggests a specific shell and confuses Windows users.
  - Wrong: `$ npm install openai`
  - Right: `npm install openai`
- Comment output in code blocks. Use # to mark expected terminal output so developers know it's not a command.
- Inline code font for all technical terms: parameter names, field names, header names, file names, status codes, and any string the developer types or copies.
- Provide explanatory text before every code block. Never drop a code block under a heading with no prose between them.
- Code examples must be complete, tested, and easy to adapt. Never include broken or untested examples.
- Provide multi-language support where your tool supports multiple languages.
- Always show inputs and outputs together so readers know what to expect.

### 4.11 UI text rules
- Bold all UI labels, buttons, field names, and selectable elements. No quotation marks around them.
- Don't overuse bold. Reserve it for UI elements and critical terms only. Bold used for general emphasis loses its meaning and makes pages harder to scan.
- Place colons outside bold formatting, not inside.
- Match UI labels exactly, including capitalisation, as they appear in the live product.
- For error messages: quote the message exactly, then explain what it means and what the developer should do next.

### 4.12 Links and signposting
- Inline linking is the default. Embed links naturally as part of the sentence.
  - Wrong: "For more information, see the [Authentication guide](#)."
  - Right: "Configure your API key using the steps in the [Authentication guide](#)."
- Don't use "click here" or raw URLs as link text.
  - Wrong: "Click [here](#) to read the guide."
  - Right: "Read the [setup guide](#) before continuing."
- Don't use "see X for Y" as a lazy signpost. Use a verb that describes the action: "read," "browse," "open."
- "See" is acceptable only when the reference is the subject of the sentence, when flagging a major topic shift, or when the linked content is a warning or prerequisite.
- Cross-links appear at the point where the developer needs them, not only at the end of the page.

### 4.13 Notes and warnings
- Use a note block for information that prevents a common mistake.
  - Example: "Note: The API key is case-sensitive. Copy it exactly as shown."
- Use a warning block for actions that are irreversible or have significant consequences.
  - Example: "Warning: Deleting a workspace removes all projects and cannot be undone."
- Place notes and warnings immediately after the step or statement they relate to. Don't group them at the top of the page.
- Don't overuse callouts. If every other step has a note, none of them stand out. Use them strategically.

### 4.14 Tables
- Use for parameter lists, option comparisons, and reference data.
- Don't use for layout.
- Keep headers short and descriptive.
- Every table needs a description paragraph above it.

### 4.15 Transitions between sections
- Conceptual content: use a short transition (one to two sentences) before each new heading.
  - Example: "Once you understand how authentication works, you can configure the token scopes your app needs."
- Task-based and reference content: no transitions between sections. Each section opens with a direct statement and stands on its own.
  - Wrong (task-based): "Now that you've installed the package, let's move on to configuration."
  - Right (task-based): "Configure your environment variables before running the app."
- The test: if removing the sentence between two sections leaves both sections fully clear, the sentence doesn't belong.

### 4.16 Abbreviations
- Never use "e.g." Write "for example" in full.
- Never use "i.e." Write "that is" in full.

### 4.17 Numbers and dates
- Spell out numbers one through nine. Use numerals for 10 and above.
- Use ISO 8601 format for timestamps: YYYY-MM-DDTHH:MM:SSZ

### 4.18 Avoid hidden verbs
Convert verb-noun constructions back to plain verbs.
- Wrong: "conduct an analysis of"
- Right: "analyze"
- Wrong: "provide a summary of"
- Right: "summarize"
- Wrong: "make a decision"
- Right: "decide"

Hidden verbs add length without adding meaning. They are almost always passive in effect even when grammatically active.

### 4.19 Italics

Use italics sparingly. Prefer clear wording over typographic stress.

**Permitted uses:**
- **Introducing a term you define in the same sentence.** Italicize the term on that first mention only, then use plain text everywhere afterward.
- **Strong emphasis (rare).** When importance would be lost without it, use italics rather than bold or underline. This should be at most once or twice per page. Often a tighter sentence removes the need entirely.

**Do not** use italics for UI labels (use bold instead), for general emphasis on ordinary words, or to repeat a term after you have already defined it.

**Markdown formatting:** Use underscores for italics (`_like this_`) so they are easy to tell apart from bold (`**like this**`) in source. Use `**` for bold, not `__`.

**Run-in labels:** When a list item starts with a short bold label and a colon, place the colon outside the bold formatting.
- Right: `**Scenario 1**: description`
- Wrong: `**Scenario 1:** description`

### 4.20 Use plural antecedents and pronouns

Use plural antecedents to avoid gendered singular pronouns. Write "developers configure their settings" not "a developer configures his settings."

### 4.21 Document limitations inline

Document known limitations where users will encounter them, not only in a separate troubleshooting section. An omission is better than an error. If you can't verify a claim, don't include it.

- Wrong: burying a limitation in a troubleshooting section the user may never read.
- Right: "This endpoint returns a maximum of 100 results per request. Use the `cursor` parameter to paginate through larger datasets."

Document the limitation at the point where the user will hit it, not somewhere else.

---

## Part 4 summary: The six documentation standards

Every piece of content must meet all six before it's ready to publish.

| Standard | What it means |
|---|---|
| User-focused | Write for what the user wants to do, not what the tool is |
| Trustworthy | Verify every claim against the live product before publishing |
| Easy to understand | Plain language, active voice, short sentences, no jargon |
| Easy to find | Structure around how users think and move through tasks |
| Usable | A user can complete the task unaided, with no guesswork |
| Style compliant | Active voice, second person, present tense, no sentence over 25 words |

---

## Part 5: Banned words and phrases

### Never use these words
Foster, Revolutionize, Landscape, Seamless, Robust, Streamline, Delve, Elevate, Facilitate, Groundbreaking, Comprehensive.

### Never use these phrases
- "Dives deep" / "Deep dive"
- "This is where X comes in"
- "X is not just about; it's about"
- "X isn't just nice to have; it's..."
- "You're not alone"
- "Thrive in a fast-paced environment"
- "The following" as a vague introducer
- "Click here"
- "See X for Y" as a default signpost

### Never use these mechanical transitions
Additionally, Furthermore, Moreover, In conclusion, To summarise, In summary, As mentioned above, As previously stated.

### Use sparingly (maximum two to three times per page)
Ensure, Enhance, Significant(ly), Effective(ly), Essential.

---

## Part 6: Content types and page structures

### The Diataxis framework
Every page has one clear purpose. Never mix content types on the same page.

| Type | Purpose |
|---|---|
| Tutorial | Learning-oriented. The user builds understanding by doing. The writer controls the sequence. |
| How-to guide | Goal-oriented. The user has a specific task. Steps to complete it. Assumes existing knowledge. |
| Reference | Information-oriented. API, CLI, and configuration details. Lookup content. Describes machinery, no instructions. |
| Explanation | Understanding-oriented. Explains how something works and why. No steps. Provides context and background. |
| Get started | Gets the user to a first successful result as fast as possible. |

**Key Diataxis rules from the Divio documentation system:**
- The four types overlap naturally and will be pulled toward each other. Resist this. Keep them separate and distinct.
- Tutorials and how-to guides are both concerned with practical steps. But tutorials are for learning, and how-to guides are for doing.
- Reference must describe, and only describe. Explanation, discussion, or instruction in reference is a distraction.
- Give reference documentation the same structure as the codebase.
- Tutorials must be reliably repeatable. Everything the learner does should accomplish something comprehensible.
- How-to guides can start and end where appropriate. Practical usability is more valuable than completeness.
- Explanation is the most neglected type. It covers background, context, and the why behind decisions.
- A how-to guide assumes the reader already knows the basics. If they don't, send them to the tutorial first.

### Page structure for tutorials
Every tutorial must include, in this order:
1. Introduction: Situation, obstacle, and promise. Apply the Pixar formula.
2. Prerequisites: What the reader needs before starting. Link every tool and resource.
3. Steps: One numbered list under one procedure heading. Not individual H2 headings per step.
4. Expected output: After every step that produces one.
5. Troubleshooting: At least three common errors with cause and fix.
6. Next steps: What the reader can do after completing the tutorial.

### Page structure for how-to guides
Every how-to guide must follow this structure in this order:
1. Introduction: State what the reader will accomplish. Be specific about the outcome.
2. Prerequisites: List what the reader needs before starting.
3. Step-by-step instructions: Numbered list. One action per step. Describe the visible result after steps that produce one.

### Page structure for API reference
Every endpoint must include all seven elements:
1. Description: what the endpoint does and when to use it (one to two sentences)
2. HTTP method
3. URL with path parameters in curly braces
4. Parameters table (name, type, required or optional, description)
5. Example request: working curl command with ALL CAPS placeholders
6. Example response: real data from a verified API run
7. Error codes: status code, cause, and fix

### Introduction: the Pixar formula
Every how-to guide and tutorial introduction follows this three-part structure:
1. **Situation:** Open with the reader's goal or context.
2. **Obstacle:** Name what stops them from achieving it with a single request or action.
3. **Promise:** State exactly what the page will help them accomplish.

Be specific. Name the tool, the API, the repository, or the exact task. Never use vague language like "a large dataset" when you can say "827 open issues from the facebook/react repository."

---

## Part 7: The caveman technique

Use when a sentence is too complex to fix directly.

1. Strip the sentence to its bare meaning. Grammar doesn't matter. Find the meaning.
   - Original: "The interface provides the ability to instruct the operating system to render items between event dispatches."
   - Caveman: "Interface tell operating system. Operating system render item between event."
2. Identify the core idea. Remove abstractions.
3. Rebuild cleanly using plain language, active voice, and second person.
   - Rebuilt: "The interface tells the operating system to render items between events."

The stripped version is never the final output. The rebuilt version is a starting point. Check it against all six documentation standards before publishing.

---

## Part 8: Voice and tone by section

Your voice is constant. Your tone changes based on what the reader is doing and how they feel.

| Section | Reader's state | Tone to use |
|---|---|---|
| Introduction | Curious, open | Warm, direct, confident |
| Prerequisites | Practical, checking | Neutral, factual |
| Steps | Focused, working | Crisp, action-oriented |
| Expected output | Relieved or checking | Reassuring, affirming |
| Troubleshooting | Frustrated, stuck | Calm, specific, helpful |

**Four voice principles (Mailchimp and Microsoft):**
- **Plainspoken:** Write like a knowledgeable colleague, not a salesperson. Not: "Unlock the power of GraphQL." Use: "This guide shows you how to fetch all results from a paginated GraphQL API."
- **Genuine:** Relate to the reader's challenge. Acknowledge what's hard.
- **Clear over clever:** Never sacrifice clarity for a clever phrase.
- **Active voice always:** Makes clear who does what. Eliminates ambiguity.

**Microsoft voice principles:**
- Warm and relaxed: natural, less formal, grounded in real conversations
- Crisp and clear: write for scanning first, reading second
- Ready to help: anticipate real needs and offer the right information at the right time
- Get to the point fast: start with the key takeaway, put the most important thing in the most noticeable spot
- Use sentence case: less formal than title case, reflects modern style

---

## Part 9: Cognitive load principles

**Three types of cognitive load:**
- **Intrinsic load:** the inherent difficulty of the subject. Manage it by breaking content into smaller pieces.
- **Extraneous load:** unnecessary effort caused by poor presentation. Eliminate this as a writer.
- **Germane load:** the mental effort to connect new information to existing knowledge. Support this with good analogies and consistent patterns.

**Ten techniques for reducing cognitive load:**
1. **Chunking:** one idea per sentence, one action per step, lists over dense paragraphs
2. **Visual aids:** diagrams and flowcharts alongside text
3. **Progressive disclosure:** overview first, quick start next, detailed reference last
4. **White space:** short paragraphs, bullet points, generous spacing
5. **Consistent structure:** same format across every section
6. **Leverage prior knowledge:** connect new concepts to things the reader already knows. Example: "The async/await pattern in JavaScript is similar to Python's coroutines."
7. **Clear navigation:** table of contents, search, glossary, descriptive headings
8. **Minimize jargon:** simpler alternatives where they exist
9. **Examples and analogies:** concrete beats abstract every time
10. **Interactive elements:** collapsible sections, interactive code samples, tooltips

---

## Part 10: Developer mindset principles

**What developers actually need:**
- Real-world implementation examples, not just API references
- Migration guides from competing tools
- Performance implications and trade-offs
- Known limitations and workarounds
- Integration patterns with popular tools
- Clear troubleshooting flows
- Docs organized by user intent: "I want to migrate from X," "I need to integrate with Y"

**What great docs do:**
- Maintain a living "gotchas" section built from GitHub issues, Discord questions, and support tickets
- Get users from nothing to something as fast as possible
- Put the most important information first. No long intros.
- Use short paragraphs (three to four lines maximum)
- Show rather than tell: JSON structures over data type summaries, screenshots over UI explanations, diagrams over workflow walkthroughs

**Developers don't read. They scan.** Structure every section to stand on its own. Match the workflow sequence: if a developer needs to install, configure, and then integrate, your docs follow that exact order. Docs that create friction lose developers. Every unclear step, every missing example, and every wall of text is friction.

---

## Part 11: Information architecture principles

### Four key components

- **Organization systems:** group content by user mental model, not company org chart.
- **Labeling systems:** use consistent, specific, predictable labels that users can scan and decide on quickly.
- **Navigation systems:** provide visible pathways such as menus, breadcrumbs, local navigation, and sidebar links.
- **Search systems:** treat search as the fallback; heavy search use often means navigation is not doing enough work.

### IA rules

- Design for a predictable structure; users forgive small imperfections, but they do not forgive surprises in hierarchy.
- Every page is a front door. People arrive from search, Slack, links, or bookmarks, so every page needs clear orientation and obvious next steps.
- Avoid junk-drawer categories like "General," "Resources," or "Other," because they create friction and force users to translate your system.
- When structure matches user mental models, users spend less time decoding the system and more time finishing the task.
- Map the full end-to-end flow of a task before you start writing. Organize content to match that flow. Headings should follow the task sequence, not the product menu structure.
- Add a "Next steps" section to tutorials. Most other pages don't need one. If a platform like Mintlify provides built-in previous and next navigation cards, a separate "Next steps" section adds redundancy on pages where the user's path forward is already clear. Use your judgment: if users arrive at a page through search or a direct link and the page is self-contained, a "Next steps" section adds value. If the navigation already handles forward movement and the context is obvious, leave it out.

**Information fragmentation** is what happens when content is structured around product features rather than user goals. Users have to jump between sections to complete one task. If a user has to visit three pages to finish one task, the content is fragmented. Reorganize around the task.

### Sidebar naming

- Sidebar names are part of the labeling and navigation system, so they should be user-facing, not org-chart-based.
- Use brief, specific labels like "Dashboard," "Projects," "Billing," "Team," and "Settings."
- Avoid vague or internal labels like "General," "Resources," "Miscellaneous," "Admin Stuff," or "Company."
- The label should make sense even when seen out of context, because users often land on a page from search or a shared link.

### Tutorial and guide labels

- Tutorial and guide labels should describe the learning goal, not just the content bucket.
- Use labels that tell users what they will learn or do, such as "Set up billing," "Connect your CRM," or "Start here."
- Use consistent patterns within a doc set so users can scan quickly and understand the difference between task, guide, and reference content.
- Good patterns include "Getting started with X," "How to X," "X setup guide," "X troubleshooting guide," and "X admin guide."

### Naming rule for style

- Use imperative verbs for tasks and step-by-step tutorials.
- Use gerunds or noun phrases for concepts and overviews.
- Keep one grammatical pattern within the same navigation level or documentation set.
- Avoid mixing styles at the same level, because it makes scanning slower and the structure feel inconsistent.

### UI product and tool labels

- For UI products and tools, labels should be clear, concise, and predictable, just like control labels in Microsoft guidance.
- Prefer labels that describe the object or action directly, not clever wording.
- Good examples: "Save," "Filters," "Import data," "API keys," "Integrations," and "Permissions."
- Avoid labels that are generic, witty, or ambiguous, such as "More," "Info," "Click here," or company-specific jargon unless the audience already knows it.
- Don't write labels as questions, and don't add unnecessary punctuation or sentence-like phrasing where a short label will do.

### Example patterns

- Task: "Create an account."
- Task: "Connect Slack."
- Task: "Set up billing."
- Guide: "API key setup guide."
- Guide: "Integration guide."
- Concept: "Creating API keys."
- Concept: "Connecting apps."
- Sidebar: "Projects," "Billing," "Team," "Settings."
- Avoid: "General," "Resources," "Other," "More," "Info."

### One-line rule

Use imperative verbs for tasks, gerunds or nouns for concepts, and short specific nouns for UI labels and sidebar navigation.

---

## Part 12: Journey mapping

**Five components of a user journey map:**
1. **Actor:** the persona or user who experiences the journey. One point of view per map. Actions in the map must be rooted in data.
2. **Scenario and expectations:** the situation the map addresses, tied to the actor's goal. Journey maps work best for scenarios that involve a sequence of events, describe a process, or involve multiple channels.
3. **Journey phases:** high-level stages that organize everything else. Examples: discover, try, buy, use, seek support.
4. **Actions, mindsets, and emotions:** what users do, think, and feel at each stage. Emotions are plotted as a single line showing ups and downs across phases.
5. **Opportunities:** insights that answer what needs to be done, who owns the change, where the biggest opportunities are, and how to measure improvements.

**Standard journey map format:**
- Top: specific user, specific scenario, corresponding expectations or goals
- Middle: high-level phases with user actions, thoughts, and emotions
- Bottom: takeaways including opportunities, insights, and internal ownership

---

## Part 13: SME collaboration principles

**Eight principles for working with SMEs:**
1. Leave your ego at the door. You represent the reader, not yourself.
2. Don't embrace the jargon. Understand it, then decide if it helps the reader. If customers use the term comfortably, keep it. If they don't, cut it.
3. Don't waste the SME's time. Prepare questions, think through user problems, check existing resources first.
4. Respect the SME's workload. If they're too busy, explain your deadline calmly.
5. Arrive calm and on time.
6. Admit when you don't understand. A few minutes of awkwardness is better than incorrect documentation.
7. Never lose your temper.
8. Be judged on your output. When your documentation helps customers, people will respect what you do.

**Source credibility by role:**
- Pre-sales and marketing: customer stories and pain points
- Product management: strategy and positioning
- Support teams: what breaks and what confuses customers
- Developers: how the product actually works

Combine all four. A developer tells you what the system does. A support agent tells you what confuses users. A pre-sales person tells you what customers care about.

**Interview technique:**
- Prepare 20 questions. Expect to use five to ten.
- Open with: "What do you want people to know about this?" and let them talk.
- Record everything. Take notes alongside any recording.
- Clarify goals before you start writing.
- Never ask the same question twice.

---

## Part 14: Docs-as-code principles

Documentation lives in the same repository as code, uses the same version control, and follows the same review process.

**Core practices:**
- Write documentation in Markdown or MDX in an IDE
- Store documentation in a Git repository alongside the code it describes
- Use pull requests to review and approve documentation changes
- Run automated checks on documentation (broken links, formatting errors, style violations)
- Publish documentation automatically when changes are merged

**Typical workflow:**
1. Developer writes a first draft in Markdown inside the code repository
2. Technical writer picks up the draft, verifies it against the product, and completes it
3. Pull request goes through peer review
4. Automated checks run (Vale linting, link validation, style enforcement)
5. Once approved, documentation publishes automatically

---

## Part 15: REST API concepts

**What REST is:**
REST (Representational State Transfer) is an architectural style for APIs. It uses standard HTTP methods and human-readable URLs, making it easy for developers to learn and use. REST is not a protocol. It's a set of architectural constraints.

**Five HTTP methods:**
- `GET`: retrieves resources. Safe and idempotent. Never use GET for operations that modify data.
- `POST`: creates new resources or triggers actions that change server state. Returns 201 Created.
- `PUT`: updates existing data entirely. Replaces the full resource.
- `PATCH`: updates specific properties on a resource without overwriting others. More flexible than PUT.
- `DELETE`: removes data from a database.

**HTTP methods map to CRUD operations:** Create (POST), Read (GET), Update (PUT/PATCH), Delete (DELETE).

**Key REST concepts:**
- **Resource:** the fundamental concept in REST. An object with a type, associated data, and relationships to other resources.
- **Endpoint:** the URL that identifies a specific resource. Use nouns only. HTTP methods handle the verbs.
- **Parameters:** path parameters (in the URL), query parameters (filter/sort), header parameters (authentication, metadata).
- **Authentication:** verifies identity. Common methods: API keys, OAuth 2.0, Bearer tokens.
- **Status codes:** 200 OK, 201 Created, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.

**URL naming rules:**
- Use nouns, not verbs in URLs. The HTTP method is the verb.
  - Wrong: `GET /getUsers`
  - Right: `GET /users`
- Nested resources follow parent path: `GET /articles/:id/comments`
- Consistent naming throughout. If you use snake_case in one endpoint, use it everywhere.

---

## Part 16: API documentation best practices

**What every API reference must include:**
- Overview: what the API does and who it's for in two to three sentences
- Getting started: help users make their first successful request as fast as possible
- Authentication: exactly how to authenticate, with a working example
- Endpoints: every endpoint documented with all seven required elements (see Part 6)
- Code examples: in multiple languages where possible, copy-paste ready, and tested
- Error codes: exhaustive list with HTTP status, unique error code, human-readable message, and resolution guide
- Changelog/release notes: what changed, when, and what it affects

**Principles from Stripe, Twilio, and Microsoft:**
- Treat documentation as a product. It goes through the same review process as code.
- Consistency in organization, terminology, and example formats from endpoint to endpoint
- Provide a living "gotchas" section built from support tickets and GitHub issues
- Include interactive elements where possible so developers can test without leaving the docs
- Never publish API docs without verifying every example against the live API

**Organizing API docs:**
- Know your audience: decision-makers need high-level overviews, developers need technical depth
- Provide quick starts for developers who want to get running immediately
- Structure navigation around user intent: "I want to authenticate," "I want to paginate," not around internal system structure

**Code examples (from Stripe's approach, via Larry Ullman at Write the Docs 2018):**
- Treat your code like your writing. Apply a style guide to code, including naming conventions, indentation rules, and placement of parentheses.
- Every example must be complete, copy-pasteable, and verified to run.
- Where possible, generate code examples programmatically to avoid inconsistency across languages.
- Always show both the request and the expected response together.
- Test examples in CI/CD so they never go stale.

---

## Part 17: Troubleshooting documentation best practices

**Structure troubleshooting guides around symptoms, not causes:**
- Organize by what the user sees, not by internal system categories
- Use exact error messages as headings so they are searchable
- Each entry must have: the error, the cause, and the fix. Not general advice.

**How to find what to document:**
- Analyze error logs and system data to find what problems occur most
- Review support tickets regularly to identify the most common questions
- Gather feedback from users through comments and surveys
- When something confuses you during testing, that's a documentation opportunity

**Writing troubleshooting entries:**
- Quote exact error messages
- Explain the root cause clearly, not just the symptom
- Give step-by-step resolution instructions, not just a one-liner fix
- Add a "Still stuck?" escalation path at the end of complex guides
- Include edge cases and situations where the feature might not behave as expected

**Error message standards (from Microsoft):**
- Error messages must be meaningful and clear
- Include what went wrong, why it went wrong, and what to do next
- Use contractions and plain language in error messages. "I couldn't print your document. Check your printer or connection." not "Printing failed."
- Never include developer error codes like "WDGeneralNetworkError Error 500" in user-facing messages. Hide them under a details section.
- Avoid long how-to guidance in errors. That content lives in the documentation.

---

## Part 18: Versioning and redirects

**Core versioning principles (from Read the Docs):**
- Publish a separate `latest` version pointing to the most up-to-date development code
- Publish a separate `stable` version pointing to the most recent release tag
- Never make a development branch your default version. Users will read unreleased instructions.
- Keep development versions hidden so they don't appear in search results
- Use semantic versioning for tags: 1.4.2, not descriptive names

**Versioning strategy:**
- Maintain separate Git branches for each release version
- When ready to release, create a new branch from main named after the version (for example, v4.0)
- Apply hotfixes to the release branch, not just to main
- Use Git tags when branching isn't needed for lighter projects

**Redirects when moving pages:**
- Every page that moves needs a redirect. People link to your documentation from emails, issues, and articles you don't control.
- The simple approach: redirect all old URLs to the latest version. Faster to implement but can confuse users who searched for a specific topic.
- The user-friendly approach: map each deprecated page to the corresponding new page. More work but preserves context.
- Use the `/page/` URL prefix for links that should always point to the default version regardless of which version is active

**Best practices for incoming links:**
- Use page redirects when linking to the default version of the default language
- If you move a page that has incoming references, create a custom redirect rule
- Use minimal filenames that don't require renaming often. Renaming an article's title is fine. Renaming the URL is disruptive.
- Establish what `latest` and `stable` mean at the beginning of a project. Changing their meaning later breaks incoming links.

---

## Part 19: Vale linter

Vale is a prose linter for documentation. It checks content against style guide rules automatically.

**What Vale does:**
- Enforces style guide rules (passive voice, banned words, heading case, jargon)
- Operates at syntactic and contextual level
- Can limit rules to certain sections (for example, only headings)
- Ignores block and inline code by default
- Supports Google, Microsoft, and custom style rules

**Core configuration (`.vale.ini`):**
```ini
StylesPath = styles
MinAlertLevel = warning

[*.md]
BasedOnStyles = Google
```

**Run Vale locally:**
```bash
brew install vale        # macOS
vale sync                # sync style packages
vale docs/               # lint docs folder
```

**Three alert levels:**
- **Error:** branding guidelines, anything that causes incorrect rendering. Must fix before merging.
- **Warning:** general style guide rules and best practices.
- **Suggestion:** style preferences that may require refactoring.

**GitHub Actions integration:**
```yaml
name: Lint docs with Vale
on:
  pull_request:
    branches:
      - main
jobs:
  vale:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: errata-ai/vale-action@reviewdog
        with:
          files: docs/
          vale_flags: "--config=.vale.ini"
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**Custom rules:** Vale allows custom YAML rule files. Use them to enforce product-specific terminology, banned phrases, and naming conventions beyond what the Google or Microsoft styles provide.

---

### cSpell for spelling

Vale does not check spelling. cSpell is a code-aware spell checker that understands technical terms, ignores code blocks, and runs in CI on every pull request.

**GitHub Actions integration:**

```yaml
name: Spell check

on:
  pull_request:
    branches:
      - main

jobs:
  spellcheck:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: streetsidesoftware/cspell-action@v6
        with:
          files: "docs/**/*.md"
```

Add a `cspell.json` file to your repo to whitelist product names, technical terms, and abbreviations that cSpell would otherwise flag incorrectly.

**Full quality workflow: Vale + cSpell + LanguageTool**

Run all three together in GitHub Actions for complete coverage:
- **Vale:** style compliance (passive voice, banned words, sentence length, heading case)
- **cSpell:** spelling and technical term accuracy
- **LanguageTool:** grammar errors Vale and cSpell don't catch

For local work without CI, install the cSpell extension for VS Code and run Vale from the terminal before submitting.

---

## Part 20: Mintlify platform rules

**docs.json configuration:**
- All navigation is defined in `docs.json` (replaced `mint.json` in February 2025)
- Navigation uses tabs-based structure
- Page paths reference files without the `.mdx` extension
- Always use `.mdx` for pages. Plain `.md` won't render components.

**Navigation structure:**
```json
{
  "$schema": "https://mintlify.com/docs.json",
  "navigation": {
    "tabs": [
      {
        "tab": "Documentation",
        "groups": [
          { "group": "Getting Started", "pages": ["docs/intro"] }
        ]
      }
    ]
  }
}
```

**Component usage rules:**
- **Steps:** all procedural content
- **Tabs:** content that varies by language, platform, or environment
- **AccordionGroup:** supplementary detail that would clutter the main flow
- **Cards and CardGroup:** navigation entry points on landing pages
- **Code blocks:** with syntax highlighting and language tabs
- **Info, Warning, Tip callouts:** important context that needs to stand out

**The rule for components:** use them where content genuinely calls for it. If a plain paragraph does the job, use a plain paragraph.

**Migration checklist:**
- Export to Markdown for the simplest migration from other platforms
- Update navigation in docs.json when you add or move files
- Navigation must match actual file structure exactly
- Reference OpenAPI file correctly or API sections won't generate
- Check that `llms.txt` is being generated properly for AI discoverability
- Avoid overusing Tabs and Accordions — too many can overwhelm users

---

## Part 21: Docusaurus quickstart

Docusaurus is a static-site generator built by Meta. It builds a single-page application using React, optimized for documentation sites.

**When to use Docusaurus:**
- You need versioning support
- Your team writes in Markdown and knows React
- You're deploying to GitHub Pages or Vercel
- You want built-in search and localization

**Setup:**
```bash
npx create-docusaurus@latest my-docs classic
cd my-docs
npm run start
```

Site runs at `http://localhost:3000`.

**Key files:**
- `docusaurus.config.js` — site configuration, navbar, footer, theme
- `sidebars.js` — sidebar navigation structure
- `docs/` — Markdown documentation files
- `static/` — static assets (images, fonts)

**Docs-only mode (no blog):**
```javascript
presets: [['classic', {
  docs: { routeBasePath: '/' },
  blog: false,
}]]
```

**Deploy to GitHub Pages:**
```bash
npm run build
```
Then connect to GitHub Pages via a GitHub Actions workflow.

**Docusaurus vs alternatives:**
- Docusaurus: best for documentation-focused sites with versioning and React
- MkDocs: good Python-based option for single-page apps
- Mintlify: best for developer-facing API docs with AI search out of the box
- GitBook: collaborative editing but less suitable for open-source projects
- Jekyll: mature and simple but less feature-rich than Docusaurus

---

## Part 22: Microsoft style guide key principles

The Microsoft Writing Style Guide sets the standard for technical documentation writing.

**Top 10 principles:**
1. Write like you speak: natural, conversational, and friendly
2. Get to the point fast: start with the key takeaway
3. Be concise: fewer words are better
4. No jargon: friendly, conversational, and helpful
5. Use contractions: "it's," "you're," "don't"
6. Lead with what's important: put keywords up front
7. No fluff: remove excess words and get to the point
8. Use sentence case: not title case for headings
9. Use active voice and indicative mood most of the time
10. Use imperative mood in procedures

**Writing tips from Microsoft:**
- Use simple sentence structure: subject + verb + object
- Use one word for a concept and use it consistently. Don't use synonyms to refer to the same concept.
- Avoid idioms, colloquial expressions, and culture-specific references
- Avoid modifier stacks (long chains of modifying words)
- Keep adjectives and adverbs close to the words they modify
- Avoid linking more than three phrases by coordinate conjunctions
- Add a determiner (a, an, the, this) before nouns to avoid ambiguity
- Don't break up steps with commentary or asides

---

## Part 23: Storytelling principles in documentation

**The Pixar framework applied to documentation:**
- **Share a unique perspective:** talk to pre-sales, marketing, and product teams who know customer stories. Use those stories as your foundation.
- **Ask "what if" questions:** "What if you could track every investment against your company strategy in real time?" These questions become your scenario and tell users why the product exists.
- **Identify the obstacles:** name the specific barrier the product removes. When you show how the product removes a specific barrier, adoption increases because users recognize themselves in the problem.

**Modular content (the Lego principle):**
- Create self-contained content nuggets that can appear in documentation, tutorials, tooltips, support articles, and education courses.
- Write it once, use it everywhere.
- Before writing, ask: where else could this information appear? What is the smallest useful unit of this content?

**Storytelling structure for introductions:**
1. Start where the user is. Meet your reader at their current level of understanding.
2. Break the problem into logical sections that build on each other.
3. Eliminate everything that doesn't help the reader solve their problem.

**User-story driven documentation:**
Every page answers one user story: "As a developer, I want to fetch all records from a paginated API so that I can process them without missing any data." The title serves it. The introduction sets it up. Every step moves toward completing it.

---

## Part 24: SME technical review standards

From Google's internal practices, technical reviews are the most important step in documentation production.

**Rules for technical reviews:**
- Engineers who know the product must do the reviews. Not project managers, not product owners.
- Be specific about what's wrong and explain why
- Meet the deadline. Late reviews cascade and delay everything.
- Treat technical reviews exactly like a code review

**What to avoid in the review process:**
- Don't change deadlines without telling the writer immediately
- Don't delay technical reviews
- Don't disregard the writer's advice on structure and clarity
- Don't share documents that aren't relevant to the project
- Assign a doc caretaker before the writer leaves. Someone on the team must own keeping the docs updated after launch.

---

## Part 25: The editing checklist

Run every page through this before submitting.

**Before you start**
- Review the relevant style guide before you begin writing or editing.
- When editing your own work, put it aside for a while before reviewing. Overnight is ideal. Read it aloud. The ear catches what the eye misses.
- Run spelling and grammar checks before submitting. Vale handles style compliance. cSpell handles spelling and catches technical term errors. Use both. For grammar, run the content through LanguageTool or Grammarly as a final pass. If you're working in a docs-as-code workflow, run all three via GitHub Actions on every pull request. If you're working locally in a CMS or editor, install the cSpell extension for VS Code and run Vale from the terminal.
- Test all links. Broken links undermine trust immediately.

**User-focused**
- Every heading uses a bare infinitive or noun phrase and describes a user task or outcome
- Every section intro tells the user what they'll accomplish
- No heading names a feature, panel, or tool without connecting it to a user goal
- Content is structured around the user's task flow, not the product menu

**Trustworthy**
- Every step has been performed in the live product before publishing
- Every claim is verified against the live product or a confirmed source
- All product names are spelled exactly as specified
- All UI labels, buttons, and error messages match the live product exactly
- All code samples run successfully in the documented environment
- Expected output matches what the reader will actually see

**Easy to understand**
- Every sentence is plain, active, and direct
- No sentence exceeds 25 words
- No passive voice anywhere on the page
- No jargon or unnecessarily complex vocabulary
- Sentence length varies naturally
- No banned words or phrases
- Sparingly-used words appear a maximum of two to three times per page
- No mechanical transitions
- "Where" is not used to connect clauses
- No extra empty lines between paragraphs or sections where they don't belong

**Easy to find**
- Each section stands on its own
- Headings follow the task sequence, not the product menu structure
- Cross-links appear at the point where the user needs them
- Inline linking is the default
- All link text is descriptive. No "click here" or raw URLs
- Transitions appear only in conceptual content
- Any reference list or further reading section at the end of a page has an introductory sentence. Don't drop a bare list of links with no context.

**Usability**
- Each numbered step contains one clear action
- System responses are not steps. Describe the result in the line after the step, not as a numbered item.
- Every step that produces a visible result describes that result immediately
- Every option is explained: what it means and when to use it
- Notes and warnings appear immediately after the step they relate to
- Every list has at least two items
- Any list of more than three items is formatted as a list, not prose
- Numbered lists are used only for sequences
- Placeholders are in ALL CAPS
- No $ before commands
- Language is specified after every code fence
- Output is commented out in code blocks
- Explanatory text appears before every code block

**Style compliance**
- Active voice throughout. No passive constructions.
- Second person throughout. "We" and "let's" don't appear.
- Present tense throughout. No future tense.
- All headings are sentence case.
- Every heading has at least one paragraph beneath it. No stacked headings.
- Bold is used only for UI elements and critical terms. It isn't used for general emphasis.
- UI elements are bold without quotation marks.
- Colons appear outside bold formatting.
- "Select" is used for all UI interactions. "Click" doesn't appear.
- "Enter" is used for form fields. "Add" is not used for form fields.
- "May" is used for permission. "Might" is used for possibility.
- Every "if" clause includes "then" in the predicate.
- Em-dashes are used only where they improve clarity or emphasis. They are not used automatically or as a default punctuation choice. Where a period, comma, or colon reads more cleanly, that punctuation is used instead.
- Contractions are used naturally.
- All list items are parallel in structure and punctuation.
- "E.g." and "i.e." don't appear.
- No banned words, phrases, or mechanical transitions.
- "The following" is not used as a vague introducer.

**File and folder structure**
- Keep one image folder in the root directory of the documentation project. This makes images easier to reuse across pages.
- The folder structure should mirror the organization of the documentation. Tab folder > Section folder > Subsection if needed. Don't let folder depth exceed three levels.

---

## Part 26: Font and formatting (Google Docs)

- Font: Avenir
- Heading size: 13
- Normal text size: 11

---

## Part 27: The RAG architecture goal

After the programme, build a RAG with all data from these resources. The AI model will have a specific voice for any project you want to work on, and there will be consistency in docs and an industry standard approach in creating documentation.

**Structure:**
1. System prompt: style rules from this document
2. RAG layer: all programme resources as reference material
3. Post-generation linting: Vale pass with Google and custom rules

If anything isn't covered in the RAG, check the Google Developer Documentation Style Guide as the fallback.

---

## Part 28: API documentation — workshop principles (Tom Johnson, Write the Docs)

**What an API is:**
APIs are requests and responses. That is the core. A system on the left, a system on the right, and the API is the interface that connects them. It lets computers talk to each other without a human manually firing off calls.

**REST APIs specifically:**
REST APIs use HTTP as the transport protocol, making them language-agnostic. A JavaScript app, a Python app, and a Ruby app can all call the same REST API. This is why REST has become dominant. A language-tied API limits your audience and makes every update require multiple SDK releases across several languages.

**The five sections every API reference endpoint must include:**
1. Description of the resource
2. Endpoint URL and HTTP method
3. Parameters (header parameters, path parameters, query string parameters, request body parameters)
4. Example request (usually curl, copy-pasteable and working)
5. Sample response (correlated with the sample request, plus a schema listing all possible fields with data types)

Good API docs define every field in the response. Bad API docs assume the user already knows what the fields mean.

**The "try it out" feature:**
Interactive API explorers that let users execute requests directly inside the docs are the defining characteristic of great API documentation. Developers learn by doing. When they can push a button and see a real response, adoption increases. Platforms like Stoplight, ReadMe, and Swagger UI generate this interactivity from an OpenAPI specification file.

**The OpenAPI Specification (OAS):**
The OAS is the structured format that powers most modern API documentation tools. When you describe your API in this format, tools can render it into interactive documentation, generate code snippets in multiple languages, and validate requests. Swagger is tooling built on top of OAS, not the specification itself.

**Conceptual topics in API docs:**
Every API documentation set needs both reference content and conceptual content. Reference covers the endpoints. Conceptual covers:
- Getting started: zero to first working request, as fast as possible
- Authentication: how to get a key, where to put it, what it costs
- Status and error codes: every possible code with cause and resolution
- Rate limits: how many requests per period, what happens when exceeded
- Tutorials: end-to-end walkthroughs using the endpoints together
- SDKs: language-specific implementations for teams working in a specific stack

**The hello world principle:**
The shorter the time from "I found these docs" to "I have something working," the higher the adoption rate. A getting started guide that says "get up and running in five minutes" is more compelling than one that says "comprehensive overview." Get users to a first successful result immediately, then let them explore deeper.

**API docs and selling the product:**
For developer-facing APIs, the documentation is often the product's user interface. Users learn about the product through the docs. They can't download a trial and click around. This means API docs must be attractive, well-structured, and compelling. Poor docs directly reduce adoption, even for a technically excellent API.

**Postman and curl:**
These are the standard tools for testing API requests before documenting them. Postman provides a GUI for making requests, viewing responses, and generating code snippets. curl is the command-line equivalent and is the standard format for showing request examples in documentation. Test every request in Postman or curl before including it in the docs.

---

## Part 29: GitHub Actions for documentation

GitHub Actions is a platform to automate developer workflows. CI/CD pipelines are one use case. For documentation teams, the most valuable use is automating quality checks on every pull request.

**Core concepts:**
- **Event:** something that happens in your repository. Push, pull request, issue creation, contributor joining.
- **Action:** a small automated task triggered by an event. Labeling an issue, running a linter, building a site.
- **Workflow:** a combination of actions that execute together in response to an event.
- **Job:** a group of steps that run in sequence on a single server.
- **Runner:** the server that executes the workflow. GitHub provides Ubuntu, Windows, and macOS runners.

**Workflow file structure:**
All workflow files live in `.github/workflows/` and use YAML format.

```yaml
name: Docs quality check

on:
  pull_request:
    branches:
      - main

jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: errata-ai/vale-action@reviewdog
        with:
          files: docs/
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**Key syntax elements:**
- `on:` defines the events that trigger the workflow
- `jobs:` groups the steps for each automated task
- `uses:` references a pre-built action from the GitHub Actions marketplace
- `run:` executes a shell command directly
- `needs:` makes one job wait for another to complete before starting
- `${{ secrets.SECRET_NAME }}` references a secret stored in repository settings

**Pre-built actions:**
The GitHub Actions marketplace contains actions for common tasks: `actions/checkout` checks out your code, `actions/setup-node` installs Node.js, `errata-ai/vale-action` runs Vale. Use pre-built actions instead of writing shell commands when they exist.

**Documentation-specific use cases:**
- Run Vale linting on every pull request to catch style violations before merge
- Build and deploy a Docusaurus or Mintlify site on every push to main
- Check for broken links on every pull request
- Run accessibility checks on every docs change

**Secrets management:**
Never put credentials in your workflow file. Store them in **Settings > Secrets and variables > Actions** and reference them as `${{ secrets.SECRET_NAME }}`. Secrets are not available to pull requests from forks by default.

---

## Part 30: The seven action model for documentation (Beyond Content Types)

Content type frameworks like Diataxis describe what to write. The seven action model describes what users need to accomplish. These are complementary. Use the action model to decide what to build, then use Diataxis to decide how to write it.

**The core principle:**
Treat documentation as a product. Design for user actions, not content types. Ask not "what content type is this?" but "what does the user need to do here?"

**The seven actions:**

**1. Appraise** (evaluate, assess)
Users who want to know whether the product is right for them before committing. Frequently neglected because it sits between marketing and documentation. But documentation is trusted in a way marketing isn't. Users come to docs to get honest answers. Pages that satisfy this need include: product overview, service description, capability comparison.

**2. Understand** (comprehend, learn)
Users who need to grasp the abstractions and concepts behind the product before they can use it effectively. Kubernetes needs a control plane explainer before a deployment tutorial makes sense. React needs a component model explainer before a how-to guide makes sense. Pages that satisfy this need include: conceptual overview, glossary, architecture diagram.

**3. Explore** (discover, browse, try)
Users who have signed up and are navigating the product for the first time. Documentation can support this through interactive elements, quick starts, and sandboxes that let users try things without commitment. The Go language tour is a strong example: code on the right, instructions on the left, editable and runnable.

**4. Practice** (exercise, operate, learn by doing)
Users who are learning to operate most of the product's features. This maps to tutorials and how-to guides. The more thoroughly a user practices, the more likely they become a product advocate.

**5. Remember** (recall, retrieve, reference)
Users who already know how to do something but need to look up a specific detail. This maps to reference documentation. The evergreen value of documentation lives here. Docker's Dockerfile reference and GitHub's syntax reference are strong examples: everything on one page, searchable, scannable.

**6. Develop** (extend, build, integrate)
Users who are building on top of the product. API documentation, SDK documentation, and extension guides satisfy this need. This turns users into co-creators and is the foundation of an ecosystem.

**7. Troubleshoot** (solve, diagnose, stabilize)
Users who have a problem and need to fix it. The most neglected action in traditional content type frameworks. The most effective troubleshooting documentation does not just list fixes. It teaches users how to think about diagnosing problems with the product.

**The doc sandwich:**
Frameworks and content types are the bread. They hold things together. User needs are the filling. Business goals (OKRs, conversion targets) are the sauce. You need all three. Frameworks are not enough on their own.

**Mapping actions to metrics:**
- Appraise: measure by conversion rate from documentation
- Understand: measure by learning path completion
- Explore: measure by user engagement and signups for new features
- Practice: measure by feature adoption rates
- Remember: measure by return visits and time on reference pages
- Develop: measure by number of integrations created
- Troubleshoot: measure by decrease in time to resolution and support tickets

---

## Part 31: Taxonomies for documentation findability (Hedden)

A taxonomy is a controlled vocabulary used to tag content so users can find it by browsing or searching on the taxonomy terms.

**Why taxonomies matter for documentation:**
Technical documentation has moved from print to online. Print documentation used a table of contents and a back-of-book index. Neither works well online. Alphabetical indexes require users to already know the term they're looking for. Taxonomies solve this.

**Taxonomy advantages over indexes:**
- Hierarchical trees allow users to drill down from broad to specific without knowing the exact term
- Faceted search lets users filter by multiple dimensions simultaneously
- Tagging is simpler than indexing because the terms and cross-references are pre-established
- The same taxonomy can apply across the entire enterprise, not just documentation

**Facets for technical documentation:**
These are the dimensions by which users filter content.
- User audience (beginner, advanced, administrator, developer)
- Content type (tutorial, how-to, reference, concept)
- Product or module
- Feature or function
- Topic

**Diverse documentation users:**
The same documentation often serves multiple audiences: customers, prospective customers, support agents, consultants, product managers, engineers. A well-designed taxonomy adapts to different user groups through different interfaces. Advanced search can expose more metadata. A simplified view can show only the facets most relevant to a specific audience.

**Tagging in docs-as-code workflows:**
In component content management systems (CCMSs), content is already managed at the component level. This makes tagging straightforward. Writers, editors, and content managers can tag components themselves without specialized indexing training. Tagging can also be automated using AI classification tools.

---

## Resource coverage log

### Reviewed and incorporated (43 resources)
1. How to work with Technical Writers (YouTube) ✅
2. What developers actually want from documentation (Reddit) ✅
3. What nobody tells developers about documentation (PostHog) ✅
4. Cognitive load theory in technical writing ✅
5. Awesome Workflow Automation (GitHub) ✅
6. User Journey Mapping 101 (Nielsen Norman Group) ✅
7. Task-based writing (Write the Docs Newsletter) ✅
8. What is information architecture? (Technical Writer HQ) ✅
9. How to interview SMEs (Craig Wright) ✅
10. Interviewing Subject Matter Experts (YouTube) ✅
11. Is Tech Writer a Tester? (Write the Docs talk) ✅
12. What is docs as code? (GitBook) ✅
13. The complete Mintlify documentation migration guide ✅
14. Versioning Documentation (Read the Docs) ✅
15. Conducting a tech documentation audit: first 30 days onsite ✅
16. Google Style Guide ✅
17. Microsoft Manual of Style ✅
18. Plain Language Principles (PlainLanguage.gov) ✅
19. Storytelling for Technical Products: Lego and Pixar ✅
20. How Storytelling Simplifies Complex Content ✅
21. Voice and Tone in Docs (Mailchimp) ✅
22. GitHub voice and tone ✅
23. Divio documentation system ✅
24. Vale documentation linter ✅
25. Mintlify Quickstart ✅
26. From code to clarity (Day 1 video) ✅
27. What is REST? ✅
28. API documentation best practices ✅
29. Postman API testing ✅
30. What makes good API documentation? ✅
31. Making Your Code Examples Shine (Larry Ullman, Write the Docs 2018) ✅
32. Developer Troubleshooting Docs: Best Practices (daily.dev) ✅
33. Docusaurus Tutorial ✅
34. Active voice principles ✅
35. Scenario-based documentation (principles incorporated from related resources) ✅
36. User-Story Driven Docs (principles incorporated from related resources) ✅
37. Technical Writing Guide 2025 — Adoc Studio (principles incorporated) ✅
38. Understanding APIs (MDN) — core concepts incorporated in REST section ✅
39. Style Guides — Write the Docs (principles incorporated) ✅
40. API workshop recordings — Tom Johnson, Write the Docs (transcript provided) ✅
41. GitHub Actions for Docs — YouTube tutorial (transcript provided) ✅
42. Beyond Content Types: A Human-first Model for Technical Documentation (transcript provided) ✅
43. Taxonomies for Technical Documentation — Hedden Information (article provided) ✅

### Intentionally excluded (1 resource)
44. VSCode Guide for Beginners — excluded at writer's direction. Not relevant for senior-level work.

### Not incorporated (1 resource — paywalled)
45. Information Architecture 101 — Interaction Design Foundation (paywalled). Core IA principles are covered in Parts 11 and 30.