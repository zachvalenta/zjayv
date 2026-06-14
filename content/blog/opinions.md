+++
title = "software principles 8 years in"
date = 2024-09-22
draft = true
+++

---

https://chriskiehl.com/article/thoughts-after-6-years

CURRENT OPINIONS
* Clarity trumps all other concerns.
* Bad code can be written in any paradigm.
* So called "best practices" are contextual and not broadly applicable. Blindly following them makes you an idiot.
> meh
* In general, RDBMS > NoSql.

> these two seem to have been in the original article but later edited out
* The word "scalable" has a mystical and stupefying power over the mind of the software engineer. Its mere utterance can whip them into a depraved frenzy. Grim actions have been justified using this word
* Despite being called "engineers" most decisions are pure cargo-cult with no backing analysis, data, or numbers.

* The top ~10% of project managers are wildly underrated in importance and the other ~90% could disappear tomorrow to either no effect or a net gain in efficiency.
* Interviewing in tech is folkloric and irrational and also seems to be as good or better than most industries.

https://news.ycombinator.com/item?id=44558151
Do the dumbest thing first until it doesn't work anymore

https://rfc.earendil.com/0020/

https://news.ycombinator.com/item?id=48106024

Rob Pike https://news.ycombinator.com/item?id=47423647

* deliverance
> It's funny to me how still so many don't realize you don't get hired for the best positions for being a 10x programmer who excels at hackerrank, you get hired for your proven ability to deliver useful products. Creativity, drive, vision, whatever. Code is a means to an end. If you're the type of programmer who thinks of yourself as just a programmer, and take pride in your secure code, ability to optimize functions and algorithms, you're exactly the kind of programmer AI will replace. https://news.ycombinator.com/item?id=47031587

https://simonwillison.net/2025/Dec/18/code-proven-to-work/
https://news.ycombinator.com/item?id=47390383
https://buttondown.com/hillelwayne/archive/choose-boring-technology-and-innovative-practices/

## simplicity

* Most powerful things can be much simpler. https://news.ycombinator.com/item?id=46781566

> Contrary to popular belief, simplicity is also not the first attempt but the hardest revision. https://github.com/tigerbeetle/tigerbeetle/blob/main/docs/TIGER_STYLE.md

> Simple is not given. It takes constant work. https://chriskiehl.com/article/thoughts-after-10-years

* simplicity takes time.
> A complex system that works is invariably found to have evolved from a simple system that worked. A complex system designed from scratch never works and cannot be patched up to make it work. You have to start over with a working simple system. https://news.ycombinator.com/item?id=42668065

## clarity

* Reabability is table stakes.
* Doctest: If someone can't start a REPL and run what's in your doctest, the code in question is failing.
* Docstrings: If someone can't read a docstring and grok context, the code in question is failing.
* Commit messages are held to the same standard as docstrings.

## precision

Good integration tests are more important than unit test coverage.

[Centralize control flow.](https://matklad.github.io/2023/11/15/push-ifs-up-and-fors-down.html)

Semantics: naming things is hard. We'll refactor until we get it right. Bad semantics metastasize confusion and will not be tolerated.

> Get the nouns and verbs just right. Great names are the essence of great code, they capture what a thing is or does, and provide a crisp, intuitive mental model. They show that you understand the domain. Take time to find the perfect name, to find nouns and verbs that work together, so that the whole is greater than the sum of its parts. - [Tigerbeetle](https://github.com/tigerbeetle/tigerbeetle/blob/main/docs/TIGER_STYLE.md)

