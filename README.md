# Combinator3000

Combinator3000 is a simple number-permutation tool that generates every unique ordering of the digits in a value you provide.

It includes:
- a Python script for direct CLI use
- a Windows batch launcher for interactive use
- a packaged `combinator.exe` binary in the repo

## Demo

![Combinator3000 demo preview](assets/combinator3000-demo-preview.gif)

[![Watch the full Combinator3000 demo](assets/combinator3000-demo-poster.png)](https://github.com/user-attachments/assets/52e5a8c3-8221-46ca-af1f-c08702ceb1f5)

If GitHub mobile does not play the embed inline, tap the preview card above to open the full demo clip.

## What It Does

Given an input like `123`, the tool generates all unique digit arrangements:

```text
123
132
213
231
312
321
```

If the number contains repeated digits, duplicate permutations are removed before output.

## Repo Contents

- `generate_combinations.py` - core permutation generator
- `run_combinations.bat` - interactive Windows launcher
- `ascii_art.py` - startup banner used by the batch flow
- `combinator.exe` - packaged executable build

## Requirements

### Python flow
- Python 3.x

### Windows launcher flow
- Windows Command Prompt
- Python 3.x available in `PATH`

## Quick Start

```bash
git clone https://github.com/gryszzz/Combinator3000.git
cd Combinator3000
```

### Run the Python script

```bash
python generate_combinations.py 1234
```

### Save the output to a file

```bash
python generate_combinations.py 1234 > combinations_1234.txt
```

### Run the Windows batch launcher

```bat
run_combinations.bat
```

The batch launcher prompts for a number and then runs the generator for you.

## How It Works

The Python script uses `itertools.permutations()` to generate permutations from the provided digits, then removes duplicates by converting the results into a set before printing them.

## Notes

- Output size grows very quickly as the number of digits increases.
- Repeated digits reduce the final number of unique outputs.
- The current Python script prints results to standard output. Use shell redirection if you want to save them into a file.

## License

This project is released under the Unlicense. See [LICENSE](LICENSE) for details.
