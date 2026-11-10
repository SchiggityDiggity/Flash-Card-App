# Flashcard App — Change Summary

## Short summary

Built a self-contained flashcard app with deck and card management, four question formats, study-mode filters, shuffled sessions, keyboard navigation, answer feedback, saved per-deck scores, and end-of-session accuracy. Decks and scores are stored locally in the browser.

## Detailed assessment

### Decks and flashcards

- Create, rename, and delete decks; select decks from the navigation list.
- Create, edit, and delete cards containing a question, answer, and optional image.
- Images are limited to 2 MB. Invalid image types, oversized files, image read/preview failures, and storage failures are reported with an on-screen notice and a console error where applicable.
- View cards in a grid or list.
- Persist decks, cards, and scores in localStorage; no backend or framework is used.

### Card formats and authoring

- New-card creation begins with a format picker that describes flashcards, multiple choice, true or false, and fill in the blank.
- After selecting a format, the editor shows the relevant fields with short instructions; existing cards can be edited or changed to another format.
- Multiple-choice cards support 2–6 distinct options and a designated correct answer.
- True-or-false cards have a selected correct response.
- Fill-in-the-blank questions require `____` or `[blank]` and accept exact answers or sufficiently close answers with explicit feedback.

### Studying and progress

- Study the entire deck using each card's saved format, or filter a study session to one format.
- Shuffle is enabled by default for a session and can be turned off to preserve deck order.
- Press Space to reveal or hide a flashcard answer; use left and right arrow keys to navigate.
- Multiple-choice, true-or-false, and fill-in-the-blank answers are graded. Flashcards can be self-rated as remembered or missed.
- Show correct and incorrect totals per deck and persist them in localStorage.
- At session completion, show accuracy and correct/incorrect counts for answers checked or self-rated; unanswered cards do not count as incorrect.

## Verification results

Browser-driven checks were run against the app in the browser. The final comprehensive run reported:

- PASS — all four card formats created and identified.
- PASS — card list/grid views toggle.
- PASS — focused study, grading, and accuracy percentage.
- PASS — all-format grading, flashcard self-rating, and cumulative scores.
- PASS — card edit, deck rename, and saved data persistence.
- PASS — unique element IDs and JavaScript syntax.
- PASS — original localStorage contents restored after testing.

Additional browser checks during implementation passed for close-answer feedback, true-or-false grading, empty-format messaging, shuffled and unshuffled order, and completion behavior when no answers were graded.
