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

### 4️⃣ New Instructions

I added custom instructions like `NOP`, `INC`, and `JNZ`. These were manually programmed into the EEPROM and supported by microcode logic. For instance, `INC` increments the accumulator, and `JNZ` allows conditional jumps based on flags.

*(You can include more screenshots or animations here to show the instructions in action.)*

---

## 🎓 What I Learned

- How data moves across a shared bus  
- The role of registers, the ALU, and control logic  
- How to design instruction sets and build a functioning microarchitecture  
- That **debugging is a learning tool**, not just a problem to fix

---

## ▶️ How to Use / Run It

If you're using physical hardware, include photos or wiring instructions.  
If you're using a simulator (like Logisim), explain how to open and run the project.

---
"""

# Guardar el README traducido al inglés
english_readme_path = "/mnt/data/README_ENGLISH.md"
with open(english_readme_path, "w", encoding="utf-8") as f:
    f.write(readme_english)

english_readme_path
