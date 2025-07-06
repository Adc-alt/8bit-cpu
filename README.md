# 🧠 8-bit CPU from Scratch
**Inspired by Ben Eater’s 8-bit computer, built from the ground up with curiosity, mistakes, and learning along the way.**

![8bits_computer](8bits_image.jpeg)

---

## 📋 Table of Contents

1. [💡 Motivation](#💡-motivation)  
2. [🔨 Project Phases](#🔨-project-phases)  
3. [🐞 Errors & Decisions](#🐞-errors--decisions)  
4. [🧩 Technical Chapters](#🧩-technical-chapters)  
5. [🎓 What I Learned](#🎓-what-i-learned)  
6. [▶️ How to Use / Run It](#▶️-how-to-use--run-it)

---

## 💡 Motivation

I wanted to take on a challenging project that would push me to truly learn electronics, not just in theory, but by getting hands-on with real components. At the same time, I was curious to deeply understand one of the most fundamental processes behind everything we interact with daily: low-level computer processing.

Even though we don’t deal with it directly, every app, video, or piece of software we use relies on that invisible layer of computation happening behind the scenes. Gaining a real grasp of how that works was my goal.

During my search, I came across a well-known figure on the internet: **Ben Eater**. His step-by-step videos on how to build an 8-bit computer from scratch were the perfect starting point. I decided to follow his guidance, replicate the machine, and document my process, not just to copy it, but to truly understand, modify, and build upon it.

---

## 🔨 Project Phases

1. **Design and planning**  
2. **Physical construction (breadboard setup)**  
3. **EEPROM programming**  
4. **Microcode development**  
5. **Custom instruction implementation**  
6. **Debugging and iteration**

---

## 🐞 Errors & Decisions

I ran into a lot of errors during this project. Honestly, way more than I would’ve liked. A lot. And when I say a lot, I mean a lot.

One of the biggest challenges was dealing with voltage spikes, those sudden jumps that happen when pressing buttons or switching RAM chips. I also had issues with the power supply voltage. All of the chips I used are TTL logic, which are supposed to work at a specific voltage range. But at higher voltages, spikes become more frequent, and they can completely throw off the logic, making the circuit behave unexpectedly.

To deal with this, I had to add lots of capacitors to smooth out signals and reduce noise. I also used RC filters to stabilize things.

There were also programming issues with the EEPROM, accidental component damage, bad wiring, and pretty much every kind of mistake you can think of.

But here’s the thing: none of that really matters, what matters is that every mistake taught me something, and eventually, I was able to fix it. That’s what this project is about.

---

## 🧩 Technical Chapters

### 1️⃣ RAM
![RAM module testing](Ram_module_testing.jpeg)



This image shows the RAM module during testing. I had to deal with noisy signals and used RC filters and capacitors to stabilize it. This was one of the most sensitive parts due to voltage spikes and data instability.

---

### 2️⃣ REGISTER

![Register module testing](Register_module_testing.jpeg)

This image reflects part of the register and control section involved in microcode execution. I structured the micro-instructions to manage control lines and ensured the fetch-decode-execute cycle was handled correctly, including adding custom instructions.

---

### 3️⃣ ALU
![ALU module wiring](Alu_module_wiring.jpeg)


This is the ALU (Arithmetic Logic Unit) section. It was critical for operations like addition, subtraction, and logical comparisons. Here I learned a lot about binary arithmetic and how to combine logic gates for operations.

---


## 🎓 What I Learned

🔌 Reverse polarity matters.
I learned that reverse polarity can destroy components, either by damaging internal transistors, diodes, or by allowing current to flow in the wrong direction. In this particular build, I didn’t implement protection for it, but it’s definitely something to consider in future designs.

⚡ How TTL logic works.
I now understand the precise voltage thresholds that define a 0 or a 1 in TTL logic. I also learned why TTL was eventually replaced by CMOS, which is far more power-efficient. At peak load, my computer was drawing up to 1.5A , though that’s partly because of all the LEDs I added.

📖 Datasheets are your best friend.
I learned to study datasheets carefully and thoroughly. They’re not just optional—they’re your final authority. You can honestly learn a ton just by reading Texas Instruments datasheets in depth.

🧰 The value of RC filters and decoupling capacitors.
Voltage spikes can cause false signals and unstable logic. I saw firsthand how RC filters and capacitors can smooth out those glitches and help keep the circuit stable.

🧠 Low-level computer architecture.
I gained a solid understanding of how a computer works at the lowest level: fetching an instruction from memory, decoding it, activating the appropriate control lines, and finally performing the operation to produce a result.


##🎥 Demo Video Summary
You can watch a 3-part video demo of the project on LinkedIn.

Here’s a brief summary of each part:

🧠 Part 1 – Human CPU Mode
In the first clip, the CPU wasn’t fully built yet — so I acted as the CPU myself. I manually toggled the control lines: first loading a 1 into Register A, then a 1 into Register B, and finally triggering the sum via the ALU. Then I inverted the ALU signal to perform a subtraction instead of an addition (2 -).

⚙️ Part 2 – Programmed Addition
The second video shows the CPU performing an addition fully on its own, programmed via the EEPROM. Register A loads the value 28, Register B gets 41, and the result 69 is shown. Everything happens at a slow clock speed so you can clearly see the operation step-by-step.

💻 Part 3 – It Becomes a Real Computer
In the final video, the system reaches a key milestone: it becomes Turing Complete. As defined by the father of computer science, a machine is considered a computer when it supports conditional jumps — and that’s exactly what’s shown here.

The program sums +15 repeatedly. Once an overflow occurs and the max value is reached, a conditional jump is triggered and the system switches to subtraction mode — all based on the program logic.


