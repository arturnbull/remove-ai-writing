# /remove-ai-writing

A Claude Code slash command that scans files for AI writing tells and helps you fix them.

It flags overused vocabulary ("delve", "tapestry", "landscape"), formulaic patterns (significance puffery, negative parallelisms, rule-of-three lists), and formatting tells (curly quotes, markdown leaking into plain text). Then it scores the text on a 1-10 human writing scale and offers to fix what you select.

## Install

Copy `remove-ai-writing.md` into your Claude Code commands directory:

```bash
# Global (available in all projects)
cp remove-ai-writing.md ~/.claude/commands/

# Project-specific
cp remove-ai-writing.md .claude/commands/
```

Then use it with `/remove-ai-writing` in Claude Code.

## How it works

1. **Scan** - Flags vocabulary, patterns, and formatting tells with line numbers
2. **Score** - Rates the text 1-10 on a human writing scale
3. **Fix** - You choose which items to address (all, specific numbers, or none)
4. **Loop** - Re-scans after fixes, asks if you want another round until score hits 8-9

The goal is 8-9, not 10. Pushing to 10 risks overwriting the author's voice.

## What it catches

**Vocabulary**: ~35 words commonly overused by LLMs (delve, foster, nuanced, pivotal, etc.)

**Patterns**: significance puffery, superficial -ing analysis, negative parallelisms, rule of three, copula avoidance, em dash overuse, elegant variation, promotional tone, vague attribution, despite-challenges formula, didactic disclaimers, formulaic headings

**Formatting**: curly quotes in wrong contexts, markdown leaking into plain text, excessive boldface, inline-header vertical lists

## Attribution

Tell list adapted from [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
