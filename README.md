# Riff: A Claude Plugin for Writing Personal Essays

**What is this?**

This plugin is a toolkit to help people with the process of writing personal essays in collaboration with Claude. There are nine skills that are part of it: Sort, Sequence, Compose, Critique, Revise, Copyedit, Title, Checkpoint, and Riff. Together, they contain almost everything I know about writing in general, framed specifically to make writing with an LLM more intuitive through different steps. Each skill works on its own, though seven of the nine skills are also designed to work together in a chain.

**Why does this exist?**

The idea behind this plugin is pretty simple. I wanted to distill the ways I've found LLMs helpful in my personal writing process over the years, and formalize those flows into a set of skills for myself, then open-source everything for other people to use.

**What do the skills actually do?**

### /sort

This skill takes unstructured material like notes, bullet points, or voice memos and distills that into a set of core points. It assesses the type of material you're working with, consolidates overlapping ideas, and preserves your original language and phrasing. Anything that doesn't fit the main structure goes into a "junk drawer" so nothing gets dropped. When it's done, it'll nudge you toward /sequence if you want to explore how those points might evolve into an essay, or suggest you take time to think about the sorted points first if the underlying material is complex.

### /sequence

This skill takes sorted points and helps you figure out how to arrange them into an essay. Before proposing structures, it asks what's driving you to write i.e. whether you want to make an argument, tell a story, explain something, or aren't sure yet. If it detects a genuine structural tension in the material (like competing throughlines), it'll ask a follow up to help you choose a direction. Then it proposes one to three structural options depending on what the material supports. When you've picked a direction, it points you toward /compose.

### /compose

This skill writes a full personal essay from structured notes in your voice. If you don't have a style profile yet, it asks for a writing sample to build one (you can upload a file, share a link, or paste text directly). This profile is saved and reused across sessions. It then asks where the essay will be published (Substack, LinkedIn, X, or other) and how long it should be, and those answers are used to calibrate tone and length. After the draft is written, this skill will either suggest sitting with what you've got or it will point you toward /critique for an honest assessment.

### /critique

This skill gives an honest assessment of a piece of writing. It opens with the single most important thing to fix, then works through remaining observations in descending order of severity. It evaluates originality, argument quality, fluff, tone, and vulnerability to criticism, focusing on the dimensions that are most relevant to your specific piece. It closes with three simulated social media reactions to show how the piece might land in public. The skill will direct you from here as it sees fit, either to the next step with /revise, or if the feedback points to structural problems, it'll suggest going back to /sort or /sequence rather than pushing forward.

### /revise

This skill takes a draft and a set of feedback and produces a stronger draft. It implements feedback point by point while preserving your voice and everything that was already working in the underlying essay. It can push back on feedback it disagrees with rather than blindly implementing everything, and it surfaces those disagreements clearly in its change summary. If the feedback reveals foundational problems, it'll say so and recommend stepping back in the pipeline rather than polishing something that isn't ready. When it's done, it asks whether you'd like to move to /copyedit for a final polish, take another revision pass, or step away and read the draft on your own first.

### /copyedit

This skill does a close read of a piece of writing to check for grammar issues, punctuation errors, and sentence rhythm. If the piece still needs structural work, it'll say so and point you toward other skills for continued iteration. It verifies every issue before flagging it to avoid false positives, and if you have a style profile, it reads that first so it doesn't flatten your voice. Each suggestion cites an existing section, states its proposed change to that section, and gives one sentence of reasoning for that change. It can implement whatever changes you like, then when you're happy with the edits, it points you toward /title to help name the piece.

### /title

This skill helps you find the right title for a piece through deep analysis of the essay's argument, imagery, and style. It generates title ideas across three categories: two-word, three-word, and longer (up to 10 words), then iterates based on what resonates with you. If something is vibenomically aligned, it digs deeper in that direction. If nothing lands, it reshuffles completely and tries a different angle.

### /checkpoint

This skill lets you save, view, and restore versions of your essay as you work with Claude. When you want to preserve the current state of a draft, just say "checkpoint this" or "save this version" and it gets saved to a `checkpoints/` folder alongside your other files, so you can continue experimenting without losing progress. You can browse your saved versions anytime, or restore an earlier draft if a revision went sideways. The other skills will sometimes remind you that checkpointing is available, but it only saves when you ask.

### /riff

This skill is for getting unstuck. Call on it at any point in the process and it'll give you a quick, honest read on where things stand with a few practical observations and a nudge toward what to do next. The /riff skill also acts as a fallback in the event other skills aren't triggered.

**How do these skills work together?**

Seven of the skills form a natural pipeline: sort → sequence → compose → critique → revise → copyedit → title. Each one suggests the next step when it finishes, though you can jump in anywhere or use them independently. That said, at key moments, the plugin will also encourage you to step away and sit with your work before moving on. Checkpoint and riff can be used at any time throughout the process.

**How does it handle voice?**

The plugin uses a style profile to capture how you write. The first time you use /compose or /revise without a profile, it asks for a writing sample. It analyzes your sample for patterns like sentence rhythm, formality, humor, and how you handle transitions, then saves a profile that compose, revise, and copyedit can reference going forward. You can skip this step and write without a profile, or update it anytime with new samples. The other six skills (sort, sequence, critique, title, checkpoint, and riff) don't need a style profile and work immediately.

**Installation**

Copy the URL of this GitHub repository, then open the Claude desktop app and move to the "Cowork" section. On the lefthand side, click "Customize." Under "Personal plugins," click the "+" button, then select "Create plugin" followed by "Add marketplace" and paste the URL. Once it syncs, you'll see the Riff plugin available to install. Click install. Once it's installed, the nine skills activate automatically based on what you say in your prompting sessions. You don't need to memorize anything, though you can also call these skills directly by using their slash commands or by referencing the skill name directly in a prompt.

**A final note**

I made this plugin because I'm a big believer that more people should publish their thoughts and ideas about the world in written form, and if this set of skills helps anyone do that I'll count it as a win. My sense is going forward human writing will leverage AI consistently for certain things, but the writing process will always be a human-led activity, and this plugin is built to help facilitate that collaborative dance. In closing, I will say that this is experimental and I update it often, so if you do mess around with it, all feedback is very welcome. Just submit a GitHub Issue or send me a message on X. Good luck out there and happy riffing.
