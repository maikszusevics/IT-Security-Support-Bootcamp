# Understanding Abstraction in Computing

## Bits and Binary: The Foundation

A **bit** is the smallest unit of data in computing. It can be:

- `1` (on / true)
- `0` (off / false)

In hardware, these states are represented by electrical signals, like 5V for `1` and 0V for `0`.

Eight bits make a **byte**, which can store values like characters or numbers.

## Boolean Logic & Logic Gates

Computers use **Boolean logic** to make decisions using simple rules:

- **AND**: True only if *both* inputs are True  
- **OR**: True if *either* input is True  
- **NOT**: Flips the value (True becomes False)

These are built using **logic gates** - physical components in circuits that process bits.

## Transistors: Hardware Implementation of Logic Gates

A **transistor** is a microscopic switch that turns current on or off. Billions of transistors in your computer form the logic gates that run programs and store data.

- **AND gate**: Output is high (1) only when all inputs are high
- **OR gate**: Output is high when at least one input is high
- **NOT gate** (inverter): Produces the opposite of its input
- **NAND gate**: Combines NOT and AND (universally functional)
- **NOR gate**: Combines NOT and OR
- **XOR gate**: Output is high when inputs are different

By connecting these gates in various configurations, engineers create circuits capable of arithmetic operations, memory storage, and decision-making.
## Analog vs Digital Signals

- **Analog** = Continuous (like sound waves or temperature)
- **Digital** = Binary (1s and 0s)

Digital signals are easier for computers to store, process, and transmit with less error.

Conversion between the two:
- **ADC**: Turns analog signals into digital (e.g., microphone)
- **DAC**: Turns digital back into analog (e.g., speaker)

## Data Flow and Abstraction Layers

Data travels through a computer and network in layers:

1. **TDU** - The actual message (e.g., a file or image)
2. **Segments** - Breaks the message into parts for transport
3. **Datagrams** - Adds IP info so it can move across networks
4. **Packets** - Adds instructions for how to handle the data
5. **Frames** - Formats the data for your specific network (like WiFi)
6. **Bits** - The raw 1s and 0s sent over wires or air

Each layer abstracts the one below it, hiding complexity while keeping things organised.

## Why Abstraction Matters

**Abstraction** means hiding details and showing only what’s necessary. It:

- Simplifies complexity
- Allows systems to be built in layers
- Makes technology easier to develop, use, and improve

Every part of computing, from code to hardware, relies on abstraction to work efficiently and scale.