# A Claude Plugin for Writing Personal Essays

**What is this?**

Benroy Writing is a plugin for Claude that offers users a toolkit to help with the process of writing essays. There are eight skills: Sort, Sequence, Compose, Critique, Revise, Copy Edit, Title, and Checkpoint. Together, they contain almost everything I know about writing. Each skill works on its own, but all the skills are also designed to work together in a chain, and each skill points you toward the next logical step when it makes sense.

**Why does this exist?**

The idea behind this plugin is pretty simple. I wanted to distill the ways I've found LLMs helpful in my personal writing process and formalize those flows into a set of skills for other people to use. I believe personal writing is still fundamentally a human act, and no tool is going to replace your personal thinking or creative spirit, but Claude is a powerful tool, and it can be very helpful with aspects of the writing process, especially when it's empowered with writing-specific instructions.

**What do the skills actually do?**

### /sort

This skill takes raw, unstructured material like notes, bullet points, or voice memos and distills all inputs into a set of core points (typically 7-10, up to 14 for denser material). It assesses the type of material you're working with behind the scenes, consolidates overlapping ideas, and preserves the writer's original language and phrasing. Anything that doesn't fit the main structure goes into a "junk drawer" so nothing gets silently dropped. When it's done, it'll nudge you toward /sequence if you want to explore how those points might become an essay.

### /sequence

This skill takes sorted points and helps you figure out how to arrange them into an essay. Before proposing structures, it asks a lightweight question about your intention — whether you're making an argument, working through something personal, telling a story, explaining a concept, or not sure yet — and checks for structural tensions in the material (like competing throughlines or tonal splits). Then it proposes one to three structural options depending on what the material supports, rather than forcing exactly two every time. When you've picked a direction, it points you toward /compose.

### /compose

This skill writes a full personal essay from structured notes in the writer's own voice. The first time it gets used, it asks for a writing sample (text, a file, or a URL to something you've published) to build a style profile. This profile is saved and reused across sessions, though publishing context and word count are asked fresh each time. It asks where the essay is going (Substack, personal blog, LinkedIn, X, or other) and uses that to calibrate tone and register. Word count options adapt based on where you're publishing — shorter ranges for LinkedIn and X, longer ranges for Substack and personal blogs, with a custom option for each. The skill watches for tonal consistency across register shifts and handles thin input gracefully rather than padding. After the draft, it points you toward /critique.

### /critique

This skill gives an honest, distilled assessment of a piece of writing in around 450 words. It opens with the single most important thing to fix, then works through remaining observations in descending order of severity. It evaluates argument quality, originality, fluff (including structural fluff at the section level), tonal consistency, and vulnerability to criticism, focusing on the 3-4 dimensions most relevant to the specific piece. It closes with three simulated social media reactions to show how the piece might land in public, then points you toward /revise if you want to act on the feedback.

### /revise

This skill takes a draft and a set of feedback (from /critique, a human editor, or the writer's own notes) and produces a stronger draft. It implements feedback point by point while preserving the writer's voice and everything that was already working. It can push back on feedback it disagrees with rather than implementing blindly, and it can add new illustrative material (scenes, examples, analogies) to develop existing ideas without introducing new arguments. When it's done, it points you toward /copy-edit for a final polish.

### /copy-edit

This skill does a close read of a piece of writing to check for grammar issues, punctuation errors, and sentence rhythm. It verifies every issue before flagging it to avoid false positives, and checks the writer's style profile before making rhythm suggestions so it doesn't flatten their voice. Each suggestion cites the original passage, states the proposed change, and gives one sentence of reasoning. When you're happy with the edits, it points you toward /title if you're ready to name the piece.

### /title

This skill helps you find the right title for a piece through deep analysis of the essay's argument, imagery, and style. It generates title ideas across three categories: two-word, three-word, and longer (up to 10 words), then iterates based on what resonates. If something catches your eye, it digs deeper in that direction. If nothing lands, it reshuffles completely and tries a different angle.

### /checkpoint

This skill lets you save, view, compare, and restore versions of your essay. When you want to preserve the current state of a draft, just say "checkpoint this" or "save this version" and it's saved. Later, you can list your saved versions, compare any two side by side (focusing on substantive changes rather than line-by-line diffs), or restore an earlier draft if a revision went sideways. The other skills will remind you that checkpointing is available, but it only saves when you ask.

**How do these skills work together?**

The skills form a natural pipeline, and each one suggests the next step when it finishes:

sort → sequence → compose → critique → revise → copy-edit → title

If you wanted to use every skill in this plugin in a chain, one possible workflow might look like this:

- Dictate some rough thoughts into a voice memo, then paste that into /sort
- Take those sorted points and use /sequence to explore structures for your ideas
- Pick a structure that you like and hand that to /compose to build a first draft
- Run /critique to see what's working in that draft and what isn't
- Feed that feedback into /revise which can then create a stronger second draft
- Finish with /copy-edit for a final polish
- Use /title whenever you're ready to name the piece
- Use /checkpoint at any point to compare versions or go back

This is just one path to use these skills. My sense is people will pick and choose what to use according to their needs, and they'll likely intervene and make changes to their work manually along the way. That's how I use this stuff personally anyway.

**What's shared across skills?**

All skills inherit from a shared `base.md` file that defines common rules: the style profile protocol, em-dash avoidance, and a checkpoint system that saves versioned drafts whenever you ask. It also includes an anti-AI voice guide, which is a list of specific words, structural habits, and tonal patterns that make writing sound machine-generated. The plugin avoids all of them, so the output reads like a person wrote it.

**Installation**

Copy the URL of this GitHub repository, then open the Claude desktop app and click "Customize." Under "Personal plugins," click the "+" button, then select "Add marketplace" and paste the URL. Once it syncs, you'll see the Benroy Writing plugin available to install. Click install. Once it's installed, the eight skills activate automatically based on what you say in your chat sessions, so just describe what you need help with and the right skill will kick in for Claude to use. You don't need to memorize anything (though you can also call these skills directly by using their slash commands).

**A final note**

I cooked up this plugin because I love writing and I like the idea of helping real people write real things. I'm a big believer that way more people should publish their thoughts about the world and the things they care about in written form, and if this set of skills helps anyone do that I'll count it as a win. If you do use this, all feedback is welcome. Good luck out there.
