# BJT Input Characteristics Using LTspice and Python

This project demonstrates how to obtain the **input characteristics of a Bipolar Junction Transistor (BJT)** in a **common-emitter configuration** using **LTspice** and visualize the results with **Python**.

The workflow covers circuit simulation, data export, and plotting the transistor's input characteristic curve.

---

## Overview

The project consists of three main stages:

1. Simulate the BJT circuit in LTspice.
2. Export the simulation data.
3. Plot the results using Python.

The resulting graph shows the relationship between:

- Base-Emitter Voltage (\(V_{BE}\))
- Base Current (\(I_B\))

---

## Project Structure

```
.
├── ltspice_smulation/
│   ├── input_characteristics.asc
│   ├── input_characteristics.net
│   └── exported_data.txt
│
├── python/
│   ├── plot_input_characteristics.py
│   └── requirements.txt
│
├── images/
│   ├── circuit.png
│   └── input_characteristics.png
│
├── LICENSE
└── README.md
```

---

## Requirements

### LTspice

Download and install LTspice.

---

### Python

Python 3.10 or newer is recommended.

Install the required packages:

```bash
pip install numpy matplotlib pandas
```

---

## LTspice Simulation

The circuit is configured in a **Common Emitter** configuration.

Simulation Type:

```
DC Sweep
```

Base voltage is swept while collector voltage remains constant.

Example command:

```
.dc V1 0 1 0.01
```

To generate multiple curves at different collector voltages:

```
.step param VCC list 2 5 10
```

---

## Exporting Simulation Data

After the simulation:

1. Run the simulation.
2. Open the waveform viewer.
3. Select:

```
File → Export Data as Text
```

Export the following variables:

```
V(B)
Ib(Q1)
```

Save the file as

```
exported_data.txt
```

---

## Python Visualization

Run

```bash
python plot_input_characteristics.py
```

The script will:

- Load the exported LTspice data
- Plot the input characteristic
- Display the graph

---

## Output

The generated graph illustrates:

- Base current versus Base-Emitter voltage
- Exponential transistor behavior
- Turn-on region
- Active region

Example output:

```
IB
│
│
│           ●
│        ●
│      ●
│    ●
│  ●
└──────────────────────► VBE
```

---

## Concepts Covered

- Bipolar Junction Transistor (BJT)
- Common Emitter Configuration
- Input Characteristics
- DC Sweep Analysis
- LTspice Simulation
- Data Export
- Python Data Visualization
- Matplotlib
- NumPy

---

## Applications

This project is useful for:

- Electronics students
- Electrical Engineering students
- Laboratory demonstrations
- Device characterization
- Analog circuit design
- Teaching transistor fundamentals

---

## Video Tutorial

A complete walkthrough is available on YouTube.


## Future Improvements

- Output characteristics
- Transfer characteristics
- Current gain (β) calculation
- Automatic LTspice data parsing
- Interactive plots
- Curve fitting
- Plot export to PDF
- Jupyter Notebook version

---

## Contributing

Contributions are welcome.

If you would like to improve the project:

1. Fork the repository.
2. Create a new branch.
3. Commit your changes.
4. Open a Pull Request.

---

## License

This project is released under the MIT License.

---

## Author

**Odari Charles**

Electrical & Electronic Engineering

---

## Support

If you find this project useful:

⭐ Star the repository

🍴 Fork the project

📢 Share it with others

Happy Learning!
