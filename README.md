# Branch Predictor Simulator

A C++ simulator of a **history-based branch predictor**, written for a Computer Organization course (Spring 2022).

- Reads a sequence of branch outcomes (`T` = taken, `N` = not taken)
- Uses a **3-bit branch history** to select one of **8 predictors**
- Each predictor is an **8-state saturating counter**: SN → WN1–WN3 → WT1–WT3 → ST
- At every step it prints the current history, all 8 predictor states, the prediction, and the actual outcome

## Run
```bash
g++ -std=c++17 -o predictor 1093343prog2.cpp
echo "TNTTNNTT" | ./predictor
```
