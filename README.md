# Quantum Computing with Qiskit

Below are the modules,

1. Fundamentals of Quantum Computing with Qiskit
2. Superdense Coding
3. Teleportation
4. Bernstein Vazirani Algorithm: Replacement for classical for-loop algorithm.
5. Deutsch Algorithm: Replacement to determine if function is constant or not.
6. Grover Algorithm: Replacement for classical search algorithm
7. Shor Algorithm: Breaking RSA encryption.
8. Variational Quantum Classifier
9. Quantum Kernel-based Classifier
10. Hybrid Neural Network (Quantum + Classical)


## Summary of Basics

- **Superposition**: A qubit can exist in multiple states (0 and 1) at the same time until it is measured.
    - For example, if a qubit is in a superposition of `|0›` and `|1›`, it holds a probability distribution of both states

- **Entanglement**: When two or more qubits are entangled, changing the state of one instantly affects the state of the other, no matter how far apart they are

- **Application**: Used in quantum cryptography and secure communications

- **Quantum Gates**: Manipulate qubits, just as classical logic gates (AND, OR, NOT) manipulate bits
    - **Z gate (π phase flip)**: Adds a 180° phase to `|1⟩`, leaving probabilities unchanged unless interference occurs later.
    - **S gate (π/2 phase shift)**: Adds a 90° phase to `|1⟩`, not affecting immediate probabilities but altering interference in subsequent gates.
    - **T gate (π/4 phase shift)**: Adds a 45° phase to `|1⟩`, preserving measurement probabilities alone while subtly influencing later interference outcomes.

- **Hadamard (H)**: Creates superposition (0 → 0 & 1 at the same time)

- **Pauli-X (X)**: Flips the qubit (0 → 1, 1 → 0)

- **CNOT (Controlled-NOT)**: Creates entanglement between qubits

- **Phase Shift (S, T, Z)**: Rotates the phase of the qubit state

- **Toffoli (CCNOT)**: Quantum version of classical AND gate

### Quantum Computing Mathematics

A Qubit state is reprsented as, where $α$ and $β$ are complex numbers representing probabilities - _where $|0⟩$ (north-pole) and $|1⟩$ (south-pole)_.

$|ψ⟩ = α|0⟩ + β|1⟩$

The probabilities must sum to $1$:

$|α|² + |β|² = 1$

For example, a Hadamard gate applied to $|0⟩$ creates an equal superposition state,

$|ψ⟩ = 1/√2 (|0⟩ + |1⟩)$

The Wave function is represented as $ψ$, which describes the Quantum system state,

$P(x) = |\psi(x)|^2$, $\int |\psi(x)|^2 \, dx = 1$

A general qubit state is

$|ψ⟩ = cos(θ/2) |0⟩ + e^{iφ} sin(θ/2) |1⟩$

- $θ$ (theta) determines the probability of measuring $0$ or $1$
- $φ$ (phi) determines the phase of the state

### Differences from Quantum to Classical Computing

| Feature | Classical Computing | Quantum Computing |
| --- | ---- | --- |
| **Unit of Information** | Bit (0 or 1) | Qubit (0, 1, or both simultaneously) |
| **Processing Speed** | Sequential processing | Parallel processing using superposition |
| **Scalability** | Limited for large problems | Exponentially faster for complex computations |
| **Key Principle** | Boolean Logic | Quantum Mechanics |
