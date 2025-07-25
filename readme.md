

# Jeopardy: 1 Kings 1-7 (KJV)

This is a Jeopardy-style game built with ReactJS, designed as a single-page web application. It features an interactive game board with 80 multiple-choice questions based on 1 Kings chapters 1-7 from the King James Version (KJV) Bible. The game includes a modal for answering questions, feedback on correct/incorrect answers, and visual indicators (green for correct, orange for incorrect) on the game board.

## Features
- **Interactive Game Board**: 8 categories with 5 questions each, valued at $200, $400, $600, $800, and $1000.
- **Multiple-Choice Questions**: Each question has four answer options, displayed in a modal.
- **Feedback Modal**: Shows "Correct!" or "Incorrect!" with the correct answer after selection.
- **Persistent State**: Answered questions are marked green (correct) or orange (incorrect) and cannot be reselected.
- **Responsive Design**: Built with Tailwind CSS for a clean, mobile-friendly interface.
- **Error Handling**: Displays user-friendly messages if the question data fails to load.

## Files
- `index.html`: The main application file containing the ReactJS code, Tailwind CSS, and game logic.
- `questions.json`: Contains 80 questions across 8 categories, formatted as JSON.

## Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge).
- A local web server to serve the files (e.g., Python's `http.server`, Node.js `http-server`, or VS Code Live Server).

## Setup Instructions
1. **Save the Files**:
   - Save `index.html` (from artifact ID `e2e861c4-8326-4194-9342-b27ee09a9df7`) in a directory.
   - Save `questions.json` (from artifact ID `501701ad-cabe-40d7-b6ea-fd528b36223f`) in the **same directory** as `index.html`.

2. **Run a Local Web Server**:
   - Browsers restrict `fetch` requests when opening `index.html` directly via `file://`. Use a local server to serve the files.
   - Example using Python:
     ```bash
     cd path/to/your/directory
     python -m http.server 8000
     ```
   - Alternatively, use:
     - Node.js: `npx serve` or `npx http-server`.
     - VS Code: Use the Live Server extension.
   - Open your browser and navigate to `http://localhost:8000` (or the port specified by your server).

3. **Verify File Access**:
   - Ensure `questions.json` is accessible at `http://localhost:8000/questions.json`. If it doesn't load, check the file path and server configuration.

## How to Play
1. Open `http://localhost:8000` in your browser.
2. The game board displays 8 categories with 5 questions each.
3. Click a question tile (e.g., "$200") to open a modal with the question and four answer options.
4. Select an answer:
   - If correct, the modal shows "Correct!" in green.
   - If incorrect, the modal shows "Incorrect!" in red with the correct answer.
5. Click "OK" to close the modal. The tile turns green (correct) or orange (incorrect).
6. Answered questions cannot be reselected.
7. Continue selecting questions until all are answered.

## Dependencies
- **React**: Loaded via CDN (`react@18.2.0` and `react-dom@18.2.0`).
- **Babel**: Loaded via CDN (`@babel/standalone@7.24.7`) for JSX transpilation.
- **Tailwind CSS**: Loaded via CDN for styling.

## Troubleshooting
- **"Failed to load questions" Error**:
  - Ensure `questions.json` is in the same directory as `index.html`.
  - Verify the local server is running and serving `questions.json` (check `http://localhost:8000/questions.json` in your browser).
  - Check the browser's Console (F12 > Console) for detailed errors (e.g., 404 Not Found).
- **MIME Type Mismatch**:
  - If you encounter a MIME type error for Babel, ensure the CDN URL is correct (`https://unpkg.com/@babel/standalone@7.24.7/babel.min.js`).
- **CORS Issues**:
  - If running on a remote server, ensure CORS policies allow fetching `questions.json`. For local development, a simple server like `python -m http.server` avoids CORS issues.
- **No Questions Displayed**:
  - Check the browser's Network tab (F12 > Network) to confirm `questions.json` is loading successfully.
  - Ensure the JSON file is valid and matches the expected format (see `questions.json`).

## Notes
- The game is designed to run in any modern browser without additional build steps.
- Questions are based on 1 Kings 1-7 (KJV), covering topics like King David's final days, Solomon's rise, and the Temple's construction.
- The application is a single-page app, with all logic contained in `index.html`.

For additional support, check the browser's developer tools for errors or consult the documentation for your local server setup.

