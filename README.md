# CPS 490 -- IA 01 Git Lab

This package creates the disposable repositories used by **IA 01 - Git State,
History, and Recovery**.

## Reference environment

The course reference environment is the **Ubuntu 24.04 VM on the Dayton
Regional Cyber Range**. Before using this package there, complete the course
handout *Setting Up Your Ubuntu 24.04 VM*.

The package also supports:

- Git Bash on Windows; and
- Bash on macOS.

Use Bash for the commands below. The lab does **not** require Python.

## Requirements

You need:

- Bash
- Git and
- standard command-line tools supplied by the supported environments.

Verify the two important requirements with:

```bash
git --version
bash --version
```

On Windows, run the lab from **Git Bash**, not Command Prompt or PowerShell.

## Build the lab

Open a terminal in the directory containing this README and run:

```bash
bash ./build-git-lab.sh git-lab
bash ./check-git-lab.sh git-lab
```

Do not begin IA 01 unless the checker ends with:

```text
Git lab: READY
```

The generated `git-lab/` directory contains the independent scenarios used by
the assignment.

## Generated scenarios

- `01-objects/`
- `02-staging/`
- `03-remotes-alice/`, `03-remotes-bob/`, and `03-origin.git/`
- `04-merge/`
- `05-rebase/`
- `06-interactive-rebase/`
- `07-conflict/`
- `08-reset-reflog/`
- `09-bisect/`

The assignment tells you which numbered repository to use for each part.

## Reset the lab

To return **all** scenarios to their original states, run:

```bash
bash ./reset-git-lab.sh git-lab
bash ./check-git-lab.sh git-lab
```

**Reset is destructive.** It deletes and recreates the entire generated
`git-lab/` directory. Capture any evidence you need before resetting, and do not
store your report, screenshots, notes, or unrelated files inside `git-lab/`.

## What the checker does

`check-git-lab.sh` verifies that every required scenario exists and still looks
like its intended starting state. It does not grade your work and does not tell
you which Git commands to use for the assignment.

## Working rules

- Work in the scenario named by the assignment part.
- Use ordinary Git commands and ordinary file editing.
- Do not edit `.git/` internals directly.
- The setup scripts may be inspected, but submitted evidence must come from the
  generated repositories.
- The numbered scenarios are independent.
- When IA 01 asks you to run a supplied shell test, invoke it through Bash, for
  example `bash ./tests/test-parser.sh`.

## Interactive rebase

Part 5 opens the Git editor configured by `core.editor`. Follow the editor
instructions from the course VM setup handout, or use another Git editor you
have already configured and know how to save and exit.
