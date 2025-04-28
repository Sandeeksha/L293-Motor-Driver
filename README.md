# Motor Driver Circuit using L293D and 5V Regulator

This project contains the schematic and PCB for a **motor driver circuit** using an **L293D H-Bridge IC**, with a regulated 5V supply provided by a **7805 voltage regulator**.

Schematic Diagram: ![Screenshot 2025-04-28 153644](https://github.com/user-attachments/assets/997a055f-efd6-40d3-8bb9-6fd9ada5e5bd)


PCB Diagram: ![Screenshot 2025-04-28 193453](https://github.com/user-attachments/assets/67547160-0b5d-4b3f-84d8-459312b6099a)

 
3D View of Front Side PCB: ![Screenshot 2025-04-28 193543](https://github.com/user-attachments/assets/4c0036b4-1954-4edf-be32-08ee4d0255f9)


3D View of Back Side PCB:![Screenshot 2025-04-28 193709](https://github.com/user-attachments/assets/91ea5992-904d-4a1c-9f37-8239b341ef73)




## ⚙️ Circuit Description

- **Input Power:**
  - External voltage is supplied via connector `J2`.
  - The **7805 voltage regulator** (`U2`) regulates the voltage down to **5V** for logic operation and powering low-power peripherals.
- **Motor Driver (L293D):**
  - The `L293D` (`U1`) is a dual H-bridge motor driver IC used to drive two DC motors independently.
  - Control inputs for the motor driver are provided through connector `J1` (4-pin header).
- **Outputs:**
  - Motor outputs are available at connectors `J3` and `J4`, each controlling one motor.
- **Status Indication:**
  - An LED (`D1`) with a current-limiting resistor (`R1`) is used to indicate that the 5V regulated power is available.
- **Power Flags:**
  - `PWR_FLAG` symbols are added for validation to indicate power availability in schematic design tools.

## 🧩Components

| Reference | Component    | Description                     |
|:---------:|:-------------:|:-------------------------------:|
| U1        | L293D         | Dual H-Bridge Motor Driver IC    |
| U2        | 7805          | 5V Linear Voltage Regulator IC   |
| J1        | Header        | Motor Control Input Connector    |
| J2        | Screw Terminal| External Voltage Input Connector |
| J3, J4    | Screw Terminals| Motor Output Connectors         |
| R1        | Resistor      | LED Current Limiting Resistor    |
| D1        | LED           | Power Status Indicator          |

## 🚀 How It Works

1. External power is connected to the circuit through `J2`.
2. `U2` (7805) steps down the input voltage to 5V DC to power the logic circuitry.
3. Control signals (e.g., PWM, direction control) are provided to `J1`.
4. `U1` (L293D) uses these signals to drive two motors connected via `J3` and `J4`.
5. The LED (`D1`) lights up to indicate that 5V regulated power is available and the system is active.


 ## 🚀 How to Use

- Connect a DC input voltage to **J2**.
- Connect control signals (motor directions) to **J1**.
- Connect your DC motors to **J3** and **J4**.
- Power up and control your motors!

## 🛠️ License

This project is open-source and free to use.
