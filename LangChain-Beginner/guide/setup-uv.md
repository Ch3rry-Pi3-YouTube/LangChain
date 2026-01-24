# Setup: uv (Python dependency manager)

We use `uv` to manage dependencies and create the project `.venv`.

## Install uv
Follow the official instructions for your OS:
https://docs.astral.sh/uv/

## Initialize the project
From the project root, run:

uv init

What this does:
- Initializes a uv project by creating `pyproject.toml` (if missing)
- Creates or updates `uv.lock`
- Sets up the project metadata so uv can manage dependencies here

## Add LangChain
Then run:

uv add langchain

This adds `langchain` to `pyproject.toml`, resolves dependencies, and installs them into `.venv`.
If `.venv` does not exist yet, uv will create it.

## Notebook kernel (important)
When you run the notebooks, make sure the kernel is set to the `.venv` Python kernel.
That ensures the notebooks use the same dependencies you installed with uv.
