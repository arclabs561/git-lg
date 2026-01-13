# git-lg

Structured `git log` output.

If the binary is in your `PATH`, you can run it as `git lg` (git subcommand).

## Example

```bash
git clone https://github.com/rust-lang/rust /tmp/rust
export GIT_DIR=/tmp/rust/.git

git lg | jq -r '.[].author_name' | sort | uniq -c | sort -nrk1
```

## Output

The output is a JSON array of commit objects with fields like `author_name`, `author_date`, `subject`, and `body`.

## License

Dual-licensed under MIT or the UNLICENSE.
