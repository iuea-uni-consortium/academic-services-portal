# Contributing to the Academic Services Portal

Thank you for contributing! These rules keep the code reliable while several
teams work in parallel. Please read them before opening your first pull request.

## 1. Who works on what

| Team | Role | Owns |
|---|---|---|
| `maintainers` | Admin | `UniversityPortal.java`, `DashboardPanel.java`, `.github/`, releases |
| `registration-results-team` | Write | `CourseRegistrationPanel.java`, `ExamResultsPanel.java` |
| `fees-hostel-team` | Write | `FeePaymentPanel.java`, `HostelPanel.java` |
| `library-team` | Write | `LibraryPanel.java` |
| `stakeholders` | Read | View code, open issues, comment (no pushing) |

Each service screen lives in its **own file**. Work inside your team's files.
If you must change another team's file, ask them first and tag them as a reviewer.

## 2. Branching

- `main` is **protected**. Nobody pushes to it directly.
- Create a branch from an up-to-date `main` for every change:
  - `feature/<module>-<short-description>` e.g. `feature/fees-add-amount-validation`
  - `fix/<module>-<short-description>` e.g. `fix/library-borrow-crash`
  - `docs/<short-description>` e.g. `docs/update-readme`

## 3. Commit messages

- Start with a verb in the imperative mood: `Add`, `Fix`, `Update`, `Remove`.
- Keep the first line under 72 characters.
- One logical change per commit.
- Good: `Add amount validation to fee payment form`
- Bad: `changes`, `fixed stuff`, `asdf`

## 4. Pull request process

1. Push your branch and open a pull request into `main`.
2. Fill in the pull request template completely.
3. The **Build** check must pass (the project must compile).
4. At least **1 approving review** is required, including approval from a
   **code owner** of every file you changed (see `.github/CODEOWNERS`).
5. You cannot approve your own pull request.
6. Resolve every review conversation, then merge using **Squash and merge**.
7. Delete your branch after merging.

## 5. Code quality standards

- Follow Java naming conventions: `PascalCase` classes, `camelCase` methods and
  variables, `UPPER_CASE` constants.
- Keep every service screen in its own class and file; do not put several
  screens in one file.
- No hard-coded personal data, passwords or file paths on your own computer.
- Build and change Swing components on the Event Dispatch Thread.
- Add a short comment above each class and any non-obvious logic.
- Remove unused code and `System.out.println` debugging before opening a PR.
- The project must compile with no errors: `javac -d out src/*.java`.
- Run the application and click through your screen before requesting review.

## 6. Reviewing someone else's pull request

- Does it compile and run?
- Does it only change what the description says it changes?
- Are names clear and the code easy to read?
- Does it follow the standards in section 5?
- Be kind and specific. Suggest improvements, don't just say "wrong".

## 7. Reporting problems

Open a GitHub **Issue** describing what you expected, what happened, and the
steps to reproduce it. Add the label for the affected module.
