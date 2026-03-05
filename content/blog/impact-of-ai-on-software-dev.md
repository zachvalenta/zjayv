+++
title = "impact of AI on software development"
date = 2025-10-27
+++

for the layman https://www.nytimes.com/2026/03/12/magazine/ai-coding-programming-jobs-claude-chatgpt.html

> Ryan Dahl, creator of Node.js, with another toll of the bell: "This has been said a thousand times before, but allow me to add my own voice: the era of humans writing code is over. Disturbing for those of us who identify as SWEs, but no less true. That's not to say SWEs don't have work to do, but writing syntax directly is not it." https://registerspill.thorstenball.com/p/joy-and-curiosity-71

* the code itself is cattle, not a pet https://x.com/thorstenball/status/2013619012932947993
* https://news.ycombinator.com/item?id=47050421
* https://simonwillison.net/2026/Feb/18/typing/
* https://www.seangoedecke.com/how-does-ai-impact-skill-formation/
* lol DDD / write things down https://simonwillison.net/2026/Feb/15/cognitive-debt/#atom-everything
* https://lucumr.pocoo.org/2026/2/13/the-final-bottleneck/
* most people don't want to build anything, MOOC https://www.youtube.com/watch?v=jgLJ5xas2ow
* https://www.chrisgregori.dev/opinion/code-is-cheap-now-software-isnt
* https://simonwillison.net/2026/Feb/18/martin-fowler/

🗄️
* `eng/doc.md`
* `linguistics.md` determinism
* `media.md` print culture

```python
a = "hey"
b = a
a is b  # True
b is a  # True
```

```sh
# msg to Roberto

agentic is getting a lot of hype but deserved IMO.

if you had to make a timeline of things that really changed the profession:

* machine code
* compiled languages
* personal computers, Java popularizes garbage collection
* the internet, high-level languages (Python, visual basic)
* Stack Overflow
* agentic

i would have agentic on there.

and maybe the most important to what it means to be a software dev.
```

# 🚧 dump from `agentic.md`

* non-local experiments (avoid pkg installs, etc.) https://simonwillison.net/2025/Nov/6/async-code-research/

---

* woodchipper https://simonwillison.net/2025/Mar/9/steve-yegge/
new languages https://simonwillison.net/2025/Nov/7/llms-for-new-programming-languages/
* https://news.ycombinator.com/item?id=44322465 https://news.ycombinator.com/item?id=44315505
* https://colton.dev/blog/curing-your-ai-10x-engineer-imposter-syndrome/
https://simonwillison.net/2025/Oct/11/vibing-a-non-trivial-ghostty-feature/
https://simonwillison.net/2025/Oct/10/superpowers/
* https://github.com/humanlayer/advanced-context-engineering-for-coding-agents/blob/main/ace-fca.md
* METR study, actually not effective? https://www.astralcodexten.com/p/links-for-september-2025
* https://www.scattered-thoughts.net/writing/everyones-got-one/
* https://blog.florianherrengt.com/vibe-coder-career-path.html
* garbage in garbage out
> OpenAI published a very long guide to ‘prompt engineering’ for GPT-4.1. I find this kind of stuff unintentionally hilarious: if your thesis is that these models are replacing software, why do I need to memorise incantations and learn what JSON means to get the best results? All of this should be abstracted away. - Ben Evans 25.05.20
* https://simonwillison.net/2025/Apr/20/ethan-mollick/
* https://news.ycombinator.com/item?id=43752492
* teaching people how to ask better questions https://paulgraham.com/writes.html
* Stack Overflow won in losing https://x.com/Altimor/status/1853893158368928124
* Cursor files https://getstream.io/blog/cursor-ai-large-projects/
* docs https://news.ycombinator.com/item?id=45884169
* autocomplete is not the reason https://www.arguingwithalgorithms.com/posts/cursor-review.html https://ghuntley.com/stdlib/
> learn how to fucking type (and how to write https://news.ycombinator.com/item?id=43739400)
* writing https://johnstone.substack.com/p/friction-was-the-feature
> Harper on An LLM Codegen Hero's Journey: "Writing skills have become critical. While we’ve always valued strong communicators on tech teams for documentation and collaboration, it’s doubly important now." One hundred thousand percent correct, I’d say. This week I gave a little talk on how to write better prompts when using Amp and I had a slide in there that said: what makes a good prompt are the same things that make a good ticket and good bug report
> have standards 💡️ use AI to write docs and understand the entire architecture of the system https://www.driver.ai/
* `.cursor/rules`/`.cursorrules` https://www.nickcraux.com/blog/cursor-tip https://news.ycombinator.com/item?id=43341506 https://docs.cursor.com/context/rules-for-ai https://news.ycombinator.com/item?id=43658923
> Eng leadership at my place are pushing Cursor pretty hard. It's great for banging out small tickets and improving the product incrementally kaizen-style, but it falls down with anything heavy. I think it's weakening junior engineers' reasoning and coding abilities as they become reliant on it without having lived for long, or at all, in the before times. I think may be doing the same to me too...As with so many products, it's cheap to start with, you become dependent on it, then one day it's not cheap and you're fucked.
* what I use it for (beyond code): summarization, taxonomization, big picture, learning new concepts (regression, dimensional analysis) https://github.com/zachvalenta/apple-models-data-analysis
> that little repo took me ~30 minutes total work, spanning initial idea to completion. that * ideas in a day * days in a year has been a massive delta for me. ++ I feel like my ability to use AI tooling well growing exponentially. diff btw today vs. a month ago night and day.
* misunderstanding https://www.youtube.com/watch?v=dkV01hBdhZE https://registerspill.thorstenball.com/p/they-all-use-it https://news.ycombinator.com/item?id=41930767
makes mistakes all the time but that's why we're here! re: `direnv` https://chatgpt.com/c/673f8c16-e090-8004-bdc8-564bbfeb33d5
> The crux of my raging hatred is not that I hate LLMs or the generative AI craze. I had my fun with Copilot before I decided that it was making me stupider - it's impressive, but not actually suitable for anything more than churning out boilerplate. Nothing wrong with that, but it did not end up being the crazy productivity booster that I thought it would be, because programming is designing and these tools aren't good enough (yet) to assist me with this seriously. https://ludic.mataroa.blog/blog/i-will-fucking-piledrive-you-if-you-mention-ai-again/
> LLMs are good at explaining code. Give it code in a language you don't understand and it will explain it with 90% accuracy. https://katherinemichel.github.io/portfolio/pycon-us-2024-recap.html#simon-willison-keynote
https://www.youtube.com/watch?v=ImNpR0O8nuA
https://marginalrevolution.com/marginalrevolution/2025/02/o1-pro.html
forcing people to think through things https://x.com/RealGeneKim/status/1853860996689064211
https://registerspill.thorstenball.com/p/surely-not-all-codes-worth-it https://registerspill.thorstenball.com/p/how-might-ai-change-programming
sketching https://simonwillison.net/2024/Dec/4/steve-yegge/
https://x.com/barbell_fi
https://simonwillison.net/2023/Dec/31/ai-in-2023/
https://simonwillison.net/2024/Dec/11/who-and-what-comprise-ai-skepticism/#atom-everything
https://simonwillison.net/2024/Dec/10/ethan-mollick/
* https://simonwillison.net/2025/Apr/7/john-carmack/
* https://www.thoughtworks.com/radar/techniques/observability-2-0 https://claude.ai/chat/6bcfcae0-6294-47ef-a3bf-588a7f178c0e
* https://crawshaw.io/blog/programming-with-llms

# writing

🗄️ `notes.md` practice

> All the principles of software engineering are not really about code per se.  They are about how to organize the highly detailed specification of a product. https://x.com/unclebobmartin/status/2022016179943117294

---

>  It’s from 2023 and that made me think that today, in 2026, no one would write a blog post like this, because why would you if anyone can press a button to have a custom version of this post generated for them? And that in turn made me wonder: but people will write in the future too and once we’ve crossed through the transitional period we’re in, what will those posts look like? https://registerspill.thorstenball.com/p/joy-and-curiosity-77

* have good incentives now! https://news.ycombinator.com/item?id=45623083
> If your project has a robust, comprehensive and stable test suite agentic coding tools can fly with it. Without tests? Your agent might claim something works without having actually tested it at all, plus any new change could break an unrelated feature without you realizing it. Test-first development is particularly effective with agents that can iterate in a loop. https://simonwillison.net/2025/Oct/7/vibe-engineering/
* https://www.sudowrite.com/
* 📙 Ousterhout comments first [131]
* https://simonwillison.net/2025/May/20/after-months-of-coding-with-llms/
* https://bsky.app/profile/emollick.bsky.social/post/3lp5afidgvc2a
> https://news.ycombinator.com/item?id=42095434 there's a fair amount of pushback as well. i align with the first comment to this guy. decent amount of pushback seems like: "im a real man, my editor is emacs, i have strong opinions about c99 vs. rust, LLMs are for wimps who write $DYNAMICALLY_TYPED_LANGUAGE_HERE" + people that are bad at writing prompts. essentially, LLMs reward the type of person who could write a good question on Stack Overflow or otherwise teaches them how to do so (if they are willing to learn) https://stackoverflow.com/help/mcve - to Josh/Kurt 24.11.15
> PG might be right for most people but I estimate that LLMs will actually make their users *better* at writing clearly. Will take the Stack Overflow ethos to a wider audience. https://stackoverflow.com/help/how-to-ask

# spec > all

https://simonwillison.net/2026/Feb/25/closed-tests/

# architecture

---

* https://simonwillison.net/2026/Mar/12/les-orchard/
> Ryan Dahl, creator of Node.js, with another toll of the bell: "This has been said a thousand times before, but allow me to add my own voice: the era of humans writing code is over. Disturbing for those of us who identify as SWEs, but no less true. That's not to say SWEs don't have work to do, but writing syntax directly is not it." https://registerspill.thorstenball.com/p/joy-and-curiosity-71
* https://x.com/goinggodotnet/status/2012209293651501069
> Martin Kleppmann: “I find it exciting to think that we could just specify in a high-level, declarative way the properties that we want some piece of code to have, and then to vibe code the implementation along with a proof that it satisfies the specification. That would totally change the nature of software development: we wouldn’t even need to bother looking at the AI-generated code any more, just like we don’t bother looking at the machine code generated by a compiler.” https://registerspill.thorstenball.com/p/joy-and-curiosity-67
* https://news.ycombinator.com/item?id=46197930
> I believe the next year will show that the role of the traditional software engineer is dead. If you got into this career because you love writing lines of code, I have some bad news for you: it’s over. The machines will be writing most of the code from here on out. Although there is some artisanal stuff that will remain in the realm of hand written code, it will be deeply in the minority of what gets produced. https://registerspill.thorstenball.com/p/joy-and-curiosity-63
> 90% of my skills just went to zero dollars and 10% of my skills just went up 1000x. - Kent Beck https://simonwillison.net/2025/Jun/22/kent-beck/
* https://news.ycombinator.com/item?id=42336553
* ADRs / Stack Overflow won https://harper.blog/2025/04/17/an-llm-codegen-heros-journey/ https://registerspill.thorstenball.com/p/joy-and-curiosity-36 https://mathstodon.xyz/@tao/110601051375142142
> While we’ve always valued strong communicators on tech teams for documentation and collaboration, it’s doubly important now. Not only do you need to communicate with humans, you need to write clear, precise instructions for AI. Being able to craft effective prompts is becoming as vital as writing good code.
> Suddenly you find yourself building out very robust specs, PRDs, and to-do docs.
* https://steve-yegge.blogspot.com/2008/09/programmings-dirtiest-little-secret.html
> For starters, non-typists are almost invisible. They don't leave a footprint in our online community...design involves communicating with other people, and design involves a persistent record of the decision tree.
>"And as for this non-college bullshit I got two words for that: learn to fuckin' type."

# vibe coding

---

* https://simonwillison.net/2025/Dec/16/gemini-thinking-trace/
* CQ https://news.ycombinator.com/item?id=45659881
* Github spark, Claude artifacts https://github.com/features/spark
> Sparks apps are client-side apps built with React
> They are authenticated: users must have a GitHub account to access them, and the user’s GitHub identity is then made available to the app.
> They can store data! GitHub provides a persistent server-side key/value storage API.
* https://simonwillison.net/2025/May/1/not-vibe-coding/
* good for MVPs https://news.ycombinator.com/item?id=43576813
* https://simonwillison.net/2025/Mar/6/vibe-coding/ https://simonwillison.net/2025/Mar/19/vibe-coding/ https://www.youtube.com/watch?v=YWwS911iLhg

# 10x

---

* legal / medical https://www.reddit.com/r/ChatGPTPro/comments/1mt5igj/what_is_the_most_profitable_thing_you_have_done/
* https://simonwillison.net/2024/Oct/21/claude-artifacts/
* supercharged smart young people https://www.youtube.com/watch?v=OmiwV8kUz2E https://www.bitecode.dev/p/what-if-ai-eventually-make-programmers
* https://marginalrevolution.com/marginalrevolution/2024/12/why-you-should-be-talking-with-gpt-about-philosophy.html
> this sounds hyperbolic, but i think AI is going to be akin to the dawn of relational databases in the 80s when it comes to the software industry. re: orgs.  take databases: "no you dont need all those people punching up figures. you can replace all your accountants and secretaries with cobol!". -> do we have more or less jobs centered around the production/maintenance/whatever of business data in 2024 than we did in 1974? it would seem to me a great deal more. dunno if this will hold for number of devs, but feel >=50% that there will be a fuck ton more code written in 5 years than today. bigger economy = longer tail
> The amount of money flowing through capitalism would astound you. The number and variety of firms participating in the economy would astound you. We don't see most of it every day for the same reason abstractions protect us from having to care about metallurgy while programming. - McKenzie https://twitter.com/patio11/status/936629780719419392
> AI as a mechanical arm - you still need to know how to hit the ball, but once you do, it'll go a lot further. https://registerspill.thorstenball.com/p/joy-and-curiosity-36

# you still need to know things

https://x.com/naval/status/2024700227111047581 https://www.lennysnewsletter.com/p/marc-andreessen-the-real-ai-boom
https://news.ycombinator.com/item?id=47001011
https://news.ycombinator.com/item?id=46759063
https://x.com/esrtweet/status/2019779602617376788
https://x.com/esrtweet/status/2019562859978539342

https://news.ycombinator.com/item?id=46782811
> The uncomfortable part: if your value was being the person who could grind through tedious work, that's no longer a moat. Orchestration and judgment are what's left. 
> I've been saying it this whole time; it's not the engineers who need to be concerned with being replaced - it's anyone involved in the busywork cycle. This includes those who do busywork (grinding through tedium) and those who create it (MBAs, without apologies to the author).

* https://news.ycombinator.com/item?id=46850588
* https://news.ycombinator.com/item?id=46765774
* https://simonwillison.net/2026/Jan/24/jasmine-sun/
> while software development as we know it is dead, software engineering is alive and well https://mike.tech/blog/death-of-software-development
reality has a surprising amount of detail https://news.ycombinator.com/item?id=46664635
https://simonwillison.net/2025/Dec/29/jason-gorman/
* purity tests https://news.ycombinator.com/item?id=46365239
* layman unleashes on his laptop https://www.lennysnewsletter.com/p/everyone-should-be-using-claude-code https://www.reddit.com/r/ClaudeCode/comments/1prn6nd/comment/nv3dc9i/
https://news.ycombinator.com/item?id=46080498
> “When thinking about coding with LLMs, think of them as generators of templates. You say what code you need, and an LLM provides you with a template from a collection that most closely resembles the code you needed.” I’ve said something similar in different conversations these past few weeks and that I’ve begun thinking of LLMs-as-code-assistant more in the category of frameworks and generators than magic wands. https://registerspill.thorstenball.com/p/joy-and-curiosity-23
> If you can make all of those trades, you can use agentic coding tools to produce software not merely faster than before, but better. But to do so, you need to know quite a lot about building good software already. If you've been building software poorly, agentic coding tools are just going to help you do so faster. https://davegriffith.substack.com/p/software-development-in-the-time

# flood of idiots

https://simonwillison.net/2026/Mar/17/tim-schilling/
https://news.ycombinator.com/item?id=47390383
https://simonwillison.net/2025/Dec/18/code-proven-to-work/

# languages

* Golang, Rust, Haskell https://news.ycombinator.com/item?id=47222270

# Jevons

https://simonwillison.net/2026/Jan/8/llm-predictions-for-2026/
https://registerspill.thorstenball.com/p/joy-and-curiosity-69
https://wesmckinney.com/blog/mythical-agent-month/

# the thing itself

> the job of a software engineer isn’t to write code, it’s to deliver code that works. https://simonwillison.net/2026/Feb/10/showboat-and-rodney/

# bespoke

https://simonwillison.net/2026/Mar/13/craig-mod/
https://news.ycombinator.com/item?id=47060206
https://news.ycombinator.com/item?id=47059997
https://news.ycombinator.com/item?id=46436186
https://news.ycombinator.com/item?id=46436427
https://news.ycombinator.com/item?id=46772132
> Steve Ruiz, founder and CEO of tldraw, with thoughts on AI and open source and why they shut down external contributions to tldraw: stay away from my trash! It’s very thoughtful and interesting (I haven’t looked at open source contributions in a year and have no clue what it’s like to be in the war zone) and I think what he writes here rhymes with my “Is GitHub dead?” video from above: “The question is more fundamental. In a world of AI coding assistants, is code from external contributors actually valuable at all? If writing the code is the easy part, why would I want someone else to write it? […] But if you ask me, the bigger threat to GitHub’s model comes from the rapid devaluation of someone else’s code. When code was hard to write and low-effort work was easy to identify, it was worth the cost to review the good stuff. If code is easy to write and bad work is virtually indistinguishable from good, then the value of external contribution is probably less than zero.” https://registerspill.thorstenball.com/p/joy-and-curiosity-71
https://changelog.com/friends/126
https://news.ycombinator.com/item?id=46888441
https://danluu.com/sounds-easy/
https://simonwillison.net/2026/Feb/7/david-crawshaw/

> “Clawdbot is a boutique, nerdy project right now, but consider it as an underlying trend going forward: when the major consumer LLMs become smart and intuitive enough to adapt to you on-demand for any given functionality – when you’ll eventually be able to ask Claude or ChatGPT to do or create anything on your computer with no Terminal UI – what will become of ‘apps’ created by professional developers? I especially worry about standalone utility apps: if Clawdbot can create a virtual remote for my LG television (something I did) or give me a personalized report with voice every morning (another cron job I set up) that work exactly the way I want, why should I even bother going to the App Store to look for pre-built solutions made by someone else? What happens to Shortcuts when any ‘automation’ I may want to carefully create is actually just a text message to a digital assistant away?” That’s by Federico Viticci. I think he has programming chops, but I don’t think he’s worked as a software engineer and, well, now he’s also seeing it: a lot of software is going to die in the next few years. Don’t make the mistake and think that there’ll be announcements or funerals. https://registerspill.thorstenball.com/p/joy-and-curiosity-73

# era

> An invitation by Nolan Lawson to mourn our craft. “Someday years from now we will look back on the era when we were the last generation to code by hand. We’ll laugh and explain to our grandkids how silly it was that we typed out JavaScript syntax with our fingers. But secretly we’ll miss it.” https://registerspill.thorstenball.com/p/joy-and-curiosity-73
> Steven Sinofsky, who’s seen quite a few platform and paradigm shifts from up close: “Death of Software. Nah.” He’s saying that “there will be more software than ever before. This is not just because of AI coding or agents building products or whatever. It is because we are nowhere near meeting the demand for what software can do.” And “new tools will be created with AI that do new things.” And also: “Finally, it is absolutely true that some companies will not make it. It is even true that in some very long time, longer than a career or generation, every company will be completely different or their product line and organization will have dramatically changed. This will not broadly happen on any investing timeline.” https://registerspill.thorstenball.com/p/joy-and-curiosity-73
> Jo Kristian Bergum with some very good thoughts on the future: “few things are worth building.” The value of 10k lines of code is approaching $0, he says, and a lot of things will disappear along with the value these lines once held. “What survives? Systems that compress hard-won insights agents would have to rediscover at enormous token cost. Systems that operate on a cheaper substrate than inference. Systems that solve hard universal problems agents can’t route around easily. Systems built for how agents actually work, not how we wish they worked.” The point about the “cheaper substrate” is something I flip back and forth on. Let’s see how it plays out. https://registerspill.thorstenball.com/p/joy-and-curiosity-73

# copying

* https://news.ycombinator.com/item?id=46654726
https://news.ycombinator.com/item?id=46271703
https://news.ycombinator.com/item?id=46272230
https://news.ycombinator.com/item?id=46268959

# people are still not using it

> I fell into an agentic coding hole earlier this year and I still haven't recovered from it. https://www.youtube.com/watch?v=tt3kY19ciFA

* https://news.ycombinator.com/item?id=46691243
* version control needs to change https://lucumr.pocoo.org/2025/12/22/a-year-of-vibes/
* https://x.com/karpathy/status/2004607146781278521
* https://blog.kierangill.xyz/oversight-and-guidance
* leave it to Kent to see it https://simonwillison.net/2025/Dec/16/kent-beck/
* even the power users are still dim! https://news.ycombinator.com/item?id=46255285
* https://lucumr.pocoo.org/2025/9/29/90-percent/
* pro https://martinalderson.com/posts/has-the-cost-of-software-just-dropped-90-percent/ https://news.ycombinator.com/item?id=46196228
* con https://andyljones.com/posts/horses.html https://news.ycombinator.com/item?id=46199723 pro https://news.ycombinator.com/item?id=46200455
* https://simonwillison.net/2024/Dec/31/llms-in-2024/#knowledge-is-incredibly-unevenly-distributed
* https://news.ycombinator.com/item?id=46207505
* https://news.ycombinator.com/item?id=46227422
* writing an algebra book https://x.com/robertghrist/status/1874105564051234951
* Armin https://www.youtube.com/watch?v=tt3kY19ciFA

# trust

https://github.com/mitchellh/vouch
https://news.ycombinator.com/item?id=47300772

# attribution

* https://simonwillison.net/2026/Mar/12/malus/ https://malus.sh/
* https://news.ycombinator.com/item?id=47259177
* licensing https://news.ycombinator.com/item?id=47257803 https://simonwillison.net/2026/Mar/5/chardet/ https://news.ycombinator.com/item?id=47263048 https://news.ycombinator.com/item?id=47259177
* https://github.com/rockorager/prise
* https://github.com/OlaProeis/Ferrite
* https://claude.ai/chat/8fa92c03-4e16-4fa8-a36c-c49d251ac426
* https://news.ycombinator.com/item?id=45865886
* https://simonwillison.net/2026/Jan/11/answers/

# job apocalypse

⬇️ me to Roberto 26.02.16

easier to replace junior / mid-tier devs and leave the truly hard stuff for the seniors / STEM degree people.

on the other hand, if frontier models are better than STEM people at almost any algos-data-structure-401 type stuff, the differentiators becomes:

* business savvy
* domain knowledge
* having taste to know what you *should* or *could* build
* being good at agentic!
* being able to write well!
* reasonable WPM typing -> the whole "code is read much more than it is written" is even more true today (if agents are writing 95% of the code), yet weirdly the *total amount* of writing will go *way* up bc you're talking to agents all day.
* dev experience: you still need to know a lot to direct the model to build non-trivial things that are reliable enough and you don't waste thousands on tokens
* an interest! most computer people hate computers, let alone laymen. if agentic makes it much easier to build software...much more software is going to be built. and we're going to need people to build it.

# not a SaaS killer

https://news.ycombinator.com/item?id=47024387

⬇️ me to Roberto 26.02.16

Weirdly, my biggest fear is that most business / gov *don't actually want better software*. They're not actually trying to | can't get better as organizations, let alone have snazzier software to help them do it. They of course would never say that; the sociology/psychology term for this is 'revealed preference':

> Take climate change, an issue with some odd dynamics. It is a very important issue, but most people don’t think it’s a very important issue. A lot of issues have that same structure (global public health, lead contamination, pandemic prevention, asteroid detection, animal welfare), but unlike the typical important neglected issue, climate has a ton of money behind it. The actual state of opinion on climate is hard to characterize, but I think it’s summed up pretty well by these two facts: 69% of Americans say the United States should take "aggressive" action to fight climate change. 34% of Americans say they would be willing to pay $100 more in taxes per year to curb emissions. In other words — people kind of care about this, but they sort of don’t really. https://www.slowboring.com/p/progressives-mobilization-delusion

So the super power of agentic will matter to enterprise insofar as they can fire X% of the eng org.

The potential counterbalance is that there will be many, many new and small SaaS companies. You hear people say things like "oh, agentic, SaaS is dead, you can build Salesforce in a weekend". Kinda true, but see my bullet points above. There are very few people who check all these boxes! Plus, you need to sell the damn thing to the happy-enough customers of whatever thing you're trying to displace. Some/many SaaS companies will get killed, but it will be much harder to kill them than people assume today. + domain knowledge i.e. there's a site that my dad uses to buy tires, like maybe I can come up w/ better software than them but...where am I sourcing the tires from? inventory mgmt? sales? I would have *no chance* at displacing them even if you gave me all the tokens in the world.
