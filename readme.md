# Jeopardy: Bible Quiz

This is a Jeopardy-style single-page application (SPA) built with ReactJS, featuring an interactive game board with multiple-choice questions based on the King James Version (KJV) Bible. Users can select from different question sets (e.g., 1 Kings 1-7 or 1 Kings 8-14) via a dropdown, which dynamically loads the chosen question set. The game includes a modal for answering questions, feedback on correct/incorrect answers, and visual indicators (green for correct, orange for incorrect) on the game board.

## Features
- **Question Set Selection**: Choose from multiple question sets via a dropdown, each loaded dynamically from a JSON file.
- **Interactive Game Board**: 8 categories with 5 questions each, valued at $200, $400, $600, $800, and $1000.
- **Multiple-Choice Questions**: Each question has four answer options, displayed in a modal.
- **Feedback Modal**: Shows "Correct!" or "Incorrect!" with the correct answer after selection.
- **Persistent State**: Answered questions are marked green (correct) or orange (incorrect) and cannot be reselected.
- **Responsive Design**: Built with Tailwind CSS for a clean, mobile-friendly interface.
- **Error Handling**: Displays user-friendly messages if question sets or questions fail to load.

## Files
- `index.html`: The main SPA containing ReactJS code, Tailwind CSS, and game logic.
- `question_sets.json`: Lists available question sets with their file paths and titles.
- `questions_1kings1-7.json`: Question set for 1 Kings 1-7 (KJV) with 80 questions.
- `questions_1kings8-14.json`: Question set for 1 Kings 8-14 (KJV) with 80 questions.

## Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge).
- A local web server to serve the files (e.g., Python's `http.server`, Node.js `http-server`, or VS Code Live Server).

## Setup Instructions
1. **Save the Files**:
   - Save `index.html` (artifact ID `e2e861c4-8326-4194-9342-b27ee09a9df7`) in a directory.
   - Save `question_sets.json` (artifact ID `b7f3e8a2-5c4d-4f2b-9c3e-2d9f1a6b7c8e`) in the same directory.
   - Save `questions_1kings1-7.json` (artifact ID `501701ad-cabe-40d7-b6ea-fd528b36223f`) in the same directory.
   - Save `questions_1kings8-14.json` (artifact ID `c8e9f2b3-6d5e-4f3a-9d4f-3e0a2b3c4e9f`) in the same directory.

2. **Run a Local Web Server**:
   - Browsers restrict `fetch` requests when opening `index.html` directly via `file://`. Use a local server to serve the files.
   - Example using Python:
     ```bash
     cd path/to/your/directory
     python -m http.server 8000