View upcoming puzzles

UI lists future puzzles (e.g. next 30 days) from all_puzzles_YYYY.json.

For each puzzle: show date, id, language, 4 categories (name, words, difficulty).

Edit puzzle content

Change category names.

Edit words inside a category (add/remove/swap), with validation that each category still has exactly 4 words and total 16 words.

Change difficulty per category (mapped to yellow/green/blue/purple).

Regenerate puzzle for a specific day

Button: “Regenerate this puzzle”.

Options: preserve target difficulty mix or choose a new mix (e.g. “overall easier / harder”).

When clicked, calls backend/script that:

Generates a new puzzle via the API.

Replaces that date’s entry in all_puzzles_YYYY.json.

Updates change log.

Change log

For each puzzle, store a history of edits: timestamp, action (edited words, changed difficulty, regenerated), and possibly a short note.

UI shows log per puzzle.

Publish rules

Puzzles remain editable until their date (e.g. locked at 00:00 of the puzzle’s day).

Published puzzle of the day is exported to public_today.json (scrambled, answerless) for the frontend.

Tech context

All JSON and code live in the GitHub repo (managed in VS Code).

Automation (weekly generation, regenerations triggered by UI) handled via Python + GitHub Actions or a small backend.
