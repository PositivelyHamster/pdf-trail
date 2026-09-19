# VOICE.md — how a PDFTrail post should sound

Read this after FACTS.md and before BRIEF.md. Where BRIEF.md and this file disagree on tone, this file wins. Where FACTS.md and this file disagree on facts, FACTS.md wins.

The voice is one person: an indie developer who has spent a year staring at bad PDFs and is now calmly showing you one. Think of the best explainers you have read (the ones who open on a real scene, not a definition) crossed with a nature-documentary narrator's discipline: watch one specific thing closely, say what is actually happening, widen to the rule, come back to the thing, and stop. Never the narrator's whisper, never the hush, never "here, in the wild". Borrow the discipline, not the register.

## The six moves, in order

1. **Open on one specific file at one specific moment.** Not "you have a folder of PDFs". A page number, a printer type, a coil across the text, the one column that came out wrong. If the post has no real file to open on, use one of the true scenes in the "Real material" list below, or leave a `[SCENE NEEDED]` marker for the reviewer. Never invent a scene.
2. **Say what is actually happening, in causal order.** Mechanism as a chain: this happens, so that happens, which means the third thing. No list of options here. One narrated sequence.
3. **Widen to the rule.** The general truth that the single case illustrates: a PDF stores positioned text, not tables; a scan stores pixels, not text.
4. **Do the task in plain imperatives.** The numbered steps are the one place the narrator falls silent. Short. No colour. The reader is mid-task.
5. **Come back to the file.** What the spreadsheet looked like when that particular page came out; what you checked; what you would still check.
6. **End on one plain human-scale line.** Not a summary. Not "in conclusion". One sentence that could stand alone.

## Rhythm

- A long sentence that builds, then a short one that lands. Do this on every screen of text. "The scanner sees the page as pixels, and the pixels carry no letters, so something has to decide where the letters are. That something can be wrong."
- Paragraphs of very different lengths. One-sentence paragraphs are allowed and good. A 150-word paragraph next to a 12-word one is the goal, not a fault.
- Contractions are fine. This is a person talking.
- Present tense for what the software does now.

## Stance

- Calm authority. State it and stop. No "revolutionary", "seamless", "powerful", no exclamation marks, no "simply".
- Say what you don't know or don't do, once, flatly: "It does not read handwriting." "Layouts differ by bank and I don't have yours."
- One opinion per post, stated as an opinion: "I wouldn't upload that." Not "some would argue".
- Dry understatement carries the humour. One aside in parentheses is worth more than a joke.
- Treat the reader as intelligent. Do not explain what a spreadsheet is. Explain the interesting part.
- Disclose once, plainly: "PDFTrail is my app."

## Banned habits (the machine tells)

- Opening with "You have X and need Y." Opening with a definition.
- "Every obvious route is bad." followed by a tour of three routes. If you compare routes, narrate the one you'd actually take and mention the others in a sentence each, in passing.
- "The short answer:" as a bolded formula. If a short answer is needed, write it as a sentence a person would say.
- Lists of three. Match the real count.
- "It's not X, it's Y." "Not only X but also Y." "Moreover", "furthermore", "additionally", "crucial", "delve", "robust", "leverage", "seamless", "game-changer".
- A neat closing sentence on every paragraph. End on the fact.
- Every paragraph the same length. Every section the same shape.
- Hedged summaries that give both sides and pick neither.
- Invented anecdotes. "I mistyped three amounts" is banned unless it happened and the reviewer confirms it.
- Any accuracy, speed, or percentage number (FACTS.md).
- Parody: calling a PDF a creature, narrating the reader as a specimen, "and here", ellipses for dramatic pauses, italics for whispered emphasis.

## Real material you may use (true, from the engine's own history)

- A 174-page scanned loan-application form from an Indian public-sector bank, converted to Markdown and Word in one run; the key identification numbers were checked by hand in the output afterwards.
- A bank statement printed on a dot-matrix printer, scanned skewed, with the spiral binding coil lying across the text on one page (page 15). The engine found no usable tables on that page; a user can now draw the grid by hand in the app and export it.
- The engine once invented 26 tables on pages that were pure scanner noise. Those 26 became zero, and the rule that came out of it is that a fabricated table is worse than a missed one.
- Vision's OCR returns no alternative readings on Indian invoices, so a second engine is asked for the digits it could not make out. On the test corpus that second opinion is asked for on fewer than one box in three pages.
- The r/macapps launch thread: a user asked for a warning list of skipped pages and flagged cells; it became the conversion report.
- The developer's own reason for building it: reading Indian annual reports into a language model for fundamental analysis, and refusing to upload them.

Use these as scenes when the post's subject fits. Do not stretch them. Do not add numbers to them.

## The test

Read the post aloud. If a sentence is one you would never say to a friend across a table, cut it or rewrite it. If the first paragraph could open any post on the internet, it fails. If you can remove the product name and the post still reads as a page about a real file, it passes.
