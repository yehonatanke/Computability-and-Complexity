### Finite Automata (FA):
- A finite automaton is a mathematical model of computation.
- It consists of a finite set of states, a set of input symbols, a transition function, an initial state, and a set of accepting (or final) states.
- Example: A simple finite automaton recognizing strings with an even number of 0s: 
  $M = ({q_0, q_1}, {0, 1}, δ, q_0, {q_0})$
  where $δ$ is the transition function such that $δ(q_0, 0) = q_1$ and $δ(q_1, 0) = q_0$.

### Non-finite Automata:
- These are automata that do not have a finite number of states.
- Examples include pushdown automata (PDA) and Turing machines (TM).

### Regular Languages:
- Languages that can be recognized by finite automata are called regular languages.
- They can also be defined using regular expressions.
- Example: The language of all strings over {0, 1} that end with '1' is regular.

### Irregular Languages:
- Languages that cannot be recognized by any finite automaton are called irregular languages.
- They may require more powerful computational models like Turing machines.
- Example: The language of balanced parentheses is irregular.

### Turing Machine (TM):
- A Turing machine is a theoretical computing machine that can simulate any algorithmic process.
- It consists of an infinitely long tape divided into cells, a read/write head, a finite set of states, and a transition function.
- Example: A Turing machine that adds two binary numbers.

In mathematical notation, a Turing machine M can be represented as:
$M = (Q, Σ, Γ, δ, q_0, q_{accept}, q_{reject})$
where:
- $Q$ is a finite set of states,
- $Σ$ is the input alphabet,
- $Γ$ is the tape alphabet,
- $δ$ is the transition function,
- $q_0$ is the initial state,
- $q_{accept}$ is the accepting state, and
- $q_{reject}$ is the rejecting state.

The transition function δ is defined as:
$δ : Q × Γ → Q × Γ × {L, R}$
indicating the next state, symbol to write, and direction to move (left or right) based on the current state and symbol read from the tape.

---

### Sorting Algorithms:

| Algorithm       | Time Complexity (Best) | Time Complexity (Average) | Time Complexity (Worst) | Space Complexity (Worst) |
|-----------------|------------------------|----------------------------|--------------------------|--------------------------|
|                 |                        |                            |                          |                          |
| Quicksort       | $Ω(n log(n))$            | $Θ(n log(n))$                | $O(n^2)$                   | $O(log(n))$                |
| Mergesort       | $Ω(n log(n))$            | $Θ(n log(n))$                | $O(n log(n))$              | $O(n)$                     |
| Timsort         | $Ω(n)$                   | $Θ(n log(n))$                | $O(n log(n))$              | $O(n)$                     |
| Heapsort        | $Ω(n log(n))$            | $Θ(n log(n))$                | $O(n log(n))$              | $O(1)$                     |
| Bubble Sort     | $Ω(n)$                   | $Θ(n^2)$                     | $O(n^2)$                   | $O(1)$                     |
| Insertion Sort  | $Ω(n)$                   | $Θ(n^2)$                     | $O(n^2)$                   | $O(1)$                     |
| Selection Sort  | $Ω(n^2)$                 | $Θ(n^2)$                     | $O(n^2)$                   | $O(1)$                     |
| Tree Sort       | $Ω(n log(n))$            | $Θ(n log(n))$                | $O(n^2)$                   | $O(n)$                     |
| Shell Sort      | $Ω(n log(n))$            | Θ(n(log(n))^2)             | $O(n(log(n))^2)$           | $O(1)$                     |
| Bucket Sort     | $Ω(n+k)$                 | $Θ(n+k)$                     | $O(n^2)$                   | $O(n)$                     |
| Radix Sort      | $Ω(nk)$                  | $Θ(nk)$                      | $O(nk)$                    | $O(n+k)$                   |
| Counting Sort   | $Ω(n+k)$                 | $Θ(n+k)$                     | $O(n+k)$                   | O(k)                     |
| Cubesort        | $Ω(n)$                   | $Θ(n log(n))$                | $O(n log(n))$              | $O(n)$                     |

---

### Data Structures:

| Data Structure        | Time Complexity (Average) | Time Complexity (Worst) | Space Complexity (Worst) |
|-----------------------|---------------------------|-------------------------|--------------------------|
|                       | Access | Search | Insertion | Deletion | Access | Search | Insertion | Deletion |
| Array                 | $Θ(1)$   | $Θ(n)$   | $Θ(n)$      | $Θ(n)$      | $O(1)$   | $O(n)$   | $O(n)$      | $O(n)$      |
| Stack                 | $Θ(n)$   | $Θ(n)$   | $Θ(1)$      | $Θ(1)$      | $O(n)$   | $O(n)$   | $O(1)$      | $O(1)$      |
| Queue                 | $Θ(n)$   | $Θ(n)$   | $Θ(1)$      | $Θ(1)$      | $O(n)$   | $O(n)$   | $O(1)$      | $O(1)$      |
| Singly-Linked List    | $Θ(n)$   | $Θ(n)$   | $Θ(1)$      | $Θ(1)$      | $O(n)$   | $O(n)$   | $O(1)$      | $O(1)$      |
| Doubly-Linked List    | $Θ(n)$   | $Θ(n)$   | $Θ(1)$      | $Θ(1)$      | $O(n)$   | $O(n)$   | $O(1)$      | $O(1)$      |
| Skip List             | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $O(n)$ | $O(n)$ | $O(n)$ | $O(n)$   | $O(n log(n))$ |
| Hash Table            | N/A    | $Θ(1)$   | $Θ(1)$      | $Θ(1)$      | N/A    | $O(n)$   | $O(n)$      | $O(n)$      |
| Binary Search Tree    | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $O(n)$ | $O(n)$ | $O(n)$ | $O(n)$      | $O(n)$      |
| Cartesian Tree        | N/A    | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | N/A    | $O(n)$   | $O(n)$      | $O(n)$      |
| B-Tree                | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(n)$ |
| Red-Black Tree        | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(n)$ |
| Splay Tree            | N/A    | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | N/A    | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(n)$ |
| AVL Tree              | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(log(n))$ | $O(n)$ |
| KD Tree               | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $Θ(log(n))$ | $O(n)$ | $O(n)$ | $O(n)$ | $O(n)$      | $O(n)$      |
