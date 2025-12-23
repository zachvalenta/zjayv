+++
title = "agentic"
date = 2025-11-25
+++

* agent: Claude Code
* `docs/` > `CLAUDE.md`
* vim readline, multi-line: `/terminal-setup`

# for bookcase/domains/sw

## context

ok, here's how I'm doing config for CC rn

* `/Users/zach/Documents/denv/dotfiles/ai/claude`

So for some work projects:

* `/Users/zach/Documents/zv/work/kero/src/automation/rush`
* `/Users/zach/Documents/zv/work/kero/docs/agentic`

they point to `kero.md`. Main config from `/Users/zach/.claude` points to `user.md`

But then I got to thinking: I'm one of those crazy Zettelkasten people. Not *exactly* what he describes here, but something along those lines. https://notes.andymatuschak.org/Evergreen_notes

Anyhow, my thinking, given that I have a ton of notes (`/Users/zach/Documents/zv/notes`), why don't I:

* get Claude to write context files for my bookcase, domains, and sw notes and put them here `/Users/zach/Documents/denv/dotfiles/ai/claude/context/notes`
* write some slash comands (`/Users/zach/Documents/denv/dotfiles/ai/claude/commands`) so I can put these contexts to use when I'm working w/ CC

## use cases

To that last point, two things I was thinking about today that could be helped by all this:

* I'm trying to redesign my personal site. `site.md` is about SSGs, but also has a bunch of design stuff in their. I have `frontend.md`, CSS stuff there. And then `design.md` more broadly. So I struggling to articulate what I wanted to do w/ my site and thought "hey, I need to learn the semantics of visual/graphic design". Be nice if I could port what I was learning in my conversation with Claude back to my notes.
* You'll notice that `bookcase` kinda sorta rhymes w/ a bibliography mgmt system like Zotero or this TUI version https://cobib.gitlab.io/cobib/cobib.html -> I'd love to make bookcase less of a mess, and it would help a lot if CC knew about my notes and how bookcase fits in.

## worklogs

Anyway, let's proceed as such, pausing btw step for me to review your work:

- [x] context file for bookcase
- [x] context file for domains
- [x] context file for sw

## slash command

Ok, here's what I'm thinking in terms of slash commands:

```sh
├── commands/notes
│   └── inject-context.md   # pull relevant context note from /Users/zach/Documents/denv/dotfiles/ai/claude/context/notes into context, in order that instead of me manually having to use the @ command, you'll have a much easier/cheaper time figuring out where to look vs. grepping through a ton of files and blowing through a ton of tokens
│   └── improve-context.md  # super version of Claude's @ command, where - if you're taking the trouble of bringing an entire file into memory, use that to also improve the TOPICS/SEARCH/RELATED tags for the file in the relevant context file @ /Users/zach/Documents/denv/dotfiles/ai/claude/context/notes
│   └── rf.md  # propose refactoring the filesystem for better taxonomy | making connections | (re)writing sections using the guidelines from /Users/zach/Documents/denv/dotfiles/ai/claude/context/markdown.md
```

Here's an example of how I imagine this working:
```sh
# CC looks at the CWD's project's spec file + uses context to figure out what languages/frameworks I know best and which ones I'm intrigued by -> throws out some suggestions
/inject-context Hey Claude, I'm trying to think of what the stack should be for $FOO_PROJECT_IN_CWD.
```
```sh
# CC takes the files that it's loaded into memory from /inject-context and uses that to improve the context files
/improve-context
```
```sh
# CC takes the files that it's loaded into memory from /inject-context and uses that to improve the notes themselves
/rf
```

Do you think this makes sense?

If so, which one do you think we should start with?

```sh
This makes a lot of sense. The flow is:

1. inject-context → smart loader (use index to find relevant notes, load them)
2. improve-context → feedback loop (after loading files, improve the index)
3. rf → deeper work (refactor the notes themselves)
```

re: the rf slash cmd, section C is mixing concerns ++ but that's not the real issue. I don't need your help in conforming to my own sui generis Markdown conventions (the fault is entirely my own!). Rather, Markdown guidance is for *you* when you're using the /rf slash command.

Now, while taxonomy and connections are useful aspects of `rf`, the real goal of `rf` - what should really be happening in section C 'content - as stated is: "CC takes the files that it's loaded into memory from /inject-context and uses that to improve the notes themselves". `rf` is the command that *is* - intentionally - token intensive. Here, I'm asking you to use `inject-context` and then go a step further: figure out where roughly in the notes we should be looking at, *then* dive deeper and read the notes and tell me what I know, what I should know, and what I need to know. *This* is the command where you're going to set me straight on compiler design | Django auth plugins | PLT, etc.

---

- [ ] use slash cmd for site design

# current setup

```sh
$ pwd
/Users/zach/Documents/zv/work/kero/src/automation/rush/.claude

$ t

 .
├──  CLAUDE.md -> /Users/zach/Documents/denv/dotfiles/ai/claude/kero.md
├──  commands -> ../../../../docs/agentic/commands
└──  settings.json -> /Users/zach/Documents/denv/dotfiles/ai/claude/settings.json
```

THINGS THAT MATTER
* model
* thinking mode
* perms
* context

WIRING
* db: slash commands symlinked to `$PROJECT/.claude/commands`
* docs: point to from `CLAUDE.md` https://github.com/zachvalenta/dotfiles-mini23/commit/33a4b64da3a67231887bfb17ff48c0e7451b7cd4
* file access: ``/Users/zach/Documents/zv/work/kero/**` | just point! https://code.claude.com/docs/en/common-workflows#reference-files-and-directories

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

# WORKLOG FROM GETTING SLASH COMMANDS GOING

🔗 https://chatgpt.com/c/691a3e15-e294-8333-83b3-d6cddee0b93e

I need a way to bring the database into context for an agent.

## org tools

Here's an example of what that looks like:

```python
"""
Check which specific markets are being published during betstops
"""
import pymongo
client = pymongo.MongoClient(CONN_STRING, directConnection=True)
event_id = event_id
db = client[event_id]
pbp = db["pbp"]
kafka = db["kafka_activity_log"]
markets = db["markets"]
event_info = db["event_info"]

# buncha queries ⬇️ specifics not important right now
```

This is fine enough, but I'd like a more systematized approach:

* seems like db connection and perms should be handled in one place
* seems like there should be a general "here's the bug, here's the codebase, i don't know what to do next so just query around and figure things out"
* seems like there should be many more specifc "here's the bug, here's the codebase, run $QUERY_X|Y|Z and let's see what's going on"

I also don't know what Claude (or more general) functionality I should use to achieve this:

* commands
* subagents
* skills
* memories

Could you provide definitions of these? My hunch is that skills are overkill to start at least, could potentially be useful.

I'd like to wire things up such that:

* things that should be global are global i.e. have a base thing for Mongo to make sure all queries are read-only
* but then have a per-project aspect that handles db connection strings per env (in the event, say, I also need to use Mongo for a different client)

Another wrinkle: while it would be helpful to have `my_docs_on_work` within `repo_I_mostly_work_on`, I'm not running the show, these guys don't care about | hostile to docs, let alone agentic. So I'd like to keep everything I'm using for `repo_I_mostly_work_on` *in* `my_docs_on_work` in a new repo.

```sh
├── work_codebases
│   └── automation
│   └──── repo_I_mostly_work_on
│   └── messagings
│   └── ML
├── my_docs_on_work
│   └── agentic  # new repo for all work scripts/MCP
│   └── eng      # docs that Claude will use
│   └── tickets  # my notes for each Jira ticket
│   └── worklogs # just a log of everything I'm doing during the week
```

FEW MORE THINGS
* There's a kind of file soup rn btw `AGENTS.md`, `CLAUDE.md`, `spec.md`. To me this misses the entire point. On the surface - if you are not serious about documentation - it might seem like some revelation. "Oh, I can write down roughly what the hell is going on and that will *help* the agent??". To me, the idea of docs in a single file is insane unless you're working on something very trivial. I have a docs *repo*. Any way to config Claude Code (or anything else) to use those docs in the same way?
* To what extent can I make this agnostic cross-agent? I'm most familiar with Claude but I have Codex and Gemini installed and I'd like to keep things flexible such that if I want to switch to Crush (https://github.com/charmbracelet/crush) or OpenCode or something else I'm not building my entire life around Claude.
* Seems like this project might be helpful but also maybe bs in the sense "here's how I [this guy] uses Claude, you do the same". It's marketing it as an OS but...seems like just a bunch of Markdown files? https://github.com/buildermethods/agent-os

## point to docs/tools

I need a way to bring my documentation + tools (primarily db access) into context for an agent.

A pretty typical workflow:

* I get a bug report
* figure out what portion(s) of the codebase it touches on
* figure out what tables/records in the database it touches on

Before going further, let's look at my filesystem and how I've set things up for this client [you can see all this from $CWD but here's an abbreviated/annotated version]:

```sh
├── denv  # ignore for now
├── docs
│   └── agentic  # scripts for Claude to pull data into context
│   └── eng      # Markdown notes on the codebase, schema, domain, workflows
│   └── tickets  # Markdown notes on Jira tickets
│   └── worklogs # ignore
├── src
│   └── automation  # my org
│   └──── rush      # repo where I do all my work for now
│   └── messaging   # Kafka, RabbitMQ
│   └── pricing     # ML for pricing markets
```

While it would be helpful to have `agentic`, `eng` etc within the repo where I do most of my work (`automation/rush`), I'm not running the show and the client don't care about | hostile to docs, let alone agentic. So I need to have Claude open with `automation/rush` *but* for Claude to know that it can use `docs/agentic` and `docs/eng` without me telling Claude every time I start a new session.

One suggestion I've seen is to set up an MCP server:
```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y", 
        "@modelcontextprotocol/server-filesystem",
        "/Users/zach/Documents/zv/work/kero/docs/agentic",
        "/Users/zach/Documents/zv/work/kero/docs/eng"
      ]
    }
  }
}
```

I don't know much about MCP. Is this the right approach? -> ANSWER! use MCP for fs access to docs/tools + slash commands to address specific tools

## 📍 db

* does MCP even work?
* how do slash commands work bc claude found this unprompted?
```sh
   /tools:run markets 7_37 7_15_4
   run tool (project)

 Do you want to proceed?
   1. Yes
 ❯ 2. Yes, and don't ask again for /tools:run markets 7_37 7_15_4 in /Users/zach/Documents/zv/work/kero/src/automation/rush
   3. Yes, and don't ask again for /tools:run:* commands in /Users/zach/Documents/zv/work/kero/src/automation/rush
   4. No, and tell Claude what to do differently (esc)
```

## cleanup scripts

```sh
Your scripts follow clear patterns for debugging betting/market issues:

  Script Categories:

  Betstop Debugging:
  - debug_betstop_data.py - Explores betstop event structure in PBP/Kafka
  - check_betstop_markets.py - Analyzes markets around betstop events
  - verify_betstop_fix.py - Validates betstop fixes

  Market Analysis:
  - check_all_markets.py - Market inventory by prefix/status
  - check_deleted_markets.py - Tracks deleted markets
  - debug_lac_orl_markets.py - Game-specific market debugging
  - diagnose_markets_config.py - Tests get_mode() logic for config issues

  Timeline/Events:
  - get_combined_timeline.py - Core utility - Merges PBP + Kafka logs, sorts by game progression
  - check_game_timeline.py - Pre-game window analysis
  - check_event_info_full.py - Complete event metadata
  - compare_events.py - Cross-event comparison

  Code Testing:
  - simulate_pregame_ranking.py - Tests pregame market initialization
  - test_delta_time.py - Time calculation testing
  - test_get_mode.py - Mode detection testing

  Structure Analysis:
  - inspect_pbp_structure.py - PBP record schema exploration
  - check_test_db.py - Test database validation

  Common Patterns:

  1. MongoDB connections (prod/beta with hardcoded creds)
  2. Event-specific queries (uses event_id as DB name)
  3. Cross-collection correlation (PBP ↔ markets ↔ kafka_activity_log)
  4. Code imports from ml_app/ml/* for integration testing

  Key Insight:

  get_combined_timeline.py is your reusable library - it's imported by other scripts and provides the core timeline merging logic that mimics the admin
  dashboard.

  Recommendations:

  1. Update MCP paths - Add docs/agentic/db/ to your MCP config since scripts moved
  2. Extract DB credentials - Move to env vars or shared config
  3. Create helper module - Extract common DB connection logic
  4. Enhance slash commands - Make /agentic-run suggest scripts based on bug type
  5. Consider skills - These could become interactive Claude Code skills
```

## add skills

```sh
my_docs_on_work/
  agentic/
    bin/                  # CLIs the agent can call
      mongo_find
      mongo_stats
      diagnose_event
      dump_markets
      ...
    config/
      global.json         # read-only DB policy, default behaviors
      proj_repo_1.json    # env-specific config for work repo
      proj_repo_2.json
    skills/
      bug_triage.md
      mongo_queries.md
      codebase_navigation.md
    mcp/                  # optional, only if needed
      mongo-mcp/
        index.js
    workflows/
      betstop_diagnosis.md
      market_anomalies.md
      timeline_sync.md
```
