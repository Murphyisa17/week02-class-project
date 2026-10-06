# Week 2 Class Project — Ohm's Law Calculator

## Purpose
Reads a voltage and a resistance, and calculates the current using Ohm's Law (I = V / R).

## Input Format
Two numbers on one line, separated by a space: `<voltage> <resistance>`

## Build and Run
g++ -std=c++17 -Wall -Wextra -pedantic src/main.cpp -o build/app
./build/app

Then type a voltage and resistance, e.g. 12 4, and press Enter.

## Example Output
$ echo "12 4" | ./build/app
Current: 3 A

## Run the Acceptance Tests
bash test.sh

Expected output: All acceptance tests passed

## Limitations
- Does not handle negative voltage as a separate error case.
- Only supports whole-line space-separated input, not comma-separated or multi-line input.

## Debugging Reflection
While setting this project up, I ran into a few real issues: pasting multi-line
heredoc commands into the terminal sometimes corrupted them (extra characters,
or commands run together), and a GitHub personal access token initially lacked
the workflow scope needed to push .github/workflows/cpp.yml, which GitHub
rejected with a clear error message pointing at the missing scope. Both were
fixed by typing/pasting commands one at a time and regenerating the token with
the correct scopes checked.
