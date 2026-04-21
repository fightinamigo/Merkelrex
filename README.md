# 💱 MerkelRex — Cryptocurrency Exchange Platform

A fully functional cryptocurrency exchange platform built in C++ as part of the **Object-Oriented Programming Specialization** by the University of London / Goldsmiths on Coursera (5-course series, Prof. Matthew Yee-King).

> Built incrementally across 5 courses, this project covers the full journey from basic C++ I/O all the way to a working order-matching engine with real trading data.

---

## 🚀 Features

- Interactive console menu system
- Order book management — place and track **bids** and **asks**
- **Order matching engine** — matches buy and sell orders by price
- CSV file parsing — reads real historical trading data
- Wallet system — tracks user balance and holdings
- Statistical analysis — min, max, and average price per product
- Exception handling for robust user input processing
- Multi-product support (e.g. ETH/BTC, DOGE/BTC)

---

## 🏗️ System Architecture

```
MerkelMain          → Top-level application controller, menu loop
OrderBook           → Manages all orders, provides query methods
OrderBookEntry      → Represents a single bid or ask order
OrderBookType       → Enum: bid / ask
Wallet              → Tracks user's currency holdings
CSVReader           → Parses trading data from CSV files
```

---

## 💡 C++ Concepts Demonstrated

| Concept | Where Used |
|---|---|
| Classes & Objects | `OrderBook`, `OrderBookEntry`, `Wallet`, `MerkelMain` |
| Static & Non-static Functions | Throughout all classes |
| File I/O | `CSVReader` parses real CSV trading data |
| Exception Handling | Input validation, file reading |
| Vectors & Iteration | Order book storage and matching algorithm |
| Enums | `OrderBookType` (bid/ask) |
| Algorithms | Price matching engine, statistical computations |
| Modular Design | Multi-file project with headers and source files |

---

## 🖥️ Menu Options

```
1. Print help
2. Print exchange stats
3. Make an ask (sell order)
4. Make a bid (buy order)
5. Print wallet
6. Continue to next time step
7. Exit
```

---

## 🛠️ Build & Run

**Requirements:** C++20, CMake, any C++ compiler (GCC, Clang, MSVC)

```bash
git clone https://github.com/fightinamigo/merkelrex
cd merkelrex
mkdir build && cd build
cmake ..
make
./MerkelRex
```

> Make sure the CSV data file is in the working directory when running.

---

## 📁 Project Structure

```
├── main.cpp               # Entry point
├── MerkelMain.h/.cpp      # Application controller & menu
├── OrderBook.h/.cpp       # Order book logic
├── OrderBookEntry.h/.cpp  # Single order model
├── OrderBookType.h        # Bid/Ask enum
├── Wallet.h/.cpp          # User wallet
├── CSVReader.h/.cpp       # CSV file parser
├── 20200317.csv           # Trading data file
└── CMakeLists.txt
```

---

## 📌 Notes

- Built as part of the [Object Oriented Programming Specialization](https://www.coursera.org/specializations/object-oriented-programming-s12n) by University of London on Coursera
- The matching engine processes time steps from real historical order book data
- The project was developed incrementally — each of the 5 courses added new functionality
