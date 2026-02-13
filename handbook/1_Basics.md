# The Basics

## Overview

Quantum Computing is an exciting and rapidly evolving field that lies at the intersection of physics, computer science, mathematics, and engineering. This handbook is to serve as a beginner-friendly yet structured guide for students who are curious about quantum computing and want a clear starting point.

Whether you are completely new or have some background, this guide aims to reduce the initial learning curve and help you navigate the vast quantum ecosystem.

---

## Contents

1. What is a Qubit?
2. What is a Python Library?
3. Using Git

---

# What is a Qubit?

## Engineering the Classical Bit

Storing information is not a trivial problem. Classical bits (simply *bits* or sometimes *cbit* in a quantum computing context) with their `1`s and `0`s seem obvious to us now, but thats because we have been exposed to them for decades as *the* way to store information in computers. Before we get to qubits, lets look at an engineer's perspective on why bits (binary units) were natural for computers as opposed to base-10 systems. 

Fundamentally, human beings used base-10 arithmetic, with 10 different digits (0 through 9) and place value representing powers of 10 (1, 10, 100, ...) for aeons. This is not exactly random: we have ten fingers, and ten digits thus becomes a natural rule to impose upon arithmetic. Of course, in the mathematician's lens, one where abstraction is paramount, the next step is to think about different ways of representing numbers. There are different bases, 2 (binary), 3(trinary), and entirely different systems like the p-adic systems.

> [!TIP]
> *(you can skip this)*
> 
> If you remember from school there was a not-so-rigorous *proof* that 0.999... = 1. The steps involved something like setting x = 0.999..., multiplying both sides by 10 to get 10x = 9.999..., subtracting x from both sides so 9x = 9, and thus x = 1. 
> 
> What if you tried doing that to ...999? 
> $$...99 = x$$
> $$...90 = 10x$$
> $$-9 = 9x$$
> $$x = -1$$
>
> This seems ridiculous, and is due to a subtle error (...999 is *not a number*), but forms the insight for the p-adic systems. Note that adding 1 to the infinite ...999 does give you zero. The *p* stands for prime. The 10-adic representation of numbers (e.g. ...999. for -1) fails to uphold that $a \times b = 0$ implies that either $a = 0$ or $b = 0$, but prime-adic systems do enforce that.

At this point, the first computer engineers had a wide variety of systems to choose from, but they also had three competing design considerations. Whatever system they chose, it needed to be: (1) intuitive, (2) reliable, and (3) expressive.

While base-10 arithmetic is the most familiar to us, base-10 had serious reliability issues. Consider a computer which represents digit by voltage, on a wire that runs between 0 to 5 Volts. Base-10 would imply that each digit occupies 0.5 Volts of bandwith, meaning a signal carrying the number 4 can easily be deflected by external noise and interference. This pushed engineers towards binary, where the digit tolerances were much wider. 

Binary was also extremely expressive since the architecture for binary could naturally be used for boolean arithmetic which was necessary for designing control flow programmatically. Additionally, the 2-adic system naturally represented negative numbers ($1 + ...111 = 0$) which is implemented in computers as 2's-complement. 

How does this tie into qubits? 

For the engineers designing current quantum computers, these same axes are important: (1) intuition, (2) reliability, and (3) expressiveness. While *qutrits* and *quduits* are being researched, *qubits* are the main focus of much of quantum computing research because quantum sytems with two orthogonal states are common and natural to think about:
- Electrons with spin-up and spin-down, $|\uparrow\rangle$, and $|\downarrow\rangle$
- The horizontal and vertical polarization of light $|H\rangle$, and $|V\rangle$
- Q = 0 and Q = 2e (cooper pair) in Josephson junctions $|0\rangle$ and $|1\rangle$

## The Computer Science of Qubits

What's the point though of going through the trouble of engineering these complex trapped ion-systems or superconducting junctions or optical quantum computers? Where does the advantage of qubits lie?

The most common answer you will receive is that qubits can exist in a superposition. That is partly the answer, but its not the whole story. *Lots* of things exhibit superposition. In fact, superposition is quite normal. Two ripples on a pond superpose; sound from multiple sources superpose at your ear (how does ANC work?); voltages in linear circuits. In fact, the most trivial example in maths might be some expression like

$$5 * (4 + 3)$$

Whether you compute $4 + 3$ or $20 + 15$ first, you get the same result, and its that kind of freedom that we're trying to exploit in quantum computing. What is neat about superposition in a quantum setting is that *discrete* states superpose. It allows you to write something like this

$$
\alpha|0\rangle + \beta|1\rangle
$$

The shear capacity of such a system to store information will be made obvious in just a moment. First lets adress $\alpha$ and $\beta$. The issue with having superpositions of discrete "incompatable" states is that when measuring these states, the superposition collapses. $|\alpha|^2$ and $|\beta|^2$ correspond to the probabilities of obtaining $|0\rangle$ and $|1\rangle$ respectively, with $\alpha, \beta \in \Complex$. The remarkable capacity of quantum computers to hold information comes from these coefficients. You can encode information in quantum computers via the bitstring itself $|0101\rangle = |5\rangle$, or in the coefficients via amplitude (which of $|\alpha|^2, |\beta|^2$, etc. are the largerst), or via phase ($\beta = e^{i\theta}\alpha$ implies same amplitude, but different kinds of interaction during processes). That is, each qubit, has *two real* degrees of freedom, since the normalisation constraint forces $\cos{\frac{\theta}{2}}|0\rangle + e^{i\phi}\sin{\frac{\theta}{2}} |1\rangle$. These coefficients in a sense have infinite resolution. While extracting that information via measurement is theoretically impossible, algorithms make use of their interaction before measurement to perform computation.

As you read further in our Handbook, the notation, the underlying physics, and the underlying algorithms will all become much more clearer as they are explained in depth. We don't expect you to catch every detail reading this right now, but keeping this in the back of your mind may help you reason about how one *thinks* while working with quantum algorithms.

# What is a Python Library?

## Wait, what's Python?

Python is *a* programming language. If you're new to programming languages, the thought of learning it might seem daunting, but it gets better with time. *This* section is not a guide towards how to write in Python, its more of an explanation as to why Python is being used in the first place. To the uninitiated, programming languages might all look the same, but each programming language exists for a reason: like all things, programming languages were *made* by people and their motivation was always that the current offerings are insufficient or flawed and that they can do better (see [xkcd-927](https://xkcd.com/927/)). Whether we're talking about C++, Python, Java, or Rust, each language was a response to what came before.

To understand the existence of Python itself, and why Python is so prevalent in quantum computing, we need to discuss some structural questions faced by anyone wanting to design a programming language. Fundamentally, it must be understood that computers are dumb machines doing sophisticated things. At the microstructural level, memory is constantly being assigned and reassigned and interpreted (everything is ones and zeroes: text looks like a number) and so programs need to provide computers with lots of information regarding what kind of data is being worked with, what kind of operation is being performed, where to-store-or-not-store information. Converseley, despite our sophistication, we're not well suited to the density of information that computers used to orchestrate themselves. We like things simplified and clear.

Therefore, there are two competing interests when designing a language: verbosity and clarity. This forms a spectrum from assembly to C to Python and beyond. 

If your goal is working with hardware or systems or brute performance, then languages like C++ or Rust are your go-tos. On the other hand, for people who might be working on Quantum Computing, who don't really care about memory management at the system level, then all this verbosity can be a massive headache and would impede your ability to effectively reason about your goals. Python is a language that lacks mandated typing, is interpreted, and is easy to read. Python is a language designed for high-level orchestration and uses both objected-oriented and functional programming techniques to its benefit in a natural way. 

You may not know what either object-oriented programming (OOP) or functional programming is, that's the point of Python: worry about your problem, not programming.

## And Libaries?

Python is of course, not the only programming language that is interpreted, lacks-typing, and human-readable. What Python has over its competitors is a massive and mature ecosystem of libraries. A library is generally user published-code that provides readymade systems to start programming with. This is not fundamentally a technical advantage of Python; its simply that an ecosystem developed early and attracted more people to grow itself - a positive feedback loop. 

This large ecosystem is why Python is so commonly used in so many different regimes. Its why general purpose machine learning tooling (`PyTorch`, `sci-kit`) exists on Python. Its why data analytics tooling (`Pandas`, `Numpy`, `matplotlib`, `seaborn`) exists on Python.

This is why quantum SDKs like Qiskit, PennyLane, and Cirq are exposed through Python — not because Python is fast, but because it is expressive, readable, and well-integrated with the broader scientific ecosystem. It allows them and you to tap into a wide range of tooling and prebuilt infrastructure without the headache of having to understand the fine details of them. For you, working with pennylane is as simple as `import pennylane as qml`. But under the hood `pennylane` is a massive collection of code written in other languages wired together using python into one seamless experience for you.

## Could I use other Languages?

Yes. While IBM and Google went to Python, Microsoft for example designed a *new* language from the groundup called `Q#` since they felt that the logic and mental thought processes behind quantum programming is fundamentally different from that used in other languages, and that the differences should be baked into the language used. 

Additionally, since Python is an interpreted language, it is also fundamentally slow. Thus, even libaries like `Qiskit` use Rust for performance-critical components and Python simply acts as an orchestration-layer.

As you learn more about quantum computing, you may or may not need to engage with the software surrounding algorithms in quantum computing. But, such designing such software is a real part of the industry, so general awareness should not be neglected and it produces one more avenue for a career in QC.



