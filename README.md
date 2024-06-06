# pre-commit-xmllint

A simple wrapper for running xmllint from a pre-commit hook.

## Configuration

The default configuration formats `.xml` and `.qlr` files, and
specifies `--exc-c14n` for xmllint. You can override the arguments
with whatever you would like, but must terminate the argument
list with `--`. For example, if you just want to run format,
you can do it like this:

```
repos:
  - repo: https://github.com/mattpublic/pre-commit-xmllint.git
    rev: 0.0.1
    hooks:
      - id: xmllint-format
        args: [--format, --]
```
