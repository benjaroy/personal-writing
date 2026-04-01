# Personal Writing

**What is this?**

Personal Writing is a plugin for Claude that offers users a toolkit to help with the process of writing essays. There are seven skills: Sort, Sequence, Compose, Critique, Revise, Copy Edit, and Title. Together, they contain almost everything I know about writing. Each skill works on its own, but all the skills are also designed to work together in a chain.

**Why does this exist?**

The idea behind this plugin is pretty simple. I wanted to distill the ways I've found LLMs helpful in my personal writing process and formalize those flows into a set of skills for other people to use. I believe personal writing is still fundamentally a human act, and no tool is going to replace your personal thinking or creative spirit, but Claude is a powerful tool, and it can be very helpful with aspects of the writing process, especially when it's empowered with writing-specific instructions.

**What do the skills actually do?**

### /sort

This skill takes raw, unstructured material like notes, bullet points, or voice memos and distills all inputs into a set of core points (typically 7-10, up to 14 for denser material). It assesses the type of material you're working with behind the scenes, consolidates overlapping ideas, and preserves the writer's original language and phrasing. Anything that doesn't fit the main structure goes into a "junk drawer" so nothing gets silently dropped. It's useful when you have a bunch of ideas and want to clarify what you're actually yapping about.

### /sequence

This skill takes sorted points and helps you figure out how to arrange them into an essay. Before proposing structures, it asks a lightweight question about your intention and checks for structural tensions in the material (like competing throughlines or tonal splits). Then it proposes one to three structural options depending on what the material supports, rather than forcing exactly two every time. It's useful when you know what you want to say but haven't figured out how to arrange it.

### /compose

This skill writes a full personal essay from structured notes in the writer's own voice. The first time it gets used, it asks for a writing sample (text, a file, or a URL to something you've published) to build a style profile. This profile is saved and reused across sessions, though publishing context and word count are asked fresh each time. Word count options are roughly 800, 1,200, or 1,600 words, with a custom option. The skill also watches for tonal consistency across register shifts and handles thin input gracefully rather than padding.

### /critique

This skill gives an honest, distilled assessment of a piece of writing in around 450 words. It opens with the single most important thing to fix, then works through remaining observations in descending order of severity. It evaluates argument quality, originality, fluff (including structural fluff at the section level), tonal consistency, and vulnerability to criticism, focusing on the 3-4 dimensions most relevant to the specific piece. It closes with three simulated social media reactions to show how the piece might land in public.

### /revise

This skill takes a draft and a set of feedback (from /critique, a human editor, or the writer's own notes) and produces a stronger draft. It implements feedback point by point while preserving the writer's voice and everything that was already working. It can push back on feedback it disagrees with rather than implementing blindly, and it can add new illustrative material (scenes, examples, analogies) to develop existing ideas without introducing new arguments.

### /copy-edit

This skill does a close read of a piece of writing to check for grammar issues, punctuation errors, and sentence rhythm. It verifies every issue before flagging it to avoid false positives, and checks the writer's style profile before making rhythm suggestions so it doesn't flatten their voice. Each suggestion cites the original passage, states the proposed change, and gives one sentence of reasoning.

### /title

This skill helps you find the right title for a piece through deep analysis of the essay's argument, imagery, and style. It generates title ideas across three categories: two-word, three-word, and longer (up to 10 words), then iterates based on what resonates. If something catches your eye, it digs deeper in that direction. If nothing lands, it reshuffles completely and tries a different angle.

**How do these skills work together?**

If you wanted to use every skill in this plugin in a chain, one possible workflow might look like this:

- Dictate some rough thoughts into a voice memo, then paste that into /sort
- Take those sorted points and use /sequence to explore structures for your ideas
- Pick a structure that you like and hand that to /compose to build a first draft
- Run /critique to see what's working in that draft and what isn't
- Feed that feedback into /revise which can then create a stronger second draft
- Finish with /copy-edit for a final polish
- Use /title whenever you're ready to name the piece

This is just one path to use these skills. My sense is people will pick and choose what to use according to their needs, and they'll likely intervene and make changes to their work manually along the way. That's how I use this stuff personally anyway.

**Installation**

Copy the URL of this GitHub repository, then open the Claude desktop app and click "Customize." Under "Personal plugins," click the "+" button, then select "Add marketplace" and paste the URL. Once it syncs, you'll see the Personal Writing plugin available to install. Click install. Once it's installed, the seven skills activate automatically based on what you say in your chat sessions, so just describe what you need help with and the right skill will kick in for Claude to use. You don't need to memorize anything (though you can also call these skills directly by using their slash commands).

**A final note**

I cooked up this plugin because I love writing and I like the idea of helping real people write real things. I'm a big believer that way more people should publish their thoughts about the world and the things they care about in written form, and if this set of skills helps anyone do that I'll count it as a win. If you do use this, all feedback is welcome. Good luck out there.
