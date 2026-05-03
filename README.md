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

### Embedded — 74HC595 Hex Counter with Button Control (Arduino)
A 7-segment display driven through a 74HC595 shift register. Two push buttons increment and decrement a hex counter (0–F), with binary state mirrored on 4 LEDs. Uses `shiftOut` and SPI-style control.

```cpp
byte seven_seg_digits[16] = {
  B11111100, // 0
  B01100000, // 1
  B11011010, // 2
  // ... 3–F
};

void sevenSegWrite(byte digit) {
  digitalWrite(latchPin, LOW);
  shiftOut(dataPin, clockPin, LSBFIRST, seven_seg_digits[digit]);
  digitalWrite(latchPin, HIGH);
}

void loop() {
  if (Serial.available()) {
    char input = Serial.read();
    if ((input >= '0' && input <= '9') || (input >= 'A' && input <= 'F')) {
      byte digit = (input <= '9') ? input - '0' : input - 'A' + 10;
      sevenSegWrite(digit);
    }
  }
}
```

---

### C++ — Grade Drop Calculator
Reads 5 grades, drops the lowest, and reports before/after averages. Demonstrates array passing by reference, function decomposition, and formatted output.

```cpp
void findDropInfo(double grades[], const int SIZE, int &lowest, double &average) {
  double total = 0;
  for (int i = 0; i < SIZE; i++) {
    if (grades[i] < grades[lowest]) lowest = i;
    total += grades[i];
  }
  average = (total - grades[lowest]) / (SIZE - 1);
}
```

---

### C++ — Dice Gambling Game
Console game with betting logic, random dice rolls, and input validation. Global funds state tracks wins/losses across rounds.

```cpp
int placeBet() {
  double amt;
  cout << "\nHow much would you like to bet?\n$";
  cin >> amt;
  while (amt > FUNDS) {
    cout << "ERROR: Invalid bet amount.";
    cout << "\nHow much would you like to bet?\n$";
    cin >> amt;
  }
  return amt;
}
```

---

### C++ — Employee Payroll Calculator
Computes weekly pay for N employees with validated hours (1–40), calculates company average. Uses separate functions for validation, calculation, and averaging.

```cpp
bool isValidHours(int hours) {
  return (hours > 0 && hours <= 40);
}

float calcPay(int hours, float payrate) {
  return hours * payrate;
}

float calcAveragePay(float totalpay, int n) {
  return totalpay / n;
}
```

---

## Projects

- **[VisionSystemAI for Industrial Process Flow](https://github.com/petem903/VisionSystemAIforIndustrialProcessFlow)** — OpenCV-based vision system to track restocks in industrial environments
- **[Line Following Robot](https://github.com/petem903/Line-Following-Robot)** — Autonomous robot with PID navigation; senior design capstone
- **[Portfolio](https://github.com/petem903/Portfolio)** — Industrial automation work from Yanfeng co-op

---

*Electrical Engineering @ UT Dallas · Co-op @ Yanfeng · Embedded systems + software*
