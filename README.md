

# Ridiculous Life Advice Machine (RLAM) 🤖✨

A Python terminal application developed for a highly questionable technology company, providing essential everyday services of dubious practical value.

---

## 📌 Project Overview

The **Ridiculous Life Advice Machine (RLAM)** is a modular CLI application built to demonstrate core Python programming paradigms including modularization, control flow, iterative loops, user input validation, and external library integration (`random` and `math`).

### Core Features

1. **Motivational Message Generator:** Dispenses inspirational yet fundamentally unhelpful life advice.
2. **Ridiculous Excuse Generator:** Produces on-demand batches of recycled excuses for everyday blunders.
3. **Unscientific Luck Score Calculator:** Uses a pseudo-mathematical formula to calculate a person's official luck quotient.

---

## 🎯 Learning Objectives

- Constructing controlled interactive loops (`while`) for menus and input validation.
- Iterating with counted loops (`for` with `range()`).
- Modular programming: defining, importing, and separating logic into custom Python modules.
- Implementing **void functions** vs. **value-returning functions**.
- Passing arguments and handling parameters.
- Working with built-in standard modules (`math`, `random`).

---

## 📂 Project Architecture

Both files must reside in the same directory:

```text
ridiculous-life-advice-machine/
├── main.py              # Application entry point: CLI menu, user routing, loop control
├── ridiculous_tools.py  # Utility module: functional logic and calculations
└── README.md            # Project documentation
```

### File Responsibilities

| File | Responsibilities |
| :--- | :--- |
| `main.py` | Contains `main()`, drives the interactive `while` loop, captures/validates input, and displays returned calculation results. |
| `ridiculous_tools.py` | Standalone module providing `motivational_message()`, `generate_excuses()`, and `calculate_luck()`. |

---

## 🛠️ Function Specifications

### 1. `motivational_message()`
- **Type:** Void function (no parameters, returns nothing).
- **Module:** `ridiculous_tools.py`
- **Behavior:** Generates a random integer ($1 \le n \le 5$) using `random.randint()` and prints a corresponding motivational quote.

### 2. `generate_excuses(quantity)`
- **Type:** Void function (accepts `quantity: int`, returns nothing).
- **Module:** `ridiculous_tools.py`
- **Behavior:** Runs a `for` loop across `range(quantity)`. Each iteration randomly selects and prints one of 5 preset excuses numbered sequentially.

### 3. `calculate_luck(age, lucky_number)`
- **Type:** Value-returning function (accepts `age: int`, `lucky_number: int`).
- **Module:** `ridiculous_tools.py`
- **Formula:** $$\text{Luck Score} = \lceil \sqrt{\text{age}} \times \text{lucky number} \rceil$$
- **Behavior:** Prints `"Calculating your luck score..."`, computes the score using `math.sqrt()` and `math.ceil()`, and returns the calculated integer to `main()` without printing the final score itself.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x installed on your machine.

### Installation & Execution

1. Clone or download this repository:
   ```bash
   git clone https://github.com/<your-username>/ridiculous-life-advice-machine.git
   cd ridiculous-life-advice-machine
   ```

2. Verify both script files are in the same directory:
   ```bash
   ls main.py ridiculous_tools.py
   ```

3. Run the application:
   ```bash
   python main.py
   ```

---

## 💻 Example Output

```text
-----------------------------------------------
RIDICULOUS LIFE ADVICE MACHINE
-----------------------------------------------
1. Motivational Message Generator
2. Ridiculous Excuse Generator
3. Calculate Your Luck Score
4. Exit
------------------------------------
Enter your choice (1-4): 2

How many excuses would you like? 3
YOUR OFFICIAL EXCUSES:
Excuse 1: My computer was updating its feelings.
Excuse 2: My homework was abducted by highly educated aliens.
Excuse 3: My alarm clock and I are no longer on speaking terms.
-------------------------------------------------------

-----------------------------------------------
RIDICULOUS LIFE ADVICE MACHINE
-----------------------------------------------
1. Motivational Message Generator
2. Ridiculous Excuse Generator
3. Calculate Your Luck Score
4. Exit
------------------------------------
Enter your choice (1-4): 3

Enter your age: 25
Enter your lucky number: 7
Calculating your luck score...
Your official luck score is: 35
This number has no scientific meaning, but it looks impressive!

-----------------------------------------------
RIDICULOUS LIFE ADVICE MACHINE
-----------------------------------------------
1. Motivational Message Generator
2. Ridiculous Excuse Generator
3. Calculate Your Luck Score
4. Exit
------------------------------------
Enter your choice (1-4): 4

Thank you for using the Ridiculous Life Advice Machine!
```
