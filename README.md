# Finite Automaton to Right-Linear Grammar Translator (AF → GLUD)

A C program that automatically translates a **Finite Automaton (FA)** into a **Right-Unit Linear Grammar (GLUD)**, developed for the **Formal Languages and Automata** course at **UTFPR Ponta Grossa**.

An academic article documenting the theory and implementation is included in this repository (`ARTIGO-LFA-AF-GLUD.pdf`).

---

## About

This project implements the classical theorem from formal language theory: every regular language recognized by a Finite Automaton can be equivalently described by a Right-Linear Grammar.

The program reads a finite automaton, validates whether it is deterministic, and generates a grammar whose productions follow the forms:

```
A → aB    (non-terminal transition)
A → a     (terminal production for accepting states)
```

---

## How It Works

```
Finite Automaton input
        │
        ▼
Determinism check     → Validates if the automaton is deterministic (DFA)
        │
        ▼
Production generation → Maps each transition δ(A, a) = B to A → aB
                        Maps accepting states to A → a
        │
        ▼
Grammar output        → Organized Right-Unit Linear Grammar (GLUD)
```

---

## Features

- Reads a finite automaton from input
- Checks for determinism
- Generates grammar productions `A → aB` and `A → a`
- Outputs the complete Right-Unit Linear Grammar

---

## Tech Stack

| | |
|---|---|
| Language | C |
| Theory | Formal Languages and Automata |

---

## How to Run

**Requirements:** GCC installed.

```bash
# Compile
gcc LFA-T2-AF-GLUD.c -o tradutor

# Run
./tradutor
```

---

## Repository Contents

| File | Description |
|---|---|
| `LFA-T2-AF-GLUD.c` | Main program — FA to GLUD translator |
| `ARTIGO-LFA-AF-GLUD.pdf` | Academic article documenting theory and implementation |

---

## Academic Context

Developed for the **Formal Languages and Automata (LFA)** course at UTFPR Ponta Grossa. The project applies the formal equivalence between finite automata and right-linear grammars, a foundational concept in the theory of computation.

---

## Author

[Giovanni Veratacci](https://github.com/nagisavt) — Computer Science student at UTFPR Ponta Grossa
