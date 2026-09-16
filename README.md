# ATM Controller using Verilog HDL



---

## What is this project?

This project is a digital design of an **Automated Teller Machine (ATM)** made using **Verilog HDL**.

It works like a real ATM but is simulated on a computer. You can insert a card, enter a PIN, check balance, withdraw money, deposit money, and change the PIN.

## What does it do?

The ATM controller can:

- Accept a card  
- Check if the PIN is correct  
- Allow only 3 wrong PIN attempts (then lock the account temporarily)  
- Show balance  
- Withdraw cash (if enough balance is available)  
- Deposit cash  
- Change PIN  
- Eject the card after the transaction  

There are **3 accounts** already stored inside the design:

| Card Number | Default PIN | Starting Balance |
|-------------|-------------|------------------|
| a2b1        | 0001        | 2000             |
| a2b2        | 0010        | 1500             |
| a2b3        | 0011        | 4000             |

## How is it designed?

The entire ATM is made as one **Finite State Machine (FSM)**.

Main states are:
- Idle  
- Card Inserted  
- Enter PIN  
- Check PIN  
- Menu  
- Balance Inquiry  
- Withdraw  
- Deposit  
- PIN Change  
- Dispense Cash  
- Eject Card  

Everything happens step by step based on the current state.

## Files in this project

- `atm.v` → Main ATM design (the controller)  
- `atm_tb.v` → Testbench (used to test the design)  

## How to test it?

1. Open the project in any Verilog simulator (Vivado, ModelSim, etc.)  
2. Run the testbench (`atm_tb`)  
3. Look at the messages printed on the screen  
4. Check whether the balance values match the expected results  

## Why is this project useful?

This project helps you learn:

- How to design a complete system using Finite State Machine  
- How to handle multiple accounts  
- How to write a good testbench  
- How real machines like ATM work at the hardware level  

## Future Improvements

- Add more accounts using memory  
- Add PIN debounce for real keypad  
- Add daily withdrawal limit  
- Connect to real FPGA board with display and buttons  

---

**Project Type:** Digital System Design Laboratory  
**Language:** Verilog HDL  
**Design Style:** Finite State Machine (FSM)

**Author:** Gayatri Galidevara
