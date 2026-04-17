# /remove-ai-writing

AI writing is a plague. 

But sometimes it's helpful to edit rather than start from scratch. Better still if that first draft doesn't start out as full-on slop. 
Or run it on your own writing to make sure you're not accidentally coming across as a large language model.

**/remove-ai-writing** is a Claude Code slash command (i.e. skill) that scans files for AI writing tells and helps you fix them. 

This is a simple skill intended to clean up the worst offenses in AI writing. But if communication is important to you, I highly recommend you write for yourself. As a reader, I want to hear your unique voice, not the sanitized robot version.

The skill is based on [Wikipedia's Signs of AI Writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). It flags overused vocabulary, formulaic patterns, and formatting tells. It scores the text on a 1-10 human writing scale and offers to fix what you select. A final prompt at the end offers to run the skill again if the score is low, as sometimes it seems to take a couple passes. At a bare minimum, you should run another pass on the final output with your own eyes and brain.

## Install

**Option 1:**
Tell your favourite AI bot to download and install the skill from github.com/arturnbull/remove-ai-writing.

**Option 2:**
Download or copy the text file from this repository.
Give it to your robot companion and tell them to create a skill for you.

---

**Option 3** (according to Claude):

Copy `remove-ai-writing.md` into your Claude Code commands directory:

```bash
# Global (available in all projects)
cp remove-ai-writing.md ~/.claude/commands/

# Project-specific
cp remove-ai-writing.md .claude/commands/
```

Then use it with `/remove-ai-writing` in Claude Code.

## How it works

1. **Scan**
Flags vocabulary, patterns, and formatting tells with line numbers
2. **Score**
Rates the text 1-10 on a human writing scale
3. **Fix**
You choose which items to address (all, specific numbers, or none)
4. **Loop** 
Re-scans after fixes, asks if you want another round until score hits 8-9

The skill is set to reach 8-9, not 10 so as not to strip out your own contributions.

## What it catches

**Vocabulary**: ~35 words commonly overused by LLMs (delve, foster, nuanced, pivotal, etc.)

**Patterns**: significance puffery, superficial -ing analysis, negative parallelisms, rule of three, copula avoidance, em dash overuse, elegant variation, promotional tone, vague attribution, despite-challenges formula, didactic disclaimers, formulaic headings

**Formatting**: curly quotes in wrong contexts, markdown leaking into plain text, excessive boldface, inline-header vertical lists

## Attribution

Tell list adapted from [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
