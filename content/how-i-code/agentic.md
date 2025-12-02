+++
title = "agentic"
date = 2025-11-25
+++

* agent: Claude Code
* `docs/` > `CLAUDE.md`
* vim readline, multi-line: `/terminal-setup`

# what I'm looking for in an AI agent

REQUIREMENTS
* read user-configured docs on startup / without prompting
* use user-configured tools to connect and read from db
* doesn't prompt me for perms all the time; either default or allow user to config such that agent will just read/edit files and run typical bash commands (cat, ls, etc.) without asking for perms

Seems like it should be fairly straight forward. Surprised that Claude Code - supposedly best in class - is not cutting it.

Other agents I know about:

* Crush
* Codex
* Gemini
* OpenCode

Tell me how each would accomplish my requirements.

# gimme the data!

🔗 https://chatgpt.com/c/691a3e15-e294-8333-83b3-d6cddee0b93e

A pretty typical workflow:

* I get a bug report
* figure out what portion(s) of the codebase it touches on
* figure out what tables/records in the database it touches on

Right now, Claude Code and other agents are great at looking at a bug report and then looking at the codebase, but: what about the data?!

I asked an LLM about this a couple months ago:
* prompt: "What I'm envisioning: in the same way you open Claude Code or Codex in a repo and can start asking questions of the codebase, you could *at the same time* give Claude Code | Codex your db creds and it could 'see' both the database and code at the same time. Feels like this should exist / exists already and I just don't know about it."
* completion: "I'll walk you through hooking up a CLI LLM interface to a database. This is a great use case for natural language data queries!"

This is not at all what I'm after. I feel like I see a lot of BI tools in this space and the pitch is something fit for an advert: "What going on with sales this quarter?" And then some stupid bar chart pops up.

Their workflow:
* takes natural language questions
* converts to SQL
* exec against db Which is all well and good, but I need the data working in concert with what agents can already do in terms of codebase analysis.

A standalone CLI that hooked up an LLM to the database is definitely helpful, but surfacing the db to a pre-existing agent seems both faster (in terms of my dev time) and more powerful. Just for reference, here's my taxonomy of a bunch of stuff in this space:
