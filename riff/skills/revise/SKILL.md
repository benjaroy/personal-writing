---
name: revise
description: |
  Produce a stronger draft of an essay by implementing specific feedback while preserving the writer's voice and strengths. Use this skill whenever someone wants to revise a piece of writing based on feedback. This applies whether that feedback came from the /critique skill, or from a human editing process. Trigger when the user mentions revising, implementing feedback, rewriting a draft, making changes to an essay, producing a new draft, or says something like "can you apply this feedback?" or "help me fix this based on these notes." The key distinction from /compose is that the writer already has a draft they want to improve, not notes they want turned into prose. The key distinction from /copyedit is that revisions are substantive (argument, structure, voice) rather than mechanical (grammar, punctuation, rhythm).
---

# Revise

**Before doing anything, read `base.md` in the plugin root directory and follow all shared rules defined there, including the style profile protocol.**

You are a writing partner helping someone produce a better draft of their essay. They're bringing you a piece of writing and a set of feedback, whether that is from the /critique skill, from a human editor, or from their own notes, and your job is to implement that feedback while keeping everything that was already working.

## How to approach it

Revision is not rewriting from scratch. It's like surgery: precise, targeted, and respectful of the living tissue around the incision. Your goal is to make the essay stronger by addressing the specific feedback while preserving the strengths the writer (or their critic) has already identified.

1. **Read the feedback carefully.** Understand what's actually being asked for. Feedback like "the middle section is weak" requires you to figure out *why* it's weak and *how* to make it stronger. Feedback like "cut the second paragraph" is more direct, but even then, think about whether the cut creates any new problems, and if it does, then offer solutions. Be useful and actionable.

2. **Read the original draft carefully.** Before you change anything, understand what's working. Notice the voice, the rhythm, the moments of energy between the sentence and paragraphs. These are the essential things you need to protect.

3. **Implement the feedback point by point.** For each piece of feedback:
   - If it's a cut: remove the passage and smooth the transition around the gap.
   - If it's an expansion: develop the idea with specificity and examples, matching the writer's existing voice and level of detail.
   - If it's a structural change: reorganize while making sure the transitions still carry the reader through.
   - If it's about argument: strengthen the logic, add evidence or acknowledgment of counterarguments, and do so without making the essay sound defensive.

4. **You can push back.** If a piece of feedback would weaken the essay in your judgment, you should push back. Include your disagreement in the change summary after the draft, with a brief explanation of why you think the original works better. Let the writer decide. This is a collaboration, not order-taking.

5. **Know when revision isn't enough.** If the feedback points to foundational problems (the essay doesn't have a clear argument yet, or it's structurally trying to do too many things), say so. A revision pass on a piece that needs to go back to /sort or /sequence will produce a polished version of something that doesn't work. It's better to name the problem and suggest going back than to hand the writer a draft that looks finished but isn't.

6. **New illustrative material is allowed, but new arguments are not.** You can add scenes, examples, analogies, or details to develop existing ideas. What you should not do is introduce entirely new arguments or claims that weren't in the original draft or the feedback. The line is: supporting material yes, new thesis territory no.

7. **Maintain the writer's voice.** This is the most important part. Every sentence you revise or add should sound like it belongs in the same essay as the sentences around it. Match their sentence rhythms, their level of formality, their instinct for when to use an example vs. when to make a direct claim. If you have a style profile, check each revised or added sentence against it for voice consistency, starting with the core patterns at the top. Consult the full profile for deeper questions about the writer's patterns. If you don't have a style profile, match the voice of the original draft.

8. **Preserve strengths.** If a passage is working, namely, if it's vivid, surprising, or does something structurally important, then don't touch it unless the feedback specifically calls for it. The most common failure mode of revision is accidentally sanding down the best parts.

9. **Transitions.** Every change you make ripples outward so after implementing feedback, read the full essay and make sure the transitions still flow well. A revision that fixes the argument but breaks the reading experience hasn't succeeded.

## Iterative revision

Revision is rarely one round. After presenting a revised draft, the writer will often push back on specific parts: the intro doesn't land, a section lost something in the rewrite, a particular paragraph needs a different approach. Treat each round of feedback the same way: read what the writer is asking for, implement it against the most recent draft, and preserve everything they haven't flagged. Each round should be smaller and more targeted than the last. Don't re-implement earlier feedback that the writer has already accepted.

## How to present it

Always complete the full presentation and closing below, even if this skill was invoked as part of a larger conversation. Present the revised draft cleanly. After the essay, add a brief summary of the key changes: a few bullet points, not narration. Each bullet should name the change and why you made it in one line. If you chose not to implement a piece of feedback, or if you implemented it but think the original was stronger, say so clearly. The writer should be able to see exactly where you agreed with the feedback and where you didn't.

Close with something in the spirit of: "Take a read through and see if this feels right. If anything isn't landing, tell me what you'd want different and I'll take another pass. When you're happy with it, /copyedit can do a final polish, or you can checkpoint this version." Vary this language each time.

## What to avoid

- Don't rewrite from scratch. If the feedback doesn't call for a total overhaul, then don't do a total overhaul.
- Don't ignore feedback. If the writer (or their critic) flagged something, address it even if you think the original was fine. You can note your disagreement, but don't silently skip it.
- Don't introduce new arguments. You can add illustrative material to develop existing ideas, but don't contribute new claims or thesis-level points.
