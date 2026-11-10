# Student CI Project (CMSC 426)

A minimal Python application used to demonstrate Continuous Integration with Jenkins and GitHub.

## Files
- `app.py`: a simple addition function and application entry point.
- `tests/test_app.py`: automated unit tests using Python's built-in `unittest` module.

## Requirements
- Python 3
- Git (for local cloning or Jenkins checkout)
- Jenkins and its Git plugin (for automated CI)

No external Python packages are required.

## Run the application
```bash
python app.py
```

## Run the tests
```bash
python -m unittest discover -s tests -v
```

## Check syntax (preparation/build step)
```bash
python -m py_compile app.py
```

## CI behavior
Jenkins checks out the GitHub repository, checks Python syntax, runs the unit tests, and fails the job when a test exits with a non-zero status. GitHub webhook or Jenkins SCM polling can trigger automatic builds on a commit.

This project uses Jenkins to run automated tests after repository changes.
