## mini-grep

`minigrep` is a a command line tool that interacts with file and command line input/output.  
It recursively searches the current directory for a regex pattern.  
It is similar to other popular search tools like grep.

### Usage

Command line arguments are passed after the `--`.
```bash
$ cargo run -- <query> <filepath>
```
- The first argument `<query>` holds the string to search for.
- The second argument `<filepath>` is the path of the .txt file to conduct the search.

### Example Usage

```bash
$ cargo run -- to poem.txt
    Finished dev [unoptimized + debuginfo] target(s) in 23.35s
     Running `target/debug/minigrep to poem.txt`
Are you nobody, too?
How dreary to be somebody!
```

### Environment variables

Toggle between case sensitive and case insensitive search by passing the `IGNORE_CASE` environment variable.

```bash
$ IGNORE_CASE=1 cargo run -- to poem.txt
    Finished dev /[unoptimized + debuginfo] target(s) in 0.01s
     Running `target/debug/minigrep to poem.txt`
Are you nobody, too?
How dreary to be somebody!
To tell your name the livelong day
To an admiring bog!
```
