# Personal Writing

**What is this?**

Personal Writing is a plugin for Claude that offers users a toolkit to help with the process of writing essays. There are six discrete skills: Sort, Sequence, Compose, Critique, Revise, and Copy Edit. Together, they contain almost everything I know about writing. Each skill works on its own, but all the skills are also designed to work together in a chain.

**Why does this exist?**

The idea behind this plugin is pretty simple. I wanted to distill the ways I've found LLMs helpful in my personal writing process and formalize those flows into a set of skills for other people to use. I believe personal writing is still fundamentally a human act, and no tool is going to replace your personal thinking or creative spirit, but Claude is a powerful tool, and it can be very helpful with aspects of the writing process, especially when it's empowered with writing-specific instructions.

**What do the skills actually do?**

### /sort

This skill takes raw, unstructured material like notes, bullet points, or voice memos and distills all inputs into 10 or fewer core points. In that process, the goal is to preserve the writer's original language, phrasing, and quirky references while consolidating what could be a chaotic mess of content. It's useful when you have a bunch of ideas and want to clarify what you're actually yapping about.

### /sequence

This skill takes in notes on a topic, then proposes two possible structures for organizing those ideas into an essay: one structure that is more conventional and one that is more experimental. Each option includes a proposed order of points alongside reasoning for the given structure. It's useful when you know what you want to say but you haven't figured out exactly how to arrange ideas in a compelling sequence.

### /compose

This skill writes a full personal essay from structured notes in the writer's own voice. To do that, the first time this skill gets used, it asks for a writing sample to build a style profile of the user. This is then saved and reused across sessions. Before drafting the essay, this skill also asks where the piece will be published (e.g. Substack, X, an IRL magazine) as well as how long the user would like the piece to be.

### /critique

This skill gives a thorough assessment of a piece of writing. It evaluates argument quality, originality of ideas, fluff, pacing, paragraph rhythm, and vulnerability to criticism. It's designed to be direct without being too intense or mean, and outputs that use this skill also end with five simulated social media reactions to show the writer how their piece might land in public.

### /revise

This skill takes a draft piece of writing and a set of feedback (whether that's from the /critique skill or a human editor) then it produces a stronger draft. It implements feedback point by point while preserving both the writer's voice and everything that was already working about the underlying piece.

### /copy-edit

This skill does a close read of a piece of writing to check for grammar issues, punctuation errors, and sentence rhythm variance. It then presents each suggested change or edit to the user by citing the original passage, then specifying the proposed change and also giving a reason for that change. It also distinguishes between the writer's intentional style and genuine errors in its assessment.

**How do these skills work together?**

If you wanted to use every skill in this plugin in a chain, one possible workflow might look like this:

- Dictate some rough thoughts into a voice memo, then paste that into /sort
- Take those sorted points and use /sequence to explore structures for your ideas
- Pick a structure that you like and hand that to /compose to build a first draft
- Run /critique to see what's working in that draft and what isn't
- Feed that feedback into /revise which can then create a stronger second draft
- Finish with /copy-edit for a final polish

This is just one path to use these skills. My sense is people will pick and choose what to use according to their needs, and they'll likely intervene and make changes to their work manually along the way. That's how I use this stuff personally anyway.

**Installation**

Download the .plugin file from this repository, then go to the Claude desktop app. When you're there, look for the "customize" button, click that, and it should give you an option to add "personal plugins," which then should offer you an option to "upload plugin" where you can drag or upload this file. Once that's done, you'll see a preview of the plugin's contents, which you can accept with a click. Then all six skills will be available to use.

**A final note**

I cooked up this plugin because I love writing and I like the idea of helping real people write real things. I'm a big believer that way more people should publish their thoughts about the world and the things they care about in written form, and if this set of skills helps anyone do that I'll count it as a win. If you do use this, all feedback is welcome. Good luck out there.
