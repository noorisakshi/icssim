# ICSSIM - Industrial Control System Security Simulation Framework

## Overview

ICSSIM is a virtual Industrial Control System (ICS) security testbed designed for studying, analyzing, and demonstrating cybersecurity attacks and defenses in industrial environments.

The framework simulates a realistic industrial automation process using Programmable Logic Controllers (PLCs), Human Machine Interfaces (HMIs), industrial communication protocols, and networked control components. By leveraging Docker containers and network emulation, ICSSIM provides a safe environment for conducting cybersecurity experiments without affecting real industrial infrastructure.

This project can be used for:

* ICS cybersecurity research
* Industrial network simulation
* Cyberattack demonstration and analysis
* Security testing of PLC-based systems
* Educational laboratories and academic projects
* Industrial process modeling and visualization

---

## Project Objectives

The primary objectives of this project are:

* Create a realistic virtual ICS environment
* Simulate industrial control processes
* Study vulnerabilities in industrial networks
* Analyze cyberattacks targeting control systems
* Evaluate mitigation and defense mechanisms
* Provide a reproducible platform for cybersecurity experimentation

---

## System Architecture

The framework follows a layered industrial network architecture inspired by the Purdue Enterprise Reference Model.

### Components

* PLC Controllers
* Human Machine Interfaces (HMI)
* Industrial Sensors
* Actuators and Valves
* Process Simulation Engine
* Industrial Communication Network
* Cyberattack Node
* Docker-based Virtual Infrastructure

Each component runs independently, allowing realistic interaction between industrial devices and network services.

---

## Simulated Industrial Process

### Bottle Filling Factory

The sample implementation models an automated bottle-filling production line.

#### Process Workflow

1. Empty bottles arrive on the conveyor belt.
2. Bottles move into the filling station.
3. PLC-1 controls the water tank and filling valves.
4. Water is dispensed into bottles.
5. PLC-2 controls conveyor movement.
6. Filled bottles are removed.
7. New empty bottles enter the process.

This setup provides a realistic environment for studying process manipulation attacks and industrial protocol exploitation.

---

## Cybersecurity Features

The simulation environment allows testing of various attack scenarios including:

### Network-Based Attacks

* Denial of Service (DoS)
* Distributed Denial of Service (DDoS)
* Packet Manipulation
* Replay Attacks
* Man-in-the-Middle Attacks

### Industrial Attacks

* Unauthorized PLC Commands
* Sensor Data Manipulation
* Actuator Tampering
* False Data Injection
* Process Disruption

### Security Research

* Intrusion Detection Testing
* Traffic Analysis
* Threat Monitoring
* Incident Response Evaluation

---

## Technology Stack

| Component                   | Technology     |
| --------------------------- | -------------- |
| Programming Language        | Python         |
| Containerization            | Docker         |
| Orchestration               | Docker Compose |
| Industrial Protocol         | Modbus TCP     |
| Simulation Environment      | GNS3           |
| Shared Memory Communication | Memcached      |
| Version Control             | Git            |

---

## Installation

### Prerequisites

Install the following software:

* Python 3.x
* Git
* Docker
* Docker Compose

Install required Python packages:

```bash
pip install pyModbusTCP
pip install memcache
```

---

## Clone Repository

```bash
git clone https://github.com/noorisakshi/icssim.git
cd icssim
```

---

## Running with Docker

Open the configuration file:

```bash
src/Configs.py
```

Set:

```python
EXECUTION_MODE = EXECUTION_MODE_DOCKER
```

Start the environment:

```bash
cd deployments
./init.sh
```

Verify running containers:

```bash
docker-compose ps
```

If all services show **Up**, the simulation is running successfully.

---

## Accessing System Components

The deployment directory contains helper scripts for interacting with different nodes:

```bash
hmi1.sh
hmi2.sh
attacker.sh
```

These scripts provide direct access to corresponding containers for monitoring, control, and attack simulation.

---

## Running Locally

Configure:

```python
EXECUTION_MODE = EXECUTION_MODE_LOCAL
```

Start the project:

```bash
cd src
python3 start.py
```

---

## Running in GNS3

1. Open GNS3.
2. Import the portable project file:

```text
deployments/GNS3/ICSSIM-GNS3-Portable.gns3project
```

3. Start all nodes.
4. Observe industrial communication and process behavior.

---

## Educational Applications

This project can be used in courses related to:

* Industrial Cybersecurity
* Network Security
* Critical Infrastructure Protection
* Control Systems Engineering
* Industrial Automation
* Cyber-Physical Systems

---

## Future Enhancements

Potential improvements include:

* SCADA integration
* Advanced attack detection
* Machine learning based anomaly detection
* Digital twin modeling
* Additional industrial protocols
* Real-time visualization dashboards

---

## Disclaimer

This framework is intended solely for educational, research, and cybersecurity training purposes. All experiments should be conducted in isolated environments. Users are responsible for ensuring ethical and legal use of the software.

---

## Author

**Noorisakshi**

Industrial Control System Security Simulation Project

GitHub Repository:
https://github.com/noorisakshi/icssim
