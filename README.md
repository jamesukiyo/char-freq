# Character Frequency Counter

A simple python script I made whilst deciding on a new keyboard layout for my corne v4.

I needed to know which symbols I use the most in my code so I could map them closer to the home row on the keyboard.

I can't guarantee this works everywhere but if something breaks feel free to open a PR or create an issue.

You can:
- save as a csv to use elsewhere
- exclude or include alphabetic characters
- exclude or include spaces/whitespace
- show a specific number of top chars
- edit the script to ignore other filetypes and directories

By default, many filetypes like images and directories such as node_modules are already ignored.

## Usage:
```
usage: char_freq.py [-h] [--top TOP] [--show-spaces] [--save-csv] [--exclude-letters] repo_path

Analyse character frequencies in a repository

positional arguments:
  repo_path          Path to the repository

options:
  -h, --help         show this help message and exit
  --top TOP          Number of top characters to display
  --show-spaces      Include spaces and whitespace characters in the output
  --save-csv         Save results as CSV in the current working directory
  --exclude-letters  Exclude all letters (A-Z, a-z) from the output
```

Example:
```
python char_freq.py --top 5 --exclude-letters ~/projects/go-http
```
Will show the top 5 non-alphabetic characters in a codebase.

## Things to add
- Add option to pass filetypes that should be included or excluded.
- Add option to pass directories that should be included or excluded.
