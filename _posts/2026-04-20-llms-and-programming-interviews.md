---
layout: post
title: LLMs and programming interviews
---

The interview loops I've planned almost always involve a code review round. Reading code is much harder than writing it, and code is much more often read than it is written (changing in this era of throwaway LLM-generated scripts, but still). Some would say this is the age of agentic engineering, and we no longer need to look at code; defining outcomes is sufficient. I disagree, but that's a topic for another day. For now, let's assume we still need to look at code.

I usually create a PR that, ostensibly, came from a junior developer, and ask the candidate to review it just like they would in a production context. Then, on a call, we go through the content of their review.

It mildly scares me that at least 90% of the candidates who reach this round, more or less, use LLMs to generate a review and call it a day. _Starting_ with LLM content is fine-ish, but during the discussion phase, they generally can't go any deeper than what the LLM did for them, which suggests to me that they've abdicated the responsibility of independent thought.

For example, I always include a very simple and obvious SQL injection vulnerability; something that GPT-3 could have easily caught. As expected, all candidates flag this first, and suggest using query parameterisation.

I then ask some variant of one of the following:

* "Is the client or the server responsible for combining the query with the parameters?"
* "How come this approach isn't vulnerable to injection?"
* "How would you exfiltrate data using this vulnerability?"

These aren't meant to be gotchas, but rather to give candidates opportunities to reason from first principles. I don't expect a perfect answer, or even a strong one (how many people have ever touched compiler/database internals?), but I am looking for curiosity and an ability to generalise. After all, everything is connected.

Orthogonal to the above, but no less important, is the fact that this process is meant to help me understand how the candidate communicates - are they able to give bad feedback (at all)? Are they able to give bad feedback (tactfully)? Do they call out implicit assumptions? How do they navigate situations where their judgment may be incorrect? 

I remember this strong candidate who didn't do super well in terms of the initial review, but who participated in the discussion eagerly and intelligently. I would have loved to work with them; that ended up not happening for multiple reasons (chief among which was that I left shortly after), but it was still a wonderful interview.

Anyway, I worry about the effect LLMs have on individuals' cognitive capabilities. It would be bad if they were just slop generators, but the problem is that they now produce real value; I've personally experienced this, though, as noted above, I think it's still important to stay close to the code.

If I were reviewing _my own_ code, then, yes, I might do an LLM-based first pass. But to do that on someone else's code, and in such a way that you clearly don't read through or edit the output (as evinced by their inability to answer even simple questions)...can you really get anywhere with that?
