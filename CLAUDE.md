# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Python project called "uv-cats" that displays cat information for specified breeds. The project uses `uv` as its package and dependency manager.

## Python Version

This project requires Python 3.14 or higher (specified in `.python-version` and `pyproject.toml`).

## Package Management with UV

This project uses `uv` instead of pip or poetry. All dependency management and virtual environment operations should be done through `uv`.

### Common Commands

**Running the application:**
```bash
uv run main.py
```

**Installing dependencies:**
```bash
uv sync
```

**Adding a new dependency:**
```bash
uv add <package-name>
```

**Adding a development dependency:**
```bash
uv add --dev <package-name>
```

**Running Python in the project environment:**
```bash
uv run python <script.py>
```

**Running a command in the project environment:**
```bash
uv run <command>
```

## Project Structure

The project is currently in early stages with a simple structure:
- `main.py` - Entry point with a `main()` function
- `pyproject.toml` - Project configuration and dependencies
- `uv.lock` - Locked dependency versions (managed by uv)

## Development Notes

- The project uses uv's lock file (`uv.lock`) for reproducible dependency resolution
- Virtual environment is automatically managed by uv (no need to manually activate)
- Always use `uv run` prefix when executing Python scripts or commands to ensure they run in the correct environment
