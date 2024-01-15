---
layout: post
title: C implementation of the DFA-NFA and e-NFA
date: 2019-02-08 09:56:00-0400
description: The provided C++ program implements a Deterministic Finite Automaton (DFA) using a menu-driven interface. The DFA is defined by specifying states, final states, alphabet, and transitions. Users can perform operations such as checking strings against the DFA, saving and loading configurations.
tags: project
categories: class-project
giscus_comments: false
related_posts: false
featured: false
---

# Documentation

## DFA (Deterministic Finite Automaton)

### Overview:

The provided C++ program implements a Deterministic Finite Automaton (DFA) using a menu-driven interface. The DFA is defined by specifying states, final states, alphabet, and transitions. Users can perform operations such as checking strings against the DFA, saving and loading configurations.

### Files:

1. **main.cpp:**
   - Implements the main logic for managing the DFA.
   - Utilizes a menu system for user interaction.
   - Supports operations like defining states, final states, alphabet, transitions, showing transitions, checking strings, saving configurations, loading configurations, and halting the program.

2. **DFA.hh:**
   - Contains the `DFA` class, representing the deterministic finite automaton.
   - Provides functions for defining states, final states, alphabet, transitions, showing transitions, checking strings, saving configurations, loading configurations, and halting the program.

### Compilation:

```bash
g++ -c main.cpp
g++ -c DFA.cc
g++ main.o DFA.o -o DFA
./DFA
```

---

## e-NFA (Nondeterministic Finite Automaton with ε-transitions)

### Overview:

Implementation of Nondeterministic Finite Automaton with ε-transitions (e-NFA) using a menu-driven approach. Similar to the DFA program, it allows users to define states, final states, alphabet, transitions, and perform operations like checking strings against the e-NFA. The program supports saving and loading configurations.

### Files:

1. **main.cpp:**
   - Implements the main logic for managing the e-NFA.
   - Utilizes a menu system for user interaction.
   - Supports operations like defining states, final states, alphabet, transitions, showing transitions, checking strings, saving configurations, loading configurations, and halting the program.

2. **e_NFA.hh:**
   - Contains the `e_NFA` class, representing the nondeterministic finite automaton with ε-transitions.
   - Provides functions for defining states, final states, alphabet, transitions, showing transitions, checking strings, saving configurations, loading configurations, and halting the program.

### Compilation:

```bash
g++ -c main.cpp
g++ -c e_NFA.cc
g++ main.o e_NFA.o -o e_NFA
./e_NFA
```

---

## NFA (Nondeterministic Finite Automaton)

### Overview:

This C++ program implements a Nondeterministic Finite Automaton (NFA) using a menu-driven approach. Similar to the DFA and e-NFA programs, users can define states, final states, alphabet, transitions, and perform operations like checking strings against the NFA. The program supports saving and loading configurations.

### Files:

1. **main.cpp:**
   - Implements the main logic for managing the NFA.
   - Utilizes a menu system for user interaction.
   - Supports operations like defining states, final states, alphabet, transitions, showing transitions, checking strings, saving configurations, loading configurations, and halting the program.

2. **NFA.hh:**
   - Contains the `NFA` class, representing the nondeterministic finite automaton.
   - Provides functions for defining states, final states, alphabet, transitions, showing transitions, checking strings, saving configurations, loading configurations, and halting the program.

### Compilation:

```bash
g++ -c main.cpp
g++ -c NFA.cc
g++ main.o NFA.o -o NFA
./NFA
```

---

**Note:** The compilation steps are provided assuming the use of g++ on a Unix-like system. Adjustments may be needed for different environments.