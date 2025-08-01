# python-examples

This repository collects representative Python projects that are useful for
test-driving Zed's Python integration and figuring out where we're lacking. Each
project is its own git submodule.

## Notes on specific projects

### pydantic-ai

This project uses a uv workspace setup, with a single uv.lock at the project
root where uv will create a venv, and several pyproject.toml manifests for
subprojects that share that lockfile.

Run `uv sync` at the root to set up the venv.

### langchain

This project has many pyproject.toml subprojects, each with its own uv.lock
(that is, it's not a uv workspace). Some of the subprojects depend on others.

Run `uv sync` in the subprojects that you're interested in to create venvs.
