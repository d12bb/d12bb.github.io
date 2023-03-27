+++
title = "Lessons learned doing Advent of Code one language a day"
description = "I did Advent of Code 2022 using a different language each day. Here's what I've learned."
+++

I've done little [Advent of Code](https://adventofcode.com) over the past years, but last November, I decided to be more ambitious. Coming December, I'd do each exercise on the day it comes out where work permits, and little later if too busy. And to add to that already kinda hard challenge, I'd use a different language for every day of the challenge. Having no formal education in computer science, AoC is not exactly easy for me. I'm mostly self-taught, I don't know lots of algorithms, and I obviously don't have the experience of someone spending every working day solving challenges in actual production code.

27 days later, I've [solved the whole thing](https://github.com/d12bb/AdventOfCode/tree/main/2022) (ignoring day 17 part two, which I'll surely do *someday*…), being very proud of myself for actually accomplishing the goal of using 25 languages for 25 days, even finishing just two days late. So, what did I learn doing this challenge, and would I do it again? To answer the latter question first: no. More on that later.

### Languages
These are the languages I've used for each day, including a small remark:

1. **Rust**. I love this language!
2. **Go**. `if err != nil` and `switch`eroo…
3. **Python**. I use tabs, btw.
4. **C**. Took me a while, glad I got this over and done with.
5. **Ruby**. Long time since I last used this one.
6. **Clojure**. If only it wasn't built on Java…
7. **Lua**. Got lucky, no off-by-one errors today.
8. **VimScript**. Thank goodness there's Neovim with Fennel nowadays.
9. **Zig**. Interesting language, just see no use over Rust for me.
10. **Fish**. Really a more friendly shell.
11. **Raku** (Perl 6). `grammar` looks nice.
12. **Swift**. Kinda torn on this one.
13. **Haskell**. GHC warns when using tabs, just why?
14. **Nim**. Compiled and statically-typed Python: Nice. Not allowing tabs for indention: Not nice.
15. **Elixir** (and Rust). Got bit by linked lists today, part two would run for hours, probably trying to concat lists.
16. **Crystal**. Ruby, compiled.
17. **Dart**. Feels like C with modern types.
18. **Racket**. Try the rainbow, use a rainbow (plugin).
19. **PHP**. WTF.
20. **D**. A systems programming language with GC by default.
21. **Pascal**. Felt great using that again. I learned programming using Delphi back then.
22. **Odin**. Feels a lot like Go. Much nicer name though!
23. **TypeScript**. Better than JS. But it's still JS…
24. **Julia**. Bit minimal for my taste.
25. **Objective C**. Objective weirdness.

### Lessons learned
* It takes time. A lot. Most of the languages I used, I’ve never touched before. So I had to make myself familiar with the most basic of its syntax and concepts before even starting to think about solving the day. I probably spent the same amount of time or more reading documentation as actually writing code or thinking about the problem at hand.
* It’s not easy. Easy days are still manageable, while hard days get even harder as concentration is split between thinking algorithms and trying to make an unfamiliar language do what I want.
* Tooling is everything. Having a good language server or other means of help while editing makes this a lot easier, as one can just try autocompleting stuff instead of having to look up absolutely everything in the documentation.
* Some languages are harder than others. There are multiple factors for that: Obviously, languages similar to ones I’m used with were easier than, for example, functional languages like Haskell. Also, to state the obvious, high-level languages are easier than low-level ones. I guess difficulty of language is a highly personal thing.
* Sometimes it doesn’t work. After waiting multiple hours waiting for my Elixir implementation of day 15 part 2 to finish and debugging the hell out of it, I rewrote it in Rust, copying the algorithm exactly. The Rust version finished in less than 650 ms, and I had not the slightest idea why it didn’t work in Elixir. Asking about it, I learned that the time-sink probably was concatenating linked lists, which requires traversing them to the end in absence of pointers to the last node.
* Order matters. Having used the language I know for the first few days, there were only unfamiliar ones left when exercises got mostly harder and harder. I should've used foreign languages first, saving familiar ones for harder stuff.

### Summary
I already stated above that I do not intend to do this again. The self-imposed pressure of doing each challenge the day it's released did take part of the fun out of it. I don't want to be stressed by something that's supposed to be fun. Additionally, while it indeed is great to peek into new languages, one day's exercise is neither sufficient to get a good impression nor does AoC being mostly about finding and using the right algorithm aid in learning. I still enjoy doing code challenges, and have already started catching up with older Advents. Maybe I'll use a new language for another year. But the most important part of doing all this for me is fun. Stay hungry, stay foolish, but most of all enjoy!
