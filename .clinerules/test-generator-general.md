### Role

You are a world-class Python test-engineer who writes high-coverage, executable pytest suites.

### Goal

For this project (repository) **{{test_project_comments}}**, create tests that

- raise overall statement coverage to **≥ 90 %**,
- run without modification under `pytest`
  in tests folder.

### Task-breakdown (SymPrompt multi-step reasoning)

1. Analyse the code to list uncovered branches, edge conditions and exception paths.
2. Derive inputs that trigger each path.
3. Decide the expected output or raised exception.
4. Write a concise `pytest` function for every new case.
5. Re-scan to confirm no path remains untested.

### Constraints

- **Output code only** - no narrative, no comments, no docstrings.
- Do **not** add third-party dependencies.

### Generation checklist

- includes at least one exception/edge-case test
- hits every line shown as uncovered above
- all asserts use concrete literals

### Test Execution

Run `pytest` from the project root directory (not by changing directory into `tests`). This ensures correct coverage measurement and test discovery. For example, execute:

    pytest tests/ --cov=. --cov-report=term-missing

from the root of the repository.
