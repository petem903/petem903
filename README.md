# Pete Mathew

**Electrical Engineering student** with hands-on experience in embedded systems, C++, and scientific computing. I work across the full hardware-software stack — from writing firmware for microcontrollers to numerical analysis in Python.

---

## Skills

| Area | Tools / Languages |
|---|---|
| Embedded Systems | Arduino, C/C++, SPI, I²C, 74HC595, 7-segment displays, LCD |
| Systems Programming | C++ — structs, arrays, functions, OOP fundamentals |
| Scientific Computing | Python, NumPy, Jupyter Notebooks |
| Hardware | Circuits, Digital Logic, VLSI, Signals & Systems, Semiconductor Devices |
| Design Tools | KiCad, Multisim, Quartus |

---

## Code Samples

### Embedded — [74HC595 Hex Display Counter](https://gist.github.com/petem903/77b51a8d4f5c0913dc7f30c472ef9d7e) (Arduino)
A 7-segment display driven through a 74HC595 shift register via `shiftOut`. Reads hex characters (0–F) over Serial and maps them to segment bit patterns using a lookup table.

```cpp
const byte SEVEN_SEG[16] = {
  0b11111100,  // 0
  0b01100000,  // 1
  0b11011010,  // 2
  // ... 3–F
};

void sevenSegWrite(byte digit) {
  digitalWrite(LATCH_PIN, LOW);
  shiftOut(DATA_PIN, CLOCK_PIN, LSBFIRST, SEVEN_SEG[digit]);
  digitalWrite(LATCH_PIN, HIGH);
}
```

---

### C++ — [Grade Drop Calculator](https://gist.github.com/petem903/bd7e1259151010bb1c4cf502729f5489)
Reads 5 grades, drops the lowest, and reports before/after averages. Demonstrates array passing, function decomposition, and formatted output.

```cpp
int findLowest(const double grades[]) {
  int idx = 0;
  for (int i = 1; i < SIZE; i++)
    if (grades[i] < grades[idx]) idx = i;
  return idx;
}

double calcDropAverage(const double grades[], int dropIdx) {
  double total = 0;
  for (int i = 0; i < SIZE; i++) total += grades[i];
  return (total - grades[dropIdx]) / (SIZE - 1);
}
```

---

### C++ — [Dice Gambling Game](https://gist.github.com/petem903/00b9f3de1b9c3d2154bc350c20d64894)
Console game with betting logic, random dice rolls, and input validation. Tracks funds across rounds and ends when the player quits or goes broke.

```cpp
double placeBet() {
  double amt;
  cout << "How much would you like to bet? $";
  cin >> amt;
  while (amt <= 0 || amt > funds) {
    cout << "Invalid. Enter a bet between $1 and $" << funds << ": $";
    cin >> amt;
  }
  return amt;
}
```

---

### C++ — [Weekly Payroll Calculator](https://gist.github.com/petem903/5c9c573aba1984a8fc01ec73acc28901)
Computes weekly pay for N employees with validated hours (1–40) and prints the company average. Clean separation between validation, calculation, and output.

```cpp
bool isValidHours(int hours) { return hours >= 1 && hours <= 40; }
float calcPay(int hours, float rate) { return hours * rate; }
float calcAveragePay(float total, int n) { return total / n; }
```

---

## Projects

- **[VisionSystemAI for Industrial Process Flow](https://github.com/petem903/VisionSystemAIforIndustrialProcessFlow)** — OpenCV-based vision system to track restocks in industrial environments
- **[Line Following Robot](https://github.com/petem903/Line-Following-Robot)** — Autonomous robot with PID navigation; senior design capstone
- **[Portfolio](https://github.com/petem903/Portfolio)** — Industrial automation work from Yanfeng co-op

---

*Electrical Engineering @ UT Dallas · Co-op @ Yanfeng · Embedded systems + software*
