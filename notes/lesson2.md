# Module 1 – How Computers Actually Work

## Lesson 2 – Binary, Bits, Bytes & How Computers Understand Everything

---

# 🎯 Goal

Build a mental model of how **all digital information**—text, images, videos, programs, AI models, and databases—is represented inside a computer.

---

# 📚 Learning Objectives

By the end of this lesson, you will be able to:

- Explain why computers use binary.
- Understand bits, bytes, KB, MB, GB, and TB.
- Convert simple decimal numbers to binary.
- Explain how text is stored.
- Understand how images and files are represented.
- Build an intuition for why binary matters in engineering.

---

# 💡 Why This Matters

Imagine you're building an AI chatbot.

The user asks:

> **"Hello"**

The AI responds:

> **"Hi! How can I help?"**

To us, that's just text.

To the computer?

It's simply **billions of electrical signals**.

Every:

- Character
- Pixel
- Sound
- Machine Learning Model
- Database
- Program

...is ultimately represented as **binary**.

---

# 🧠 First Principles

Let's begin with the most fundamental question.

## What is Electricity?

Electricity is the movement of electrons.

Inside your computer, billions of microscopic electronic circuits can exist in one of **two stable states**:

- ⚡ Electricity Flowing
- ❌ No Electricity

That's all.

There isn't a reliable "half-on" state for digital logic.

Because of this, engineers designed computers around **two stable electrical states**.

---

# 🔌 The Two States

We represent these electrical states as:

| Electrical State | Binary |
|------------------|--------|
| Electricity ON | **1** |
| Electricity OFF | **0** |

This is called **Binary**.

> **Important:** Computers didn't invent binary.

Binary is simply a convenient way to represent the physical behavior of electronic circuits.

---

# 💡 A Light Switch Analogy

Imagine a room with **one light switch**.

```text
OFF → 0

ON  → 1
```

Only **two possibilities** exist.

---

## Two Switches

```text
00
01
10
11
```

Total possibilities:

**4**

---

## Three Switches

```text
000
001
010
011
100
101
110
111
```

Total possibilities:

**8**

---

### Rule

Every additional **bit doubles** the number of possible values.

| Number of Bits | Possible Values |
|---------------:|----------------:|
| 1 | 2 |
| 2 | 4 |
| 3 | 8 |
| 4 | 16 |
| 8 | 256 |

---

# 🔹 What is a Bit?

A **Bit** (Binary Digit) is the **smallest unit of information**.

A bit stores exactly one value:

```text
0

or

1
```

Nothing else.

---

# 🔹 What is a Byte?

A **Byte** consists of:

> **8 Bits**

Example:

```text
01000001
```

This entire sequence is **one byte**.

A byte can represent:

```text
2⁸ = 256
```

different values.

Therefore, one byte can store numbers from:

```text
0 → 255
```

---

# 🤔 Why 8 Bits?

Historically, computers experimented with different word sizes.

Eventually, **8-bit bytes** became the industry standard because they efficiently represented:

- Text
- Numbers
- Memory

Today:

> **1 Byte = 8 Bits**

This is the universal standard.

---

# 👀 Visualizing a Byte

### Bit Positions

|7|6|5|4|3|2|1|0|
|-|-|-|-|-|-|-|-|
|0|1|0|0|0|0|0|1|

Each position represents a value.

|128|64|32|16|8|4|2|1|
|---|--|--|--|--|--|--|--|

---

## Example

Binary:

```text
01000001
```

Calculation:

```text
0 × 128 = 0

1 × 64 = 64

0 × 32 = 0

0 × 16 = 0

0 × 8 = 0

0 × 4 = 0

0 × 2 = 0

1 × 1 = 1
```

Total:

```text
64 + 1 = 65
```

Decimal:

```text
65
```

---

# 🔢 Decimal vs Binary

Humans use the **Decimal Number System**.

Why?

Because we have **ten fingers**.

Decimal digits:

```text
0
1
2
3
4
5
6
7
8
9
```

Computers use **Binary**.

Binary digits:

```text
0
1
```

---

# 🔄 Converting Decimal to Binary

| Decimal | Binary |
|---------:|:-------|
|0|00000000|
|1|00000001|
|2|00000010|
|3|00000011|
|4|00000100|
|5|00000101|
|6|00000110|
|7|00000111|
|8|00001000|

Notice the pattern?

Binary counts just like decimal—but using only **0** and **1**.

---

# 🔤 How Does a Computer Store the Letter "A"?

This surprises almost everyone.

The computer **doesn't store**:

```text
A
```

Instead, it stores a **number**.

According to the **ASCII** standard:

```text
A = 65
```

Now convert **65** into binary:

```text
01000001
```

So internally:

```text
A
   ↓
65
   ↓
01000001
   ↓
Electrical Signals
```

---

# 🔠 Other Characters

ASCII assigns numbers to every character.

Examples:

| Character | Decimal | Binary |
|-----------|--------:|:--------|
|A|65|01000001|
|B|66|01000010|
|C|67|01000011|
|D|68|01000100|

Even numbers are stored as character codes when written as text.

---

# 🌍 Unicode & UTF-8

ASCII worked well for English.

But what about:

```text
नमस्ते

你好

こんにちは

😊

🚀
```

ASCII couldn't represent all of these.

The solution was **Unicode**.

The most common encoding today is:

> **UTF-8**

UTF-8 can represent nearly every writing system and emoji used around the world.

---

# 🖼️ Images Are Also Binary

Imagine a tiny image.

```text
⬜⬛

⬛⬜
```

The computer doesn't store the picture.

It stores **numbers** for each pixel.

Example:

```text
255

0

0

255
```

Each number is converted into binary.

Millions of pixels together create a photograph.

---

# 🎥 Videos

A video is simply a rapid sequence of images.

```text
Frame 1

↓

Frame 2

↓

Frame 3

↓

Frame 4
```

Each frame is an image.

Each image consists of pixels.

Each pixel is represented by numbers.

Each number is stored in binary.

---

# 🤖 AI Models

Modern AI models contain **millions or even billions of parameters**.

Each parameter is stored as a number.

Each number is represented in binary.

Therefore, even the most advanced AI models are ultimately stored as sequences of bits.

---

# 💾 File Sizes

Since everything is stored in bytes, storage is measured using byte-based units.

| Unit | Value |
|------|------:|
|1 Byte|8 Bits|
|1 KB|1024 Bytes|
|1 MB|1024 KB|
|1 GB|1024 MB|
|1 TB|1024 GB|

---

# ❓ Why Isn't 1 KB Equal to 1000 Bytes?

Because computers count using powers of two.

```text
2¹⁰ = 1024
```

Traditional binary-based storage therefore uses **1024** instead of **1000**.

---

# 🚀 Why Does This Matter?

Suppose your AI application loads a:

> **7 GB Model**

That means approximately:

```text
7 × 1024 MB
```

of binary data must be loaded into RAM before the model can begin inference.

Understanding storage and memory becomes essential when working with:

- Large AI models
- Databases
- Distributed systems
- Cloud computing
- High-performance applications

---

# ❌ Common Misconceptions

### ❌ Binary is a programming language.

No.

Binary is simply a **number system**.

---

### ❌ Computers think in binary.

No.

Computers don't "think."

They manipulate electrical states represented using binary digits.

---

### ❌ Images are stored as pictures.

No.

Images are stored as binary data describing the color and intensity of pixels.

---

### ❌ AI understands language directly.

No.

Before AI models process language, text is converted into numbers (tokens and embeddings), which are then represented in binary.

---

# 📌 Key Takeaways

- Computers use **binary (0 and 1)** because electronic circuits have two stable states: ON and OFF.
- A **bit** is the smallest unit of information.
- A **byte** contains **8 bits** and can represent **256 different values**.
- Humans use the decimal system; computers use binary.
- Characters are stored as numbers using encoding standards like **ASCII** and **UTF-8**.
- Images, videos, audio, programs, and AI models are ultimately represented as binary data.
- Storage units are measured in bytes: **KB, MB, GB, and TB**.
- Understanding binary helps explain how computers store, process, and transmit all forms of digital information.