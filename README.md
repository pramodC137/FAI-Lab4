# FAI-Lab4 — Python & Autograder Tutorial

This lab is based on **UC Berkeley CS188 Project 0 (the Python / Autograder Tutorial)**.
Its purpose is to get familiar with Python basics and with the autograder that is
used to check all subsequent AI projects.

There are three small programming tasks. Each one asks you to fill in a function
where the placeholder `"*** YOUR CODE HERE ***"` appears.

## Requirements

- Python 3.x (developed/tested with Python 3.12)
- No third-party packages required — only the standard library

## Project Structure

| File | Description |
| --- | --- |
| `addition.py` | Task 1 — implement `add(a, b)` to return the sum of two numbers. |
| `buyLotsOfFruit.py` | Task 2 — implement `buyLotsOfFruit(orderList)` to compute the cost of a fruit order. |
| `shop.py` | `FruitShop` class used by the shopping tasks. |
| `shopSmart.py` | Task 3 — implement `shopSmart(orderList, fruitShops)` to pick the cheapest shop for a whole order. |
| `shopAroundTown.py` | Extra/optional exercise — find the optimal route between shops given a gas cost. |
| `town.py` | `Town` class (shops + distances) used by `shopAroundTown.py`. |
| `autograder.py` | Runs the test cases in `test_cases/` and reports your score. |
| `test_cases/` | Test definitions for questions `q1`, `q2`, `q3`. |
| `grading.py`, `testClasses.py`, `testParser.py`, `tutorialTestClasses.py`, `textDisplay.py` | Autograder support code. |
| `projectParams.py` | Project metadata (project name, files to submit, etc.). |
| `submission_autograder.py` | Packages your solution for submission. |
| `util.py` | Shared utility data structures used across CS188 projects. |

## The Tasks

### Task 1 — `addition.py`

Implement `add(a, b)` so it returns `a + b`.

```bash
python autograder.py -q q1
```

### Task 2 — `buyLotsOfFruit.py`

`buyLotsOfFruit(orderList)` receives a list of `(fruit, numPounds)` tuples and
returns the total cost using the `fruitPrices` dictionary.

Expected output when run directly:

```
Cost of [('apples', 2.0), ('pears', 3.0), ('limes', 4.0)] is 12.25
```

```bash
python buyLotsOfFruit.py
python autograder.py -q q2
```

### Task 3 — `shopSmart.py`

`shopSmart(orderList, fruitShops)` returns the `FruitShop` with the lowest total
price for the given order (the whole order must be bought at a single shop).

Expected output when run directly:

```
Welcome to shop1 fruit shop
Welcome to shop2 fruit shop
For orders:  [('apples', 1.0), ('oranges', 3.0)] best shop is shop1
For orders:  [('apples', 3.0)] best shop is shop2
```

```bash
python shopSmart.py
python autograder.py -q q3
```

## Running the Autograder

Run all questions:

```bash
python autograder.py
```

Run a single question (`q1`, `q2`, or `q3`):

```bash
python autograder.py -q q2
```

Other useful flags:

- `python autograder.py --no-graphics` — skip graphical tests (not needed here)
- `python autograder.py -t test_cases/q2/addTests` — run one specific test

## Licensing / Attribution

The Pacman AI projects were developed at UC Berkeley. The core projects and
autograders were primarily created by John DeNero and Dan Klein, with student-side
autograding added by Brad Miller, Nick Hay, and Pieter Abbeel.

These materials are provided for educational use only: do not distribute or publish
solutions, retain the original license notices, and give clear attribution to
UC Berkeley — http://ai.berkeley.edu.
