# AGENT

## Core rules

- prefer small, incremental changes
- keep the book renderable
- do not silently restructure the table of contents without updating `_quarto.yml`
- keep chapter prose readable and compact
- write code examples that are executable and teach something concrete
- extract repeated helper logic into `tools/`
- update docs when structure or workflow changes
- surface assumptions explicitly
- avoid hidden scope expansion

## Division of labor

### ChatGPT should own
- chapter sequencing
- deciding how concepts should be introduced
- tradeoff analysis about scope and organization
- editorial consistency across chapters
- deciding when examples belong in chapters versus tools

### Coding agents should own
- creating and editing files
- refactoring repeated helper code
- fixing render issues
- wiring up dependencies
- adding tests for helper modules

## When to escalate

Ask for a plan refresh before:
- large table-of-contents changes
- introducing heavy dependencies
- turning a chapter example into a package
- changing the teaching level of the book

## Handoff format

When completing work, report:
- files changed
- what was added or revised
- assumptions made
- anything still blocked or unresolved

## Chapter conventions

- start with why the concept matters in synbio
- introduce one clean working example early
- build complexity gradually
- show outputs when practical
- end with exercises, prompts, or extensions when useful

## Code conventions

- prefer clear Python over clever Python
- keep imports minimal
- comment only when it improves understanding
- use plotting sparingly and meaningfully
- make examples robust to re-execution
