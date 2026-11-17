# T4: Kept-as-is (Humanize mode)

## Purpose

Text that already reads clean gets no forced edits. The skill states that the text is already clear, or returns it with minimal changes only.

## Mode

Humanize 80% (default).

## Input

> The app saves the file. It writes the file to disk. It shows a message when the save ends.

## Expected behavior

- The skill does not invent edits. It keeps each fact and adds nothing.
- The skill may state that the text is already clear.
- If it returns a rewrite, the rewrite keeps all three facts and adds no sentence.

## Pass criteria

- All three facts appear in the output: app saves the file, writes it to disk, shows a message when the save ends.
- No new fact, example, or warning appears.
- The output adds no word-count line. Counts come from the checker, never from the model.
