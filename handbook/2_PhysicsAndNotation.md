# **Physics And Notations**

## **A Note To Readers**

We welcome you to this beautiful journey of quantum. In this section we will introduce you to some basic concepts of physics and maths required to explore our quantum world. With our experience we have given our utmost effort to make things easy and understandable in simple language. It is not a difficult glossary containing textbook but a guide written with passion.

Instead of introducing you to the basic math concepts we are opting for a different approach. We will take physics and maths simultaneously. It means that we will introduce some physics concepts, then will give a problem or scenario and its solution will explain the math concept from scratch. This will help you to grasp math concepts and how to apply them in a physics scenario. It will solve a problem which I encountered during my learning journey that how to apply a mathematical tool in a problem or how to proceed further if you are stuck anywhere. 

All the best and keep going. Remember in quantum, your intuition can get wrong but maths can’t. So trust the calculation not your heart. 

## **Contents**

1. **Quantum: New Physics Season 2.O**  
   1. We have Classical Mechanics. Then why do we need Quantum Mechanics?  
      1. What classical mechanics can not explain.  
      2. Introduction to Quantum Mechanics  
   2.  Can we apply Quantum Logic to Classical Problems?  
   3. Fundamentals of Quantum  
      1. Heisenberg Principle  
      2. Multiple States at Once -- SuperPosition

2. **Qubits**  
   1. Classical Bits Vs Qubits  
   2. Quantum Computing  
      1. How can we create a Quantum Processor
      2. Decoherence
   3. Notations  
      1. Psi symbol  
      2. Ket and bra notations  
   4. Probability amplitudes  
      1. Standard Notation  
      2. Normalization  
      3. |+\> and |-\> state  
         

3. **Quantum Gates and its Matrix Form**   
   1. What are Quantum gates?  
      1. Intro To gates   
      2. Their matrix form  
   2. How can we apply Gates to Qubits  
      1. Matrix representation of Qubit  
      2. How we apply gates (Both matrix and Psi representation)

4. **Operations On Qubit**  
   1. Dot Product  
   2. Tensor Product  
   3. Measurement of Qubit  
   4. Probability of observing a basis state in Ψ

5. **Multiple Qubit Systems and their maths**  
   1. How we can get Ψ of multiple qubits?  
   2. Operations on Multiple Qubits  
      1. Ψ and Matrix representation  
   3. Special Cases:  
      1. Entanglement  
      2. Bell state

      

      

# **Chapter 1**

## **a).We have Classical Mechanics. Then why do we need Quantum Mechanics?**

We had classical mechanics till late 1800’s thanks to Newton and Maxwell. You have learnt Newton Laws and Maxwell equations in your JEE Physics. Let’s recall the laws that can explain the following:

1. Predict motion of planets (Newton & Kepler \- Gravitation Chapter)

2. Explain falling objects, pendulums, projectiles. (Kinematic Chapter)

3. Describe electricity, magnetism, and light as waves (Maxwell)

Many physicists thought physics was "complete."

Scientists found that classical physics works well for matter and energy at the macroscopic, human scale.  
But at the microscopic level, particles showed behaviors classical theory couldn’t explain—leading to a new story in physics.

   **The Debate of Nature of Light (Particle Vs Wave)**  
(Story based on real life facts, narrated like a dialogue driven story. It includes your JEE concepts only.)
<!-- This whole thing needs to go -->

Let us travel to the time when the concept of Quantum was unknown. 

Newton \- Light has particle nature. Take a ball and hit it on the wall and it will bounce making the same angle of incidence and reflection. Just like the light with a mirror.

Huygens \- No Newton, light is just a wave. Reflection can be explained by my theory of the Huygens Principle.

Newton \- But it cannot have both nature simultaneously. It's the core idea of Classical Mechanics. We cannot have two different possibilities at once, Huygens. Classical Mechanics is all about having 100% certainty.

Huygens \- Yeah, you are correct, light must have one nature according to our classical physics. But…..

Young Thomas \- Wait guys, I have my double slit experiment where light has constructive and destructive interference just like water waves.

Huygens \- Yess\!\!\! And my Huygens Principle can explain interference. 

Newton \- Yeah you win. Your wave theory can explain reflection, refraction and interference. I think light has a wave nature.

Maxwell \- And I have my mathematical equations to describe the state of light as waves… Light is an electromagnetic wave.

Einstein \- Wait guys I have my photoelectric effect. It can only be explained by light’s particle nature. 

Plank \- Yes and my quantized nature of photon energy tells that light has a particle nature because energy flows in packets just like particles.

Plank \- It means light has DUAL nature. We have proved both nature by experiments and maths. But how is it possible for anything in this world to exist in 2 entirely different states? 

De Broglie \- If light can have dual nature then other objects like electrons can also have dual nature??? It means our classical theory fails to explain everything in this world. **We have to begin Physics Season 2.O…**

<!-- -->

**Introduction To Quantum Mechanics**  
**Quantum Mechanics**

**• Fundamental difference:**  
● C.Mech: Future history of a particle is completely  
determined by its initial position and momentum  
together with the forces that act upon it.

● Q.Mech: Nature of an observable quantity is  
different in the atomic realm

Cause and effect are related, but “certainty” is  
“Impossible”. It is a probabilistic concept.

Quantum Mechanics says every particle has dual nature. It has wavelength, frequency (wave like nature) and quantization of energy ( discrete energy packets).

Discretization of energy level  (Max Planck 1900\) \-   
The below formula connects both concepts \-   
∆ E \= hν (quantum of action).  
 

## **b) Can we apply quantum logic to Classical Problems**

Yes, we can say classical is just an approximation of quantum mechanics.  
**“certainties are illusory”**  
Ordinary objects consist of large atoms and we observe  
average behavior. Let's understand this by an example-  
You know de-broglie wavelength \= h/p. Now momentum is of order 10 but h is so small, hence the wavelength obtained is so small to observe.  
 

## **c) Fundamentals of Quantum**

**i) The Heisenberg Uncertainty Principle**  
The Heisenberg Uncertainty Principle is one of the pillars of quantum mechanics introduced in 1927\.   
It is the same as your JEE physics Heisenberg principle that “You can’t know both the exact position and the exact speed of a tiny particle (like an electron) at the same time.” Δx⋅Δp≥(h/4π)​

As the position of an electron is uncertain, so is the quantum state.

In quantum computing, this principle reminds us that measuring a quantum system disturbs it. We cannot observe everything about it without changing it. This limitation is also what makes quantum systems powerful, as it allows them to process information in ways classical systems cannot.

**ii) SuperPosition Principle**  
In our daily life, a coin is either head or tails, a switch is either on or off, a person is either male or female. But in quantum life, a coin can be both head and tails at the same time.   
This principle is called superposition which states that a particle can be in multiple states at the same time(until we observe it). A coin spinning in air is a mix of both heads and tails at the same time(superposition).  
This allows quantum computers to:

* Try many possibilities at once  
* Solve certain problems much faster than normal computers

Let’s say we have one particle in the state:

∣ψ⟩=​(∣0⟩+​∣1⟩)/root2

This means:

There's a 50% chance to get 0,

And a 50% chance to get 1 when we measure it.

But before measuring, the system is in a mix — holding both possibilities at once.

**Don’t worry if you don’t understand these notations as they will be explored in detail in further sections.**

# **Chapter 2** **Qubits**

## Qubits vs. Classical Bits  

At first glance, the term qubits may seem similar to bits, but they represent different concepts. Qubits can perform tasks that classical bits cannot achieve.  

a) Classical Bits vs. Qubits    
In classical computers, data is stored and processed using bits, which can take only one value at a time, either 0 or 1\.    
Quantum computers, on the other hand, use quantum bits (qubits). Unlike classical bits, a qubit can be in state 0, state 1, or a superposition of both at the same time. This unique property allows quantum computers to explore many possibilities in parallel.  

Key distinctions include:  

i. State    
Bit: Can exist only as 0 or 1\.    
Qubit: Can exist as 0, 1, or a superposition of both.    
Analogy: A coin lying flat shows either heads or tails (bit). A spinning coin represents a mix of both outcomes (qubit).  

ii. Measurement    
Bit: Measuring a bit does not change its value.    
Qubit: Measurement forces the qubit to collapse to either 0 or 1, destroying the superposition.    
Analogy: Opening a wrapped gift—you only know its contents after opening it, and the act of opening finalizes the surprise.  

iii. Computational Potential    
Bit: Processes information step by step.    
Qubit: Uses quantum properties like superposition to evaluate many possibilities at once, allowing certain problems to be solved much faster.  

b) Quantum State    
In classical physics, an object can be fully described by measurable quantities like its position and velocity.    
In quantum mechanics, however, we describe particles using a quantum state, which includes all the information that can be known about the system.    
For example, a spinning coin in the air is like a superposition of heads and tails. Once caught (measured), it produces a definite outcome, either heads or tails.    
For a single qubit, the quantum state is represented as:    
∣ϕ⟩=α∣0⟩+β∣1⟩  
Here, α and β are complex numbers that determine the probabilities of observing the qubit in state ∣0⟩ or ∣1⟩. The condition    
∣α∣^2+∣β∣^2=1 ensures that the total probability equals 1\.    
When measured:    
The qubit collapses to ∣0⟩  with probability ∣α∣^2.    
The qubit collapses to ∣1⟩ with probability ∣β∣^2.    
So, while the qubit exists in superposition before measurement, the act of measurement forces it into a definite state.  

c) Notation (Bra-Ket Formalism)    
Quantum mechanics commonly uses Dirac notation to represent quantum states:    
i. Ket ∣⋅⟩   
Represents a quantum state.    
Examples:    
∣0⟩  → state “0”    
∣1⟩  → state “1”    
∣ϕ⟩=α∣0⟩+β∣1⟩ → superposition of both states  

ii. Bra ⟨⋅∣     
Represents the conjugate transpose (mirror) of a ket. <!-- FIXME: This would make no sense since you did not define that a ket is expressable as a column matrix/vector -->  
If ∣ψ⟩ is a state, then its bra is ⟨ψ∣.  

iii. Bra-Ket ⟨⋅∣⋅⟩    
Represents an inner product, similar to a dot product in vectors.    
Examples:    
⟨0∣0⟩=1   
⟨0∣1⟩=0     
This notation is essential for calculating probabilities of measurement outcomes.    
iv. Symbols (ϕ and ψ)    
The Greek letters ϕ (phi) and ψ (psi) are commonly used to denote quantum states, much like x and y are used in mathematics.    
For example, ∣ϕ⟩ | or ∣ψ⟩ may each represent a qubit in superposition.

matrix  representation, tensor product and other basic maths to be explained here

**Multiple Qubit Systems**  

1\. How can we get Ψ of multiple qubits?

For a single qubit, the state is written as  
∣𝜓⟩ \= 𝛼∣0⟩ \+ 𝛽∣1⟩, 𝛼, 𝛽 ∈ 𝐶, ∣𝛼∣² \+ ∣𝛽∣² \= 1\.

When we combine multiple qubits, we get their overall state using the tensor product (⊗). For example, for two qubits:  
∣𝜓⟩ \= ∣𝜓₁⟩ ⊗ ∣𝜓₂⟩  
If  
∣𝜓₁⟩ \= 𝑎∣0⟩ \+ 𝑏∣1⟩ and ∣𝜓₂⟩ \= 𝑐∣0⟩ \+ 𝑑∣1⟩,  
then  
∣𝜓⟩ \= 𝑎𝑐∣00⟩ \+ 𝑎𝑑∣01⟩ \+ 𝑏𝑐∣10⟩ \+ 𝑏𝑑∣11⟩.

Thus, for n qubits, the state vector lives in a 2ⁿ-dimensional Hilbert space.

2\. Operations on Multiple Qubits

Quantum operations are always represented by unitary matrices. These are linear transformations that keep the length of the state vector the same. In a multi-qubit system, these operations extend naturally from single-qubit gates to multi-qubit gates.

2.1 Single-Qubit Gates in Multi-Qubit Systems

A single-qubit gate acts on one qubit in an n-qubit register. It is shown as the tensor product of the gate with identity matrices for the qubits that are not affected.

Example: Applying the Hadamard gate H to the first qubit of a two-qubit system:

U \= H ⊗ I \=   
1/2  
\[1    1    0    0  
1   \-1    0    0  
0    0    1    1  
0    0    1   \-1\]

This setup ensures only the selected qubit changes while the others stay the same.

2.2 Two-Qubit Gates <!-- Doesn't make sense to introduce here since gates are detailed below right? Especially with Kronecker products -->

Some operations need two qubits. These gates create correlations or entanglement between qubits.  
Controlled-NOT (CNOT): Flips the second qubit (target) only if the first qubit (control) is in |1⟩.

CNOT \=  
\[1    0    0    0  
0    1    0    0  
0    0    0    1  
0    0    1    0\]

SWAP gate: Switches the states of two qubits.  
SWAP \=  
\[1    0    0    0  
0    0    1    0  
0    1    0    0  
0    0    0    1\]

These gates are crucial for communication between qubits in a circuit.

2.3 Multi-Qubit Operations

For n qubits, a valid quantum operation is always a 2^n × 2^n unitary matrix. Examples include:

Tensor product of single-qubit gates: To apply Hadamard to both qubits at once:

H ⊗ H \=   
1/2  
\[1    1    1    1  
1   \-1    1   \-1  
1    1   \-1   \-1  
1   \-1   \-1    1\]

Composite circuits: By combining tensor products and multi-qubit gates, we can construct complex algorithms like Shor’s and Grover’s.

3\. Special Case: Entanglement

Entanglement is one of the most important and unique aspects of quantum mechanics.It describes a situation in which the state of a composite quantum system cannot be separated into independent states of its subsystems.

3.1 Definition  
A two-qubit state ∣ψ⟩ is separable (not entangled) if it can be expressed as  
∣𝜓⟩=∣𝜓1⟩⊗∣𝜓2⟩

for some single-qubit states ∣𝜓1⟩ and ∣𝜓2⟩.  
If such a separation is not possible, the state is entangled.

3.2 Example: Separable State

Consider

∣𝜓⟩= (1/root2)\*​(∣0⟩+∣1⟩)⊗∣0⟩=(1/root2)\*​(∣00⟩+∣10⟩).

This state can easily be separated into two independent qubits, so it is not entangled.

3.3 Example: Entangled State

Now consider

∣𝜓⟩=(1/root2)\*(∣00⟩+∣11⟩).

This state cannot be broken down into two single-qubit states.  
Measuring the first qubit instantly determines the state of the second: if the first is ∣0⟩, the second will also be ∣0⟩; if the first is ∣1⟩, the second will be ∣1⟩.  
These correlations cannot be explained by classical means.

3.4 Importance of Entanglement

* It provides the non-local connections that set quantum mechanics apart from classical physics.  
* It serves as a resource in quantum information theory.  
* It enables key protocols:  
* Quantum teleportation (transmitting unknown states using entanglement and classical communication).  
* Superdense coding (sending two classical bits with one qubit).  
* Quantum cryptography (secure communication based on entangled pairs).

4\. Bell States

The Bell states are a unique set of maximally entangled two-qubit states. They create an orthonormal <!-- how would this make sense without the vectorial intuition --> basis for the two-qubit Hilbert space and play a key role in quantum information science.

4.1 The Four Bell States    
∣Φ+⟩ \= 1/√2 (∣00⟩ \+ ∣11⟩),    
∣Φ−⟩ \= 1/√2 (∣00⟩ − ∣11⟩)    
∣Ψ+⟩ \= 1/√2 (∣01⟩ \+ ∣10⟩),    
∣Ψ−⟩ \= 1/√2 (∣01⟩ − ∣10⟩)  

Each of these states shows perfect correlations or anti-correlations <!-- NOTE: was correlation discussed? --> between the two qubits, depending on the measurement basis.

4.2 Construction of a Bell State  

Bell states can be created using simple quantum gates.

Example (constructing ∣Φ+⟩):  

Start with ∣00⟩.  

Apply the Hadamard gate H on the first qubit:    
(H ⊗ I)∣00⟩ \= 1/√2 (∣00⟩ \+ ∣10⟩).  

Next, apply CNOT with the first qubit as control and the second as target:    
CNOT(1/√2 (∣00⟩ \+ ∣10⟩)) \= 1/√2 (∣00⟩ \+ ∣11⟩) \= ∣Φ+⟩.  

This process shows that entanglement can be created from initially separable qubits.

4.3 Applications of Bell States  

Quantum teleportation: Transferring an unknown qubit state over a distance using entanglement.  

Superdense coding: Sending two classical bits of information with just one qubit.  

Bell test experiments: Testing the violation of classical locality and supporting the predictions of quantum mechanics.  

Quantum cryptography: Providing secure communication channels.  

# **Chapter 3 : Quantum Gates and its Matrix Form**

Every time you use a classical computer, whether to send an email, play a game, or read this article, it is performing an incredible number of complex tasks. Yet, all this complexity is built from remarkably simple components. At their core, classical computers operate using fundamental building blocks called logic gates (like AND, OR, and NOT) that manipulate classical bits

In the same way, quantum computers have their own fundamental building blocks: quantum gates. These gates, however, operate not on bits, but on qubits, the quantum equivalent of a classical bit. By manipulating qubits, these gates unlock the powerful phenomena of the quantum world, such as superposition and entanglement, to perform computations.

Interesting Fact \- Have you ever wondered can we reverse the classical gates. Take the `AND` gate for example, If after applying gate, I get a `0` then can I know for sure are original bits were (0,0) or (0,1) or (1,0). No right ? I can not be sure. But In case of `NOT` gate I am sure... <!-- TODO: rewrite --> 

But in quantum world, gates must be reversible i.e I can obtain original qubit from result. But why is this? Are gates made in such way? So answer is it is a mathematical necessity. As Ranco will say from 3 idiots would say \- Quantum ki duniya mei intuition ke peche mat bhago, maths ka peecha karo, sare jawab jhak marke khud tumhare peeche ayenge…. I mean only maths can answers our questions as maths is language of this world.

So lets dive into how quantum gates can be modeled in form of matrices and therefore their inverse (conjugate transpose) can give us original qubit.

# **How can we apply Gates to Qubits**

Note \- Please Paste below code in latex for showing of all symbols and matrices: <!-- FIXME: what the actual fuck -->

—Code begins—  
\\documentclass{article}  
\\usepackage{amsmath}  
\\usepackage{amssymb}  
\\usepackage{geometry}  
\\geometry{a4paper, margin=1in}

\\begin{document}

\\section{Introduction}  
We use a state vector to represent a qubit. This is a column matrix that tells us the probability of the qubit being in a certain state.

\\section{1. Matrix Representation of a Qubit}  
Think of a qubit as a vector (an arrow) in space. We usually describe it using two notations: \\textbf{Dirac Notation} (bra-ket) and \\textbf{Matrix Notation}.

\\subsection{The Basics}  
A single qubit is represented by a "state vector" $|\\psi\\rangle$. It is a combination of two base states:  
\\begin{itemize}  
    \\item $|0\\rangle$: The "Ground" state (like Heads)  
    \\item $|1\\rangle$: The "Excited" state (like Tails)  
\\end{itemize}

\\subsection{From Ket to Matrix}  
To do math with computers, we turn these symbols into column vectors (matrices).

\\\[  
|0\\rangle \= \\begin{bmatrix} 1 \\\\ 0 \\end{bmatrix} \\quad \\text{and} \\quad |1\\rangle \= \\begin{bmatrix} 0 \\\\ 1 \\end{bmatrix}  
\\\]

If we have a qubit in a superposition (a mix of 0 and 1), we write it as:  
\\\[  
|\\psi\\rangle \= \\alpha|0\\rangle \+ \\beta|1\\rangle \\quad \\rightarrow \\quad \\begin{bmatrix} \\alpha \\\\ \\beta \\end{bmatrix}  
\\\]  
Here, $\\alpha$ and $\\beta$ are complex numbers that tell us the probability of finding the qubit in state 0 or 1\.

\\section{2. How Can We Apply Gates to Qubits?}  
In classical computers, logic gates (like AND, OR, NOT) change bits. in Quantum computers, \\textbf{Quantum Gates} change the state vector of a qubit.

Mathematically, a gate is just a \\textbf{Matrix}. When we "apply" a gate, we are simply performing \\textbf{Matrix Multiplication}.

\\section{3. Applying Gates: Two Ways}  
Lets understand via an example... Take \\textbf{X-Gate} (the Quantum NOT gate). It is similar to classical not gate. It flips $|0\\rangle$ to $|1\\rangle$ and vice-versa.

\\subsection{The Matrix Way (Linear Algebra)}  
The X-Gate is represented by this matrix:  
\\\[  
X \= \\begin{bmatrix} 0 & 1 \\\\ 1 & 0 \\end{bmatrix}  
\\\]

To apply the X-gate to the $|0\\rangle$ state, we multiply the matrix by the vector:  
\\\[  
X|0\\rangle \= \\begin{bmatrix} 0 & 1 \\\\ 1 & 0 \\end{bmatrix} \\begin{bmatrix} 1 \\\\ 0 \\end{bmatrix} \= \\begin{bmatrix} (0\\cdot1) \+ (1\\cdot0) \\\\ (1\\cdot1) \+ (0\\cdot0) \\end{bmatrix} \= \\begin{bmatrix} 0 \\\\ 1 \\end{bmatrix} \= |1\\rangle  
\\\]  
\\textit{Result: The state flipped from 0 to 1\!}

\\subsection{The Psi Way (Dirac Notation)}  
Sometimes it is easier to use algebra instead of full matrices. We know that $X$ swaps the coefficients of $|0\\rangle$ and $|1\\rangle$.

If our state is $|\\psi\\rangle \= \\alpha|0\\rangle \+ \\beta|1\\rangle$:  
\\\[  
X|\\psi\\rangle \= X(\\alpha|0\\rangle \+ \\beta|1\\rangle)  
\\\]  
Beauty is that we can apply $X$ (or any other gate) individually to both $\\alpha$ and $\\beta$ coefficients independent of each other:  
\\\[  
\= \\alpha(X|0\\rangle) \+ \\beta(X|1\\rangle)  
\\\]  
We do this because we know on applying gate to $|0\\rangle$ will give $X|1\\rangle$ and vice versa.  
Knowing that $X|0\\rangle \= |1\\rangle$ and $X|1\\rangle \= |0\\rangle$, we get:  
\\\[  
\= \\alpha|1\\rangle \+ \\beta|0\\rangle  
\\\]  
\\textit{Result: The coefficients $\\alpha$ and $\\beta$ have swapped places.}

\\section{Summary}  
\\begin{enumerate}  
    \\item \\textbf{Qubit:} A column vector $\\begin{bmatrix} \\alpha \\\\ \\beta \\end{bmatrix}$.  
    \\item \\textbf{Gate:} A $2 \\times 2$ matrix (e.g., $X, Z, H$).  
    \\item \\textbf{Action:} Matrix Multiplication (Gate $\\times$ Qubit).  
\\end{enumerate}

\\end{document}

—Code ends—

# Chapter 4 : **Operations On Qubit**

# 

Copy this code in latex-  
\\documentclass{article}  
\\usepackage{amsmath}  
\\usepackage{amssymb}  
\\usepackage{geometry}  
\\usepackage{xcolor}  
\\usepackage{tcolorbox}

\\begin{document}

\\section{Introduction}  
Now that we can define a qubit, we need to perform mathematical operations on it. In this chapter, we explore how to compare qubits, combine them, and measure them.

\\section{1. The Dot Product (Inner Product)}  
In classical geometry, the dot product tells us the angle between two lines. In Quantum Computing, we call this the \\textbf{Inner Product}. It calculates the "overlap" between two quantum states.

\\begin{tcolorbox}\[colback=blue\!5\!white,colframe=blue\!75\!black,title=The Bra-Ket Rule\]  
To take the inner product of state $|\\phi\\rangle$ and state $|\\psi\\rangle$, we turn the first one into a row vector (a "Bra" $\\langle \\phi |$) and multiply it by the column vector (a "Ket" $|\\psi\\rangle$).  
\\end{tcolorbox}

\\subsection\*{The Math}  
If $|\\phi\\rangle \= \\begin{bmatrix} a \\\\ b \\end{bmatrix}$ and $|\\psi\\rangle \= \\begin{bmatrix} c \\\\ d \\end{bmatrix}$:  
\\begin{enumerate}  
    \\item Convert $|\\phi\\rangle$ to $\\langle \\phi|$. This involves taking the \\textbf{Conjugate Transpose} (turn column to row, and flip signs of imaginary numbers).  
    \\\[ \\langle \\phi | \= \\begin{bmatrix} a^\* & b^\* \\end{bmatrix} \\\]  
    \\item Multiply:  
    \\\[ \\langle \\phi | \\psi \\rangle \= \\begin{bmatrix} a^\* & b^\* \\end{bmatrix} \\begin{bmatrix} c \\\\ d \\end{bmatrix} \= (a^\* \\cdot c) \+ (b^\* \\cdot d) \\\]  
\\end{enumerate}

\\textbf{Why do we care?}  
If $\\langle \\psi | \\psi \\rangle \= 1$, the probabilities add up to 100\\% (Normalized).  
If $\\langle \\phi | \\psi \\rangle \= 0$, the states are totally distinct (Orthogonal).

\\section{2. The Tensor Product ($\\otimes$)}  
The Inner product made things smaller (result was a number). The \\textbf{Tensor Product} makes things bigger. This is how we represent \\textbf{two or more qubits} at once.

\\begin{tcolorbox}\[colback=red\!5\!white,colframe=red\!75\!black,title=The Expansion Rule\]  
If you have a 2-qubit system, the total state is the tensor product of the individual states. The size of the vector grows from 2 to 4\.  
\\end{tcolorbox}

\\subsection\*{The Math}  
Let Qubit A be $\\begin{bmatrix} a \\\\ b \\end{bmatrix}$ and Qubit B be $\\begin{bmatrix} c \\\\ d \\end{bmatrix}$.  
\\\[  
A \\otimes B \= \\begin{bmatrix} a \\cdot \\begin{bmatrix} c \\\\ d \\end{bmatrix} \\\\ b \\cdot \\begin{bmatrix} c \\\\ d \\end{bmatrix} \\end{bmatrix} \= \\begin{bmatrix} a \\cdot c \\\\ a \\cdot d \\\\ b \\cdot c \\\\ b \\cdot d \\end{bmatrix}  
\\\]  
This resulting 4D vector represents the probabilities of the states 00, 01, 10, and 11\.

\\section{3. Measurement and Probability}  
In the quantum world, we cannot "see" the vector $\\begin{bmatrix} \\alpha \\\\ \\beta \\end{bmatrix}$ directly. We can only "measure" it.

\\subsection{Probability of a Basis State}  
A qubit is usually in a superposition $|\\psi\\rangle \= \\alpha|0\\rangle \+ \\beta|1\\rangle$.  
When we measure it, the universe "rolls the dice."

\\begin{itemize}  
    \\item \\textbf{Question:} What is the chance I see a 0?  
    \\item \\textbf{Answer:} It is the magnitude of $\\alpha$ squared ($|\\alpha|^2$).  
    \\item \\textbf{Question:} What is the chance I see a 1?  
    \\item \\textbf{Answer:} It is the magnitude of $\\beta$ squared ($|\\beta|^2$).  
\\end{itemize}

\\subsection{The Measurement Collapse}  
This is the most unique part of quantum mechanics. Before measurement, the qubit is in both states (superposition). \\textbf{After} measurement, the superposition is destroyed.

\\\[  
|\\psi\\rangle \= \\alpha|0\\rangle \+ \\beta|1\\rangle \\xrightarrow{\\text{Measure}} \\text{Either } |0\\rangle \\text{ OR } |1\\rangle  
\\\]

If you measure a $|0\\rangle$, the new state becomes purely:  
\\\[  
|\\psi\_{new}\\rangle \= \\begin{bmatrix} 1 \\\\ 0 \\end{bmatrix}  
\\\]  
The $\\beta$ component vanishes entirely. You cannot "undo" a measurement.

\\end{document}

# **Chapter 5 : Multiple Qubit Systems and their maths**

Enter this code in latex \-   
\\documentclass\[11pt, a4paper\]{article}  
\\usepackage\[utf8\]{inputenc}  
\\usepackage{geometry}  
\\usepackage{amsmath, amssymb, amsthm}  
\\usepackage{physics}  
\\usepackage{xcolor}  
\\usepackage{tcolorbox}  
\\usepackage{parskip}   
\\usepackage{hyperref}

\\begin{document}

\\section{Introduction to Multiple Qubits}

In a single qubit system, we deal with a 2-dimensional space spanned by $\\ket{0}$ and $\\ket{1}$. However, real quantum computing power arises when we combine multiple qubits.

\\begin{tcolorbox}\[title=Key Concept: The State Space\]  
    If you have $n$ qubits, the size of your vector space grows exponentially.  
    \\begin{itemize}  
        \\item 1 Qubit: $2^1 \= 2$ states ($\\ket{0}, \\ket{1}$)  
        \\item 2 Qubits: $2^2 \= 4$ states ($\\ket{00}, \\ket{01}, \\ket{10}, \\ket{11}$)  
        \\item 3 Qubits: $2^3 \= 8$ states  
    \\end{itemize}  
    Generally, for $n$ qubits, we have $2^n$ basis states.  
\\end{tcolorbox}

% \-------------------------------------------------------------------

\\section{Constructing the Composite State ($\\Psi$)}

\\subsection{How do we get $\\Psi$ for multiple qubits?}

To describe two separate qubits as a single system, we use a mathematical operation called the \\textbf{Tensor Product}, denoted by the symbol $\\otimes$.

If Qubit A is in state $\\ket{\\psi\_A}$ and Qubit B is in state $\\ket{\\psi\_B}$, the combined state $\\ket{\\Psi}$ is:  
\\begin{equation}  
    \\ket{\\Psi} \= \\ket{\\psi\_A} \\otimes \\ket{\\psi\_B}  
\\end{equation}

Often, we simplify the notation:  
\\\[  
    \\ket{0} \\otimes \\ket{1} \\equiv \\ket{0}\\ket{1} \\equiv \\ket{01}  
\\\]

\\subsection{Example: Tensor Product of Basis States}  
Let's see how the standard basis states for a 2-qubit system are formed:  
\\begin{itemize}  
    \\item $\\ket{0} \\otimes \\ket{0} \= \\ket{00}$  
    \\item $\\ket{0} \\otimes \\ket{1} \= \\ket{01}$  
    \\item $\\ket{1} \\otimes \\ket{0} \= \\ket{10}$  
    \\item $\\ket{1} \\otimes \\ket{1} \= \\ket{11}$  
\\end{itemize}

A general 2-qubit state is a \\textbf{superposition} of all these combinations:  
\\begin{equation}  
    \\ket{\\Psi} \= \\alpha\_{00}\\ket{00} \+ \\alpha\_{01}\\ket{01} \+ \\alpha\_{10}\\ket{10} \+ \\alpha\_{11}\\ket{11}  
\\end{equation}  
Where the probabilities must sum to 1: $|\\alpha\_{00}|^2 \+ |\\alpha\_{01}|^2 \+ |\\alpha\_{10}|^2 \+ |\\alpha\_{11}|^2 \= 1$.

% \-------------------------------------------------------------------

\\section{$\\Psi$ and Matrix Representation}

While Dirac notation ($\\ket{\\Psi}$) is great for algebra, linear algebra uses column vectors. 

\\subsection{The Vector Form}  
For a single qubit:  
\\\[  
\\ket{0} \= \\begin{pmatrix} 1 \\\\ 0 \\end{pmatrix}, \\quad \\ket{1} \= \\begin{pmatrix} 0 \\\\ 1 \\end{pmatrix}  
\\\]

For two qubits, we calculate the tensor product of the vectors. Let's find the vector for $\\ket{01}$ (which is $\\ket{0} \\otimes \\ket{1}$):

\\begin{equation}  
    \\ket{0} \\otimes \\ket{1} \= \\begin{pmatrix} 1 \\\\ 0 \\end{pmatrix} \\otimes \\begin{pmatrix} 0 \\\\ 1 \\end{pmatrix} \=   
    \\begin{pmatrix}   
        1 \\cdot \\begin{pmatrix} 0 \\\\ 1 \\end{pmatrix} \\\\   
        0 \\cdot \\begin{pmatrix} 0 \\\\ 1 \\end{pmatrix}   
    \\end{pmatrix}   
    \= \\begin{pmatrix} 0 \\\\ 1 \\\\ 0 \\\\ 0 \\end{pmatrix}  
\\end{equation}

\\begin{tcolorbox}\[title=The 4 Basis Vectors\]  
    The basis vectors for a 2-qubit system are:  
    \\\[  
    \\ket{00} \= \\begin{pmatrix} 1\\\\0\\\\0\\\\0 \\end{pmatrix}, \\quad  
    \\ket{01} \= \\begin{pmatrix} 0\\\\1\\\\0\\\\0 \\end{pmatrix}, \\quad  
    \\ket{10} \= \\begin{pmatrix} 0\\\\0\\\\1\\\\0 \\end{pmatrix}, \\quad  
    \\ket{11} \= \\begin{pmatrix} 0\\\\0\\\\0\\\\1 \\end{pmatrix}  
    \\\]  
\\end{tcolorbox}

% \-------------------------------------------------------------------

\\section{Operations on Multiple Qubits}

Operations are represented by Unitary Matrices. If the state vector has size $2^n \\times 1$, the gate matrix must be size $2^n \\times 2^n$.

\\subsection{Single Qubit Gates on Multi-Qubit Systems}  
If we apply a Hadamard gate ($H$) to the first qubit and do nothing (Identity $I$) to the second, the operator is $H \\otimes I$.

\\\[  
    (H \\otimes I) \\ket{00} \= (H\\ket{0}) \\otimes (I\\ket{0}) \= \\ket{+} \\otimes \\ket{0} \= \\ket{+0}  
\\\]

\\subsection{Multi-Qubit Gates (The CNOT)}  
The most famous multi-qubit operation is the \\textbf{Controlled-NOT (CNOT)}.   
\\begin{itemize}  
    \\item \\textbf{Control Qubit:} The first qubit.  
    \\item \\textbf{Target Qubit:} The second qubit.  
\\end{itemize}  
\\textit{Logic:} If the control is $\\ket{1}$, flip the target. If the control is $\\ket{0}$, do nothing.

\\\[  
    \\text{CNOT} \\ket{00} \\to \\ket{00} \\quad \\text{CNOT} \\ket{10} \\to \\ket{11}  
\\\]

% \-------------------------------------------------------------------

\\section{Special Cases: Entanglement}

This is the heart of quantum mechanics.

\\subsection{Product States vs. Entangled States}

\\begin{tcolorbox}\[title=Product States\]  
    A state is a \\textbf{Product State} if it can be written as:  
    \\\[ \\ket{\\Psi} \= \\ket{\\psi\_{first}} \\otimes \\ket{\\psi\_{second}} \\\]  
    This means the two qubits are independent. Measuring one tells you nothing about the other.  
\\end{tcolorbox}

\\begin{tcolorbox}\[title=Entangled States, colframe=red\!75\!black\]  
    A state is \\textbf{Entangled} if it \\textbf{cannot} be factored into two separate qubit states.  
    \\\[ \\ket{\\Psi} \\neq \\ket{\\psi\_{first}} \\otimes \\ket{\\psi\_{second}} \\\]  
    The qubits lose their individual identity and can only be described as a single unit.  
\\end{tcolorbox}

\\subsection{The Bell States}  
The Bell states are the four maximally entangled two-qubit states. They are the "Hello World" of entanglement.

\\begin{enumerate}  
    \\item \\textbf{The Phi Plus ($\\ket{\\Phi^+}$):}  
    \\\[ \\ket{\\Phi^+} \= \\frac{\\ket{00} \+ \\ket{11}}{\\sqrt{2}} \\\]  
    \\textit{Explanation:} When you measure the first qubit, if you get 0, the second \\textbf{must} be 0\. If you get 1, the second \\textbf{must} be 1\. Perfect correlation.

    \\item \\textbf{The Phi Minus ($\\ket{\\Phi^-}$):}  
    \\\[ \\ket{\\Phi^-} \= \\frac{\\ket{00} \- \\ket{11}}{\\sqrt{2}} \\\]

    \\item \\textbf{The Psi Plus ($\\ket{\\Psi^+}$):}  
    \\\[ \\ket{\\Psi^+} \= \\frac{\\ket{01} \+ \\ket{10}}{\\sqrt{2}} \\\]  
    \\textit{Explanation:} The results are always opposite (01 or 10).  
      
    \\item \\textbf{The Psi Minus ($\\ket{\\Psi^-}$):}  
    \\\[ \\ket{\\Psi^-} \= \\frac{\\ket{01} \- \\ket{10}}{\\sqrt{2}} \\\]  
\\end{enumerate}

\\end{document}

The End—

