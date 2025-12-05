# Propositional Logic Playground

An interactive, web-based practice environment for students in a discrete mathematics course to learn and play with the formal symbols of propositional logic.

The app focuses on engagement and exploration instead of rote drill, while still supporting core skills with logical connectives such as:

- Conjunction: `∧`
- Disjunction: `∨`
- Implication: `→`
- Negation: `¬`
- Equivalence (biconditional): `↔`

---

## What this project does

This project provides a single-page front-end web application where students can:

- Enter and edit propositional logic expressions using the standard symbols.
- Get instant feedback on syntax (valid vs. invalid formulas).
- See truth tables and evaluations for given assignments of truth values.
- Practice recognition and construction tasks in short, playful “challenges.”
- Explore logic through small game-like interactions instead of static exercises.

The app is intended as a low-friction companion to a discrete mathematics course, especially in units on propositional logic.

---

## Why this project is useful

Discrete math students often struggle to:

- Move from informal English statements to formal logical notation.
- Remember and correctly use the different connectives and their symbols.
- Develop an intuition for how expressions behave under different truth assignments.

This project addresses those issues by:

- Providing a safe environment to experiment with expressions.
- Giving non-punitive, immediate feedback (hints, highlighting, suggestions).
- Using light gamification (streaks, small challenges, random “puzzles of the day”) to increase time-on-task and engagement.

---

## Core design and interaction goals

These are especially important for implementation (for both human contributors and GitHub Copilot):

1. **Engagement and playfulness**
   - Short, self-contained challenges (for example, “Build a formula equivalent to ¬(P ∧ Q) using only ∨ and ¬”).
   - Friendly microcopy and visual feedback (success messages, subtle animations).
   - Optional “challenge mode” with simple scoring or streaks.
   - No punitive grading; emphasize exploration and learning.

2. **Clarity and accessibility**
   - Clear, readable layout that works well on desktop and tablet.
   - Keyboard-friendly input of symbols (for example, type `&` and get `∧`, type `->` and get `→`).
   - Accessible color choices; do not rely only on color to convey correctness.
   - Meaningful ARIA labels and semantic HTML for screen readers.

3. **Pedagogical focus**
   - Support both **symbol fluency** (typing/recognizing logical symbols) and **conceptual fluency** (understanding the truth-functional behavior).
   - Encourage students to test multiple interpretations and see how truth values propagate.
   - Provide brief, inline explanations for each connective on hover or click (tooltips or help panel).

---

## Features (current and planned)

### Initial feature set

- Interactive expression editor for propositional formulas.
- Support for logical operators: `∧`, `∨`, `→`, `¬`, `↔`.
- Basic parsing and validation with real-time feedback on malformed expressions.
- Truth table generation for a given well-formed formula.
- A small set of prebuilt practice tasks, such as:
  - “Translate this English sentence into a propositional formula.”
  - “Is this formula a tautology, contradiction, or contingent? Explore to decide.”
  - “Construct a formula equivalent to a given one.”

### Possible future enhancements

- Progress indicators or lightweight achievement badges.
- Randomized formula-generation for practice.
- Instructor mode to define custom exercises.
- Localization support for different languages.
- Persistence of user progress via local storage or simple backend.

---

## Tech stack

This is a **front-end–only** project intended to be hosted on **GitHub Pages (`github.io`)**.

A typical implementation can use:

- **Language:** TypeScript or JavaScript
- **Framework:** React (with Vite or similar bundler), or another modern front-end framework
- **Styling:** CSS modules, Tailwind CSS, or a simple component library
- **Build/Tooling:** Node.js-based toolchain

The implementation should:

- Be easy to run locally with a small number of commands.
- Produce a static bundle that can be deployed to GitHub Pages.

---

## Getting started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS version recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
npm install
# or
yarn
```

### Running the app locally

```bash
npm run dev
# or
yarn dev
```

Then open the indicated local URL (commonly `http://localhost:5173` or `http://localhost:3000`) in your browser.

### Building for production

```bash
npm run build
# or
yarn build
```

This produces a production build (commonly in `dist/`) that you can deploy to GitHub Pages.

---

## Deploying to GitHub Pages

There are several ways to deploy the built app to GitHub Pages. A simple approach is:

1. Configure the build so that the output directory is `docs/` instead of `dist/`, or copy the contents of `dist/` into `docs/` after building.
2. Commit and push the updated files to the default branch (for example, `main`).
3. In the repository settings on GitHub, enable **Pages** and choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/docs`

Alternatively, you can:

- Use a GitHub Actions workflow to build and deploy to a `gh-pages` branch.
- Or configure your chosen framework’s GitHub Pages deployment plugin.

When hosted, the app will be available at a URL like:

`https://<your-username>.github.io/<your-repo-name>/`

Ensure the app correctly handles this base path (for example, by setting `base` in Vite config).

---

## How to use the app

Once the app is running (locally or on GitHub Pages):

1. **Open the expression editor.**
   - Type variables such as `P`, `Q`, `R`.
   - Use keyboard shortcuts like `&`, `v`, `!`, `->`, `<->` to insert logical symbols.

2. **Check syntax and structure.**
   - As you type, the app should highlight syntax errors or mismatched parentheses.
   - Suggestions or hints may appear to guide corrections.

3. **Generate and inspect truth tables.**
   - Use the relevant control to view a truth table for the current formula.
   - Explore how changing the formula affects its truth-functional behavior.

4. **Try challenge modes.**
   - Select a challenge from the list.
   - Follow the instructions (for example, match a target truth table or translate from English).
   - Receive immediate feedback and optional hints.

---

## Project structure (example)

The exact structure may vary by implementation, but a typical organization might be:

```text
src/
  components/
    ExpressionEditor/
    TruthTable/
    ChallengePanel/
    Layout/
  logic/
    parser/
    evaluator/
    truthTable/
  data/
    sampleChallenges.ts
  styles/
  App.tsx
  main.tsx
public/
README.md
LICENSE
```

Key ideas:

- Keep parsing and evaluation logic separate from UI components.
- Make it easy to add new challenge types without restructuring the whole app.

---

## Contributing

Contributions that improve pedagogical effectiveness, accessibility, and student engagement are especially welcome.

Suggested contribution areas:

- New challenge types or exercise templates.
- Improved feedback messages and hints.
- Accessibility and usability improvements.
- Additional visualizations of logical structure.

Before opening a pull request:

1. Open an issue describing the change you propose.
2. Fork the repository and create a feature branch.
3. Ensure tests (if present) pass and your changes are documented.

See the contribution guidelines for details:

[Contribution guidelines for this project](docs/CONTRIBUTING.md)

---

## Getting help

If you encounter issues or have feature suggestions:

- Open an issue in the repository with a clear description and, if possible, screenshots.
- Tag issues as “bug,” “enhancement,” or “question” as appropriate.

---

## Maintainers

This project is maintained by the course instructor and contributors from the discrete mathematics teaching team. Contributions from the broader community are welcome, especially if they improve teaching and learning of propositional logic.

---

## License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for details.
