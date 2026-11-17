# Pass 1: AI tells in full

These entries expand the compact tables in SKILL.md. The order follows blader/humanizer. *Weak alone* means: act only when other tells stand near it.

## A. Staging instead of stating

These are the strongest and most frequent tells. Act on one sighting.

### §1. Not X but Y

**Watch for:** not X but Y; not just, not only, not merely X, but Y; it is not X, it is Y; X rather than Y; the same contrast across two sentences ("This does not mean X. It means Y."); a clipped negative tail ("..., no guessing"). Each language has this formula. Treat it the same way.
**Problem:** The negative half names something nobody claimed, so the positive half sounds bigger. It adds weight but no claim. State the point. Keep a contrast only if the reader really believes the X half, or if both halves carry information.
**Before:**
> It is not just a cache, it is a new way to think about speed.
**After:**
> The cache stores repeat answers, so repeat requests take milliseconds.
**Before (split across sentences):**
> This does not mean backups are optional. It means the checker finds the easy errors first.
**After:**
> The checker finds the easy errors before the backups run.

### §2. One-line closers and dramatic fragments

**Watch for:** a one-sentence paragraph that repeats the paragraph before it; "That is the real win."; "That distinction matters."; "Let that sink in."; "Read that again."; the same closer after several sections; a sentence that names what an example just showed ("This shows the importance of..."); a row of fragments ("No setup. No config. No waiting."); one word in ALL CAPS or with periods (every. single. day.).
**Problem:** The line asks the reader to pause on a claim instead of adding to it. A short sentence is fine when it carries a new fact. Cut a closer that repeats. Merge a row of fragments into one sentence with a real claim.
**Before:**
> We moved the queue to a worker. Jobs finish in seconds. No waiting. No timeouts. No lost jobs.
>
> That is the power of the queue.
**After:**
> We moved the queue to a worker. Jobs finish in seconds now. Timeouts and lost jobs stopped.
**Before (repeated closer):**
> Caching cuts repeat work. That is the real win.
>
> Retries hide short outages. That is the real win.
**After:**
> Caching cuts repeat work. Retries hide short outages.

### §3. Sayings that sound deep

**Watch for:** the real question is, at its core, in reality, what really matters, fundamentally, the deeper issue, the heart of the matter, X is the Y of Z, X becomes a trap, not a tool but a mirror, the language of, the currency of, the architecture of
**Problem:** An ordinary point wears the dress of a hidden truth. The dressing adds no detail. Replace the saying with the specific claim.
**Before:**
> At its core, good logging is the language of trust between teams.
**After:**
> One shared log lets the night shift see what the day shift saw.

### §4. Staged run-up before the point

**Watch for:** Let us dive in, let us explore, let us break this down, here is what you need to know, now let us look at, without further ado, heads up, quick note, Honestly?, Look, Here is the thing, The thing is, Let us be honest, Real talk
**Problem:** The writer announces the point instead of making it. Remove the run-up. "Honestly" inside a casual sentence is normal. The tell is the stand-alone opener before a routine claim.
**Before:**
> Let us dive into how retries work. Here is what you need to know.
**After:**
> The client tries three times. Then it returns an error.
**Before (staged candor):**
> Is the paid plan worth it? Honestly? It depends on your team size.
**After:**
> The paid plan pays off for teams of more than five people.

### §5. Arguing with no one

**Watch for:** This is not (mainly) about, I am not saying, To be clear, Do not get me wrong, This is not to say, Some might say... but, A tempting approach would be, One might be tempted to, You might think... but, It would be easy to just
**Problem:** The text answers an objection or rejects an option that appears nowhere else. Usually it is left over from a draft. Remove the defense. If it holds a real claim, state the claim. Keep an objection that someone in the context really made.
**Before:**
> To be clear, I am not saying the old design was bad. We kept the login flow and changed the dashboard first.
**After:**
> We kept the login flow and changed the dashboard first.

## B. Rhythm by rule

Shapes and punctuation used everywhere, whether the meaning needs them or not.

### §6. Forced triads

**Problem:** Ideas come in threes to sound complete. It can be one phrase ("fast, reliable, and scalable"), three parallel examples, or three short facts and a lesson. Check that each item adds a distinct idea. Keep three only when the meaning has three parts. Two or four is fine. If the list is itself a claim in the source (stated values, named features), keep its content in plainer form. Cutting it drops a fact.
**Before:**
> The new search is fast, accurate, and simple. It brings speed, clarity, and confidence to daily work.
**After:**
> The new search returns results in under a second and shows the match in the title.
**Before (paragraph scale):**
> A backup can look fine and fail. A test can pass and hide a bug. A log can be clean and lie. Production rarely explains itself.
**After:**
> A backup can look fine and still fail, and a clean test or log can hide a bug. Production rarely explains itself.

### §7. Repeated sentence openings

**Problem:** Several sentences in a row start with the same subject because repetition runs by rule, not by ear. Merge sentences, change the subject, or start with the action. Do not ban the word. Writers also repeat an opening on purpose for rhythm. *Weak alone.*
**Before:**
> It opens the file. It reads the header. It writes the index.
**After:**
> It opens the file, reads the header, and writes the index.

### §8. Dashes as the universal connector

**Rule:** The final text has no em dashes or en dashes, unless the writer's sample uses them. Then match the sample's rate. Replace each dash with a period, comma, colon, or parentheses, or rewrite the sentence. This includes spaced dashes and ` -- `. Leave dashes in code, commands, paths, and URLs alone.
**Problem:** A dash lets the writer skip the choice of how two clauses relate, so models use it everywhere. Many editors use dashes too, so one dash is *weak alone*. A text full of them is not.
**Before:**
> The release — which took four weeks — is ready. The old build -- at last -- is gone.
**After:**
> The release took four weeks and is ready. The old build is gone.

### §9. Stacked qualifiers

**Watch for:** to be fair, it is also possible, could potentially, might arguably, in some cases it may, this is an inference
**Problem:** Edit after edit adds qualifiers until each claim sounds unsure. Usually they repair an overstatement, not real doubt. Keep one qualifier when the source supports it. Keep scope statements, legal and safety notes, and real corrections. A single "perhaps" or "tends to" is human, not a tell. *Weak alone.* See also S9.
**Before:**
> This change could potentially cause problems in some edge cases.
**After:**
> This change can break imports with empty file names.

### §10. Hyphenated pairs everywhere

**Watch for:** high-quality, well-known, well-documented, long-term, real-time, client-facing after the noun they describe
**Problem:** Compound modifiers keep their hyphen in each position. Keep it before the noun ("a well-documented API") and drop it after ("the API is well documented"). Words that always take a hyphen (third-party, cross-platform) keep it. *Weak alone.*
**Before:**
> The guide is well-written and the support is long-term.
**After:**
> The guide is well written and the support is long term.

### §11. Passive voice and missing subjects

**Problem:** The text hides who acts, or drops the subject. Name the actor when it makes the action clearer. *Weak alone.* In Pass 2 this is a full rule (S6).
**Before:**
> No setup needed. Your files are backed up each night.
**After:**
> You need no setup. The app backs up your files each night.

## C. Inflation and borrowed authority

The fact underneath is usually sound. Keep it and remove the dressing.

### §12. Overused AI words

**Watch for:** actually, additionally, align with, bolstered, crucial, deep dive, delve, enduring, enhance, garner, gate/gated (figurative), highlight (verb), interplay, intricate, key (adjective), landscape (abstract), leverage, meticulous, pivotal, quietly, robust (figurative), seamless, showcase, tapestry, testament, underscore (verb), utilize, valuable, vibrant
**Problem:** Models use these words far more often than people, especially in groups. They are tells wherever they appear. A formal word outside this list is not a tell by itself. STE gives the plain swap: see `references/word-swaps.md`.
**Before:**
> Additionally, the platform leverages a robust engine, showcasing a meticulous approach to data.
**After:**
> The platform also stores each record twice, so a disk failure loses nothing.

### §13. Inflated significance

**Watch for:** stands as a testament, a pivotal or crucial moment, plays a key role, marking or shaping the, underscores its importance, reflects a broader, lasting legacy, setting the stage for, evolving landscape, indelible mark; "Despite these challenges... continues to thrive"; sections called "Challenges and Legacy" or "Future Outlook"; the future looks bright, exciting times ahead
**Problem:** An ordinary detail is said to mark a change, prove a legacy, or promise a future. It shows up as a phrase, a stock "challenges and outlook" section, or a send-off paragraph. Keep the fact. End on the last concrete fact.
**Before:**
> Version 3.0 marks a pivotal moment in the history of the project, and the future looks bright.
**After:**
> Version 3.0 adds offline mode and drops Python 3.8.
**Before (send-off):**
> The future looks bright for the project. Exciting times lie ahead!
**After:**
> (Cut the paragraph. End on the last concrete fact.)

### §14. Vague connection or association

**Watch for:** associated with, in association with, connected to, in connection with, linked to, tied to
**Problem:** The text says two things are connected but not how. "She is associated with the project" hides whether she founded it, maintains it, or once filed a bug. Name the relation the source gives. If the source does not say, keep the vague words. Do not invent a role.
**Before:**
> The outage was linked to the deploy, and the author is associated with the core team.
**After:**
> The deploy caused the outage. The author maintains the core package.

### §15. Shallow -ing riders

**Watch for:** highlighting, underscoring, emphasizing, ensuring, reflecting, symbolizing, contributing to, cultivating, fostering, encompassing, showcasing
**Problem:** An -ing phrase is bolted onto a simple fact to make it sound deeper. Keep the fact. Keep the rider only if the source supports its claim. STE agrees: no "-ing" verb forms as riders (S8).
**Before:**
> The team shipped the new editor in June, highlighting its focus on speed and fostering a better workflow.
**After:**
> The team shipped the new editor in June.

### §16. Sales language

**Watch for:** rich (figurative), profound, exemplifies, commitment to, nestled, in the heart of, groundbreaking, renowned, featuring, diverse array, breathtaking, must-try, stunning, world-class, cutting-edge, best-in-class
**Problem:** The text reads like an ad. State what the thing is and what it does.
**Before:**
> Nestled in the heart of the cloud, our groundbreaking platform offers a world-class experience.
**After:**
> The platform runs in the cloud and stores files in three regions.

### §17. Borrowed authority

**Watch for:** experts argue, observers have noted, industry reports, some critics, several publications; featured in [list of outlets]; over N followers
**Problem:** A name or an unnamed authority stands in for what was said. If the source names who said what, use that. Otherwise cut the claim or the list. A missing citation alone is not a tell. Never invent a source.
**Before:**
> Experts agree that this stack is the future. The tool was featured in TechCrunch, Wired, and The Verge.
**After:**
> The tool is written in Go. It reached the front page of Hacker News in April.

### §18. Avoiding is, are and has

**Watch for:** serves as, stands as, functions as, operates as, marks, represents [a]; boasts, features, offers, maintains [a]; refers to
**Problem:** Simple verbs become longer phrases. Use *is*, *are* and *has*.
**Before:**
> The settings page serves as the central hub for options and boasts 30 toggles.
**After:**
> The settings page holds the options. It has 30 toggles.

## D. Formatting by rule

Templates also produce clean formatting. The tell is decoration on each item.

### §19. Bold as decoration

**Problem:** Words are bold for no reason, and each list item has a bold label and a colon. Remove the bold. Turn a labeled list into prose when the labels add nothing. Keep bold for warnings, UI labels, and terms the reader must find again.
**Before:**
> - **Speed:** Speed improved a lot.
> - **Safety:** Safety improved with new checks.
**After:**
> Pages load faster, and new checks block bad input before it saves.

### §20. Decorative headings

**Problem:** Headings Capitalize Each Word, carry emoji or arrows, and a rule separates each section. A heading written for effect ("The decision, on one screen") should name what the section holds ("How the options compare"). Use sentence case. Remove the decoration. A five-sentence answer does not need three headings.
**Before:**
> ## 🚀 Start Fast With The Tool →
**After:**
> ## Install the tool

### §21. Curly quotation marks

**Problem:** Curly quotes (“...”) appear where the format uses straight quotes ("..."). Most editors curl quotes automatically, so this is *weak alone*. In Markdown and code, use straight quotes.
**Before:**
> Set the value to “true” in “settings.yaml”.
**After:**
> Set the value to "true" in `settings.yaml`.

## E. Leftovers from the chat and the draft

Remove these outright. Nothing here needs rewriting.

### §22. Chatbot residue

**Watch for:** I hope this helps, Of course!, Certainly!, Great question!, You are absolutely right, Would you like..., Want me to...?, Should I continue?, let me know, here is a...
**Problem:** A chatbot's greeting, praise, offer, or sign-off stays in text that should stand alone. It is the most certain tell and the easiest to miss when it wraps real content. Remove the wrapper. Keep the content.
**Before:**
> Great question! Here is how tokens work. A token has two parts: a key and a value. I hope this helps! Let me know if you want more.
**After:**
> A token has two parts: a key and a value.

### §23. Knowledge-limit disclaimers and guesses

**Watch for:** as of [date], up to my last training update, while specific details are limited, based on available information, not publicly available, not widely documented, maintains a low profile, likely [grew up, began], it is believed that
**Problem:** The text says where the model's knowledge ends, or admits it found no source and then fills the gap with a guess. State what the source does not show, or cut the sentence.
**Before:**
> While details are limited, the tool was likely built in 2021 to fix slow deploys.
**After:**
> The sources do not say when the tool was built.

### §24. A heading repeated in the first sentence

**Problem:** A heading is followed by a one-line paragraph that repeats it. Remove that line.
**Before:**
> ## Backups
>
> Backups are important.
>
> The server copies data each night.
**After:**
> ## Backups
>
> The server copies data each night.

### §25. Writing about the document instead of its subject

**Watch for:** what the text replaced ("was added to replace"); how it was made ("generated from", "compiled from", "anything unconfirmed is flagged"); a layout the reader can see ("the table below compares", "this section is organized by")
**Problem:** The text describes itself instead of its subject. Mention an old version only in change logs and migration guides. Keep a source credit the reader can follow. Cut the story of how you worked. A single description of the page is *weak alone*.
**Before:**
> This page was added to replace the old guide, which covered the same steps in more detail.
**After:**
> This page lists the steps to install the tool.

## F. Writing for the wrong reader

A model writes for a reader with no context. A reply in a thread has a reader who already knows the background. Act on this tell only when you can see the conversation or the text is plainly a reply.

### §26. Re-explaining what the reader knows

**Watch for:** a short reply that repeats the problem, walks through the diagnosis, and shows the evidence before it reaches the decision; numbers or commands included to prove a plan works; background the other person wrote; the answer in the last line.
**Problem:** The reader already has the context, so rebuilding it buries the point. Each sentence can read fine alone, so this tell survives a sentence-level cleanup. Lead with the decision. Keep only what could change the reader's mind, usually one fact they lack and any link they need.
**Before:**
> Yes, you are right that the build fails on Fridays. I checked the logs: the job runs at midnight, and on Friday the date rolls to the next week, which breaks the tag. I tested it twice. So we should move the job to 2 a.m.
**After:**
> Agreed. I will move the job to 2 a.m. The midnight run breaks the tag on Fridays.
