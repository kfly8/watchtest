# watchtest

A simple file watcher that automatically runs Perl tests when files change.

## Requirements

- Perl 5.40+
- [watchexec](https://github.com/watchexec/watchexec)

## Usage

```bash
watchtest -- prove -lvr
```

This will watch `.pm` and `.t` files and run `prove -lvr` with the relevant test files when changes are detected.

## How it works

- Watches all `.pm` and `.t` files in your project
- When a test file (`.t`) changes, it runs that test
- When a module file (`lib/*.pm`) changes, it finds and runs the corresponding test file in `t/`

## Example

```bash
# Watch and run tests automatically
watchtest -- prove -lvr

# Get help
watchtest --help
```
