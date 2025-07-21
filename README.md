# Clocked SR Flip-Flop: Truth Table, Circuit Diagram, Working

![Status](https://img.shields.io/badge/status-active-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Maintained](https://img.shields.io/badge/maintained-yes-success)
![Platform](https://img.shields.io/badge/platform-Proteus-blue)

This repository contains supporting media (GIFs and images) for the article on **Clocked SR Flip-Flop**, a key digital electronics component used for data storage and control in synchronized circuits.

---

## 🔧 Overview

The **Clocked SR (Set-Reset) Flip-Flop** is an improved version of the SR latch. It includes a clock input, making it a **synchronous** circuit. The output only changes on the clock edge, helping avoid unwanted state changes.

---

## ⚙️ Inputs and Outputs

- **Inputs**:  
  - `S` (Set)  
  - `R` (Reset)  
  - `CLK` (Clock)

- **Outputs**:  
  - `Q` (Normal)  
  - `Q̅` (Inverted)

---

## 📊 Truth Table

| CLK | S | R | Q (Next State) | Description         |
|-----|---|---|----------------|---------------------|
|  0  | X | X | No Change      | Clock is LOW        |
|  1  | 0 | 0 | No Change      | Hold                |
|  1  | 1 | 0 | 1              | Set                 |
|  1  | 0 | 1 | 0              | Reset               |
|  1  | 1 | 1 | Invalid        | Forbidden State     |

---

## 🧪 Circuit Implementations

### NAND Gate Version
- Uses a basic SR latch made from NAND gates
- Clocked using two additional NAND gates

### NOR Gate Version
- Uses a basic SR latch made from NOR gates
- Clocked using two AND gates

---

## 🧠 Working Summary

- **When CLK = 0**: Inputs are ignored, output remains unchanged.
- **When CLK = 1**:  
  - `S = 1`, `R = 0` → Set  
  - `S = 0`, `R = 1` → Reset  
  - `S = 0`, `R = 0` → Hold  
  - `S = 1`, `R = 1` → Invalid

---

## 📁 Contents

This repository includes:
- GIF videos showing simulations of Clocked SR Flip-Flop using NAND and NOR gates
- Circuit diagrams and symbol illustrations

---

## 📌 Applications

- Digital memory registers
- Data synchronization
- Sequential state machines
- Timing-critical control logic

---

> ⚠️ Avoid using both Set and Reset HIGH when the Clock is active — it leads to an invalid state.
