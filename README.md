# Password Based Room Security and Automation System

---

## Introduction

The Password Based Room Security and Automation System combines access control and home automation. It provides secure access to a room while also controlling electronic devices like light and AC through a password-protected logic system.

## Table of Contents
- [Introduction](#introduction)
- [Description of the Project](#description-of-the-project)
- [Components Required](#components-required)
- [Circuit Design and Explanation](#circuit-design-and-explanation)
- [Simulation Result](#simulation-result)
- [Project Picture](#project-picture)
- [Application Areas and Limitations ](#application-areas-and-limitations)
- [Conclusion](#conclusion)

## Description of the Project

This project includes a keypad for password input, a door locking system, a buzzer alarm, and logic-based control of devices like bulb and AC. The system uses logic gates to check if the password is correct. A JK flip-flop counter is used to count wrong attempts, and an alarm is triggered if a set limit is crossed. The light and AC turn on only if the correct password is entered.

## Components Required

| Type | Component Name |
|------|----------------|
| Digital | 2-input 74LS266 XNOR IC |
|        | 3-input 74LS11 AND IC |
|        | 2-input 74LS08 AND IC |
|        | 2-input 74LS32 OR IC |
|        | 74LS04 NOT IC |
|        | 7476 JK Flip-Flop |
|        | 555 Timer IC |
|        | 4511 BCD to 7-segment Latch/Decoder/Driver |
|        | Dip Switches |
| Analog | Capacitors (1nF, 10μF) |
|        | Resistors (10kΩ, 100kΩ) |
|        | BC547 BJT |
|        | 1N4007 Diode |
| Additional | Buzzer |
|           | Battery |

## Circuit Design and Explanation
<p align="center">
  <img src="https://github.com/user-attachments/assets/599b82ae-de40-44c5-988d-6e8cac76bce3" width="400">
</p>

Step 1: Input Equality Check  
- We used XNOR gates to compare each digit of the 6-digit password with the correct one.  
- If all match, the output is HIGH, allowing access.

Step 2: Counter using JK Flip-Flop  
- A counter is built using JK flip-flops to count the number of wrong attempts.  
- On the 7th wrong attempt, it triggers the alarm circuit.

Step 3: Alarm System  
- If the wrong password is entered 7 times, the alarm is activated using logic gates connected to the counter output.

Step 4: Conditional Control  
- Light and AC are connected using logic gates so they only turn on when the correct password is entered.


## Simulation Result

- When the correct password is entered, access is granted, and devices turn on.  
- For 2 wrong attempts, nothing happens but the counter increases.  
- On the 7th wrong attempt, the alarm activates.  
- The system works as expected in simulation.

<p align="center">
  <table align="center">
    <tr>
      <td><img src="https://github.com/user-attachments/assets/34a73616-b844-4d0d-82d7-8c91efb97464" width="300"></td>
      <td><img src="https://github.com/user-attachments/assets/6a9e3995-a3df-4928-8701-e41600bb2ea5" width="300"></td>
      <td><img src="https://github.com/user-attachments/assets/c7103958-42b7-4838-b71e-2dd1cd2e459a" width="300"></td>
    </tr>
    <tr align="center">
      <td><b>Fig 1: Password Match</b></td>
      <td><b>Fig 2: 2 Times Wrong Password</b></td>
      <td><b>Fig 3: 7th Time Wrong Password and Alarm</b></td>
    </tr>
  </table>
</p>


## Project Picture

<p align="center">
  <img src="https://github.com/user-attachments/assets/128d1eb9-fd85-4ad7-bdab-21b4ad072cac" width="400">
</p>

## Application Areas and Limitations

**Application Areas:**

- Can be used in home or office security systems.  
- Useful in labs or restricted areas where automation and access control are needed.

**Limitations:**

- Can be vulnerable to brute-force attempts without a lockout system.  
- Initial setup may be hard for non-technical users.  
- Fixed logic makes it hard to change password without hardware modification.

## Conclusion

The Password Based Room Security and Automation System is a useful small-scale project to understand digital logic design. It combines XNOR-based password matching, JK flip-flop counting, and logic-based automation. It’s a good example of combining security and device control using only basic digital and analog components.

---
