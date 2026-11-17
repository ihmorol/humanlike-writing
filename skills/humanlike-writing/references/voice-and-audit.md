# Voice calibration, self-audit, and extra patterns

Read this when the user supplies a writing sample, when a rewrite is longer than a few sentences, or when the draft is "clean" but still reads flat. Several ideas here are adapted from [blader/humanizer](https://github.com/blader/humanizer) (MIT) and common editorial practice.

## Voice calibration from a sample

When the user gives a sample of their own writing (inline or as a file), read it before editing and note:

- Sentence length habits: short and clipped, long and winding, or mixed.
- Register: casual, academic, technical, somewhere between.
- How paragraphs open: straight into the point, or context first.
- Punctuation habits: parentheses, semicolons, dashes, exclamation marks.
- Recurring phrases, verbal tics, and preferred plain words ("stuff", "thing", "basically").
- Transitions: explicit connectors, or just starting the next point.

Then match it. Removing AI patterns is not enough; replace them with the writer's own patterns. If they write short sentences, don't hand back long ones. If they say "stuff", don't upgrade it to "elements". If the sample uses dashes, the writer's own dashes may stay in their rewrite; the no-em-dash rule applies to prose you author in your own voice.

Never invent biography, experiences, or opinions for the writer. Calibration copies style, not facts.

## Clean but soulless

A draft can pass every pattern check and still read like a press release. Signs:

- Every sentence has the same length and shape.
- Pure neutral reporting where the reader wanted a view.
- Pros and cons perfectly balanced when the evidence is not balanced.
- No first person where first person fits the context.
- No concrete detail a reader could picture or check.

Repairs, within the facts you actually have:

- State the judgment the evidence supports ("I'd pick B; A's migration cost is the problem").
- Admit real mixed signals plainly ("It's faster, but the setup is annoying") instead of a symmetric pros/cons block.
- Use the specific detail already in the source rather than a summary of it.
- Let structure be a little uneven when the content is uneven. A tangent that matters can stay.

Do not fake feeling. "I keep coming back to this" is only acceptable when it's true of the author whose voice you are writing.

## Self-audit pass

For any rewrite longer than a short paragraph, do a second pass before returning:

1. Write the draft.
2. Ask yourself: "What still makes this read as machine-written?" List the remaining tells briefly (to yourself unless the user asked for an audit).
3. Fix those tells. Re-check facts and protected spans afterwards.
4. Read it as if aloud. Anything you would not say out loud to the intended reader gets rewritten or cut.

Show the draft, the tell list, and the final version only when the user asks for an audit or change report. By default return just the final text.

## Extra patterns

These supplement the 144 entries in [pattern-catalog.md](pattern-catalog.md). IDs use the `HV` prefix.

| ID | Pattern | Rule | Example | Repair |
|---|---|---|---|---|
| HV-01 | Stock openers | Drop throat-clearing openers that announce rather than say. | "Let's dive in." / "Here's the thing:" / "Great question!" | Start with the first real sentence. |
| HV-02 | "It's worth noting" family | Remove "it's worth noting", "it's important to remember", "notably" when they only flag the next clause. | "It's worth noting that the API is rate-limited." | "The API is rate-limited." |
| HV-03 | Hype labels | Cut "game-changer", "next-level", "unlock", "supercharge", "elevate" unless quoting. | "This feature is a game-changer for teams." | Say what the feature changes and for whom. |
| HV-04 | Curly quotes in plain-text contexts | Use straight quotes in code, commit messages, Markdown source, and terminals unless the house style uses typographic quotes. | `He said “run it”` in a README | `He said "run it"` |
| HV-05 | Title Case Headings | Use sentence case for headings unless a style guide says otherwise. | "## Best Practices For Error Handling" | "## Error handling" |
| HV-06 | Symmetric both-sides framing | Don't present "on one hand / on the other" as equal when the evidence favors one side. | "Both approaches have their merits." | Say which is better for this case and why. |
| HV-07 | Uniform paragraph openers | Avoid starting consecutive paragraphs with the same connective or shape ("Additionally,", "In addition,", "Another key..."). | Three paragraphs each opening "Additionally," | Open with the subject of each paragraph. |
| HV-08 | Overpolished closer | Drop the neat final line that restates the point with a flourish. | "In the end, it's all about finding the right balance." | End on the last concrete fact or decision. |
| HV-09 | Sanded-off voice | Don't strip a writer's slang, humor, or quirks while "cleaning" their draft. | Writer's "this thing is a mess" becomes "this component presents challenges". | Keep "this thing is a mess" if the register allows it. |
