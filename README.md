# Academic Services Portal

A Java Swing desktop application that gives students one place to use the
university's academic services: course registration, fee payment, exam
results, hostel applications and library services.

This repository belongs to the **iuea-uni-consortium** GitHub Organization and is
developed by several teams working in parallel.

## Project structure

```
academic-services-portal/
├── .github/
│   ├── CODEOWNERS                 # who must review which files
│   ├── pull_request_template.md   # checklist shown on every pull request
│   └── workflows/build.yml        # compiles the project on every pull request
├── .vscode/                       # VS Code run configuration
├── src/
│   ├── UniversityPortal.java          # shared shell: window, top bar, sidebar, navigation
│   ├── DashboardPanel.java            # landing page
│   ├── CourseRegistrationPanel.java   # course registration screen
│   ├── FeePaymentPanel.java           # fee payment screen
│   ├── ExamResultsPanel.java          # exam results screen
│   ├── HostelPanel.java               # hostel application screen
│   └── LibraryPanel.java              # library services screen
├── CONTRIBUTING.md
└── README.md
```

**Why one file per screen?** When every screen lived in a single file, two teams
editing different screens would constantly collide in the same file. With one file
per screen, each team edits its own files, merge conflicts become rare, and
GitHub can ask the right team to review each change.

## Teams and permissions

| Team | Repository role | Responsibility |
|---|---|---|
| `maintainers` | Admin | Shell, dashboard, repo settings, final say on merges |
| `registration-results-team` | Write | Course registration and exam results |
| `fees-hostel-team` | Write | Fee payment and hostel applications |
| `library-team` | Write | Library services |
| `stakeholders` | Read | Review and comment only |

## Running the application

Requires Java 17 or newer.

**In VS Code:** open this folder, install the *Extension Pack for Java*, open
`src/UniversityPortal.java` and click **Run** above `main`
(or choose **Run UniversityPortal** in the Run and Debug panel).

**From a terminal:**

```bash
javac -d out src/*.java
java -cp out UniversityPortal
```

The top bar loads a logo from a file named `IUEA LOGO.png` in the project root
folder (the folder you run the program from). If the file is missing the app
still runs, just without the logo.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
`main` is protected: all changes go through a reviewed pull request.
