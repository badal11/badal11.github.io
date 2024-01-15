---
layout: post
title: TurboTuring Cpp Accelerated Turing Machine Simulator 
date: 2019-03-17 09:56:00-0400
description: 
tags: project
categories: class-project
giscus_comments: false
related_posts: false
featured: false
---

# Turing Machine Accelerator

This project is an attempt to replicate the remarkable work showcased in the online Turing machine simulator at [turingmachinesimulator.com](http://turingmachinesimulator.com), now implemented in C++ for faster testing of substantial machines. 

This project simulates a Deterministic Finite Automaton (DFA). It provides a menu-driven interface to define the DFA's states, final states, alphabet, transitions, and then allows users to check strings against the defined DFA.

**Components:**
1. **`DFA.hh`**: Header file for the DFA class declaration and its member functions.
2. **`Menu.hh`**: Header file for the Menu class declaration and its member functions.
3. **`main.cpp`**:
   - Includes necessary headers, declares a Menu instance, a DFA instance, and a string variable.
   - Defines a menu with options to manage DFA configuration and string checking.
   - Uses a loop to continuously display the menu and execute the selected option.

**Classes:**
1. **`DFA` Class:**
   - Manages the DFA configuration.
   - Allows users to define states, final states, alphabet, transitions, and check strings against the DFA.
   - Provides functionality to show transitions, save DFA configuration, and load DFA configuration.

2. **`Menu` Class:**
   - Manages the menu interface.
   - Allows the addition of submenus and the execution of menu options.

**Menu Options:**
1. **Define States (Option 1):**
   - Allows users to define states for the DFA.

2. **Define Final States (Option 2):**
   - Allows users to define final states for the DFA.

3. **Define Alphabet (Option 3):**
   - Allows users to define the alphabet for the DFA.

4. **Define Transitions (Option 4):**
   - Allows users to define transitions for the DFA.

5. **Show Transitions (Option 5):**
   - Displays the transitions of the DFA.

6. **Check String (Option 6):**
   - Prompts users to enter a string and checks whether it is accepted by the DFA.

7. **Save DFA Configuration (Option 7):**
   - Saves the DFA configuration to a file.

8. **Load DFA Configuration (Option 8):**
   - Loads the DFA configuration from a file.

9. **Exit (Option 9):**
   - Exits the program.

**User Interaction:**
- Users can interact with the DFA by defining its properties and checking strings against it through the menu-driven interface.

**Conclusion:**
This DFA Simulator provides a user-friendly interface to define and interact with a DFA. It offers functionalities to define states, final states, alphabet, transitions, and to check strings for acceptance by the DFA. The menu-driven approach enhances user experience and ease of use.

## Compilation
To build the simulator, simply use the following command:

```bash
make
```


## Operation
In the examples directory, you'll find various algorithms originally implemented for the online simulator, some directly copied, and others created by me. The basic syntax for simulation is as follows:

```bash
./turing <tm_code> <input_string>
```

If you wish to simulate the machine without providing input, you can use "_" as the second argument. The underscore character functions as the Turing machine's blank symbol.

### Flags
The simulator offers several flags to extract more information during simulation. The following summary is displayed when the simulator is executed without any arguments:

```bash
Usage
turing <tm_file> <input_word>

--show_machine [false]:
    Show a summary of the parsed TM
--show_steps [false]:
    Show each step of the main tape of the TM execution
--run [true]:
    Run the TM
--output [true]:
    Output the final content of the TM tapes
--max_steps [10000000]:
    Maximum number of steps
--limit [true]:
    Limit number of steps
```

## Examples
Try out these commands to witness the simulator in action:

```bash
# 5-state busy beaver machine. It will run for a while
./turing examples/bb5.tm _ --nolimit --nooutput

# Decimal to binary converter. This will only show the machine
./turing examples/dec2bin.tm --show_machine --norun

# Duplicate binary string with a single tape
./turing examples/dup_bin_string.tm 101 --show_steps

# Sort a list of binary numbers
./turing examples/list_sort.tm 0101#0011#0110#0111#0011#1000
```

Happy simulating! 🚀