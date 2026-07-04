# Shared ruff configuration

## Usage

This repository is intended to be installed as a Python package via the following dependency specifier:

    "ruff-config-ivasilev @ git+https://github.com/v--/ruff-config-ivasilev.git@v{ruff-version}.post{config-revision}"

After installing, the file `ruff.ivasilev.toml` should be placed into a `shared/ruff` directory by the package manager.

## Motivation

The linter [ruff](https://docs.astral.sh/ruff/) is quite convenient, however it suffers from some defects. It does not support custom presets (unlike, for instance, [eslint](https://eslint.org/)) and only has a minimal default preset (see [this discussion](https://github.com/astral-sh/ruff/discussions/3363)). Moreover, it cannot be extended with plugins (unlike [flake8](https://flake8.pycqa.org/en/latest/)).

I used to enable all rules (the "ALL" preset), but that turned out to be flaky with version updates (which has caused me issues when building [AUR](https://wiki.archlinux.org/title/Arch_User_Repository) packages). So I cherry-picked some useful rule groups and shared them here. Enabling an entire rule group like `S` or `RUF` is still flaky, but hasn't caused me issues yet.
