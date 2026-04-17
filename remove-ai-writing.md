Scan the specified file (or the file the user is currently working on) for AI writing tells. Present findings as a numbered list, grouped by category. Do NOT fix anything until the user confirms which items to address.

## What to scan for

### Vocabulary (overused AI words)
Flag any of these when used in ways that feel generic or filler:
- additionally (especially starting a sentence), align with, boasts (meaning "has"), bolstered, crucial, comprehensive, cutting-edge, delve, emphasizing, enduring, enhance, encompassing, features (meaning "has"), foster/fostering, garner, groundbreaking, highlight (as verb), innovative, interplay, intricate/intricacies, key (as adjective), landscape (abstract noun), maintains (meaning "has"), meticulous/meticulously, nuanced, offers (meaning "has"/"gives"), pivotal, profound, renowned, robust, seamless/seamlessly, showcase/showcasing, tapestry (abstract noun), testament, transformative, underscore (as verb), valuable, vibrant, vital

Note: AI vocabulary shifts over time. "Delve" was peak 2023–2024; "enhance," "highlighting," and "showcasing" became more dominant mid-2025 onward. Use judgment — flag words that feel like filler in context, not words used precisely.

### Patterns
- **Significance puffery**: "stands/serves as", "is a testament to", "a vital/significant/crucial/pivotal role", "underscores its importance", "reflects broader", "setting the stage for", "marking/shaping the", "evolving landscape", "indelible mark", "deeply rooted"
- **Superficial -ing analysis**: sentences ending with dangling present participles that add vague commentary ("highlighting its importance", "ensuring quality", "reflecting the broader trend", "contributing to the field", "fostering innovation")
- **Negative parallelisms**: "not just X, but also Y", "not only... but...", "it's not... it's..."
- **Rule of three**: formulaic three-item lists where two would do ("innovation, collaboration, and excellence")
- **Copula avoidance**: "serves as" instead of "is", "boasts" instead of "has", "represents" instead of "is", "stands as" instead of "is", "features" instead of "has", "maintains" instead of "has", "offers" instead of "gives"
- **Em dash overuse**: excessive use of em dashes where commas, parentheses, or periods would be more natural
- **Elegant variation**: avoiding repeating a word by cycling through fancy synonyms unnecessarily
- **Promotional tone**: "nestled in", "in the heart of", "diverse array", "rich heritage", "natural beauty", "commitment to"
- **Vague attribution**: "experts argue", "observers note", "industry reports suggest", "observers cite"
- **Despite-challenges formula**: "Despite [positive thing], [subject] faces challenges..." followed by optimistic resolution
- **Didactic disclaimers**: "it's important to note", "worth noting", "it's crucial to remember"
- **Formulaic headings**: "Challenges and Future Prospects", "Legacy and Impact", "Significance and Influence"

### Formatting tells
- **Curly quotes/apostrophes** in contexts that expect straight quotes
- **Markdown syntax leaking** into non-markdown contexts (stray `**bold**` or `[links](url)` in plain text)
- **Excessive boldface** used for emphasis where none is needed
- **Inline-header vertical lists** (bolded word followed by colon on every list item when a simple list would do)

## Output format

Present findings as:

```
## AI Writing Tells Found

### Vocabulary
1. Line X: "delve" — consider a simpler alternative
2. Line X: "fostering" — filler verb

### Patterns
3. Line X: Negative parallelism — "not just X, but Y"
4. Line X: Significance puffery — "serves as a testament"

### Formatting
5. Line X: Curly quotes in a code context

### Summary
X items found across Y categories.

### Human Writing Score: X/10
```

**Scoring guide:**
- **10**: Reads like a specific human wrote it. Has a voice.
- **9**: Clean. No tells. Could be human or AI but nothing flags.
- **8**: One or two minor patterns but nothing a reader would notice.
- **7**: Competent but generic. A few tells that a trained eye would catch.
- **6**: Obviously polished by AI. Multiple vocabulary/pattern flags.
- **5 or below**: Reads like a chatbot wrote it.

Then ask: "Which items should I fix? (all / specific numbers / none)"

## When fixing
- Replace flagged words with simpler, more direct alternatives
- Cut superficial -ing phrases entirely rather than rewriting them
- Flatten negative parallelisms into direct statements
- Break rule-of-three lists if the third item adds nothing
- Replace "serves as" / "stands as" with "is" where appropriate
- Only change what was approved — do not refactor surrounding text

## After fixing
Re-scan the text and score it again. Present the updated findings and score. If the score is below 8, ask "Another round? (yes / no)" — do not auto-fix without confirmation. Repeat until the score reaches 8–9 or the user says stop. A score of 10 is not a goal — trying to hit 10 risks overwriting the author's voice.

---

*Tell list adapted from [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Modified and extended for use as a code editor skill.*

*This file is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).*
