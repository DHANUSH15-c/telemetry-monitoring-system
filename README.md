# 🚀 Telemetry Monitoring System

A fault-tolerant real-time telemetry visualization framework designed for mission-critical environments such as propulsion testing and industrial monitoring systems.

This project implements a **dual-server redundant telemetry architecture** to ensure uninterrupted real-time data visualization, even when one telemetry source fails.

---

## 📌 Project Overview

Telemetry monitoring systems continuously track parameters such as **pressure, temperature, and flow rate**. Traditional systems rely on a single data source, creating a **single point of failure**.

This project addresses this limitation by implementing a **redundant telemetry monitoring framework with automatic failover**, ensuring continuous system monitoring during server or network failures.

---

## 🏗 System Architecture

```
Telemetry Server 1 (Primary)
        │
        │ UDP Telemetry Stream
        ▼
Monitoring Application
 ┌─────────────────────────┐
 │ Receiver Thread (S1)    │
 │ Receiver Thread (S2)    │
 └─────────────────────────┘
        │
        ▼
 Queue Buffer System
        │
        ▼
Failover Monitoring Logic
        │
        ▼
Real-Time Plotting Engine
```

---

## ⚙ Key Features

- Dual-server redundant telemetry architecture  
- Automatic failover mechanism  
- UDP-based real-time data acquisition  
- Heartbeat-based server health monitoring  
- Multithreaded receiver architecture  
- Queue-based buffering system  
- CDT (Count Down Timer) synchronization  
- Cooldown-based switching logic  
- Smooth waveform transition during switching  
- Real-time visualization using Python & Matplotlib  

---

## 🧠 System Workflow

1. Telemetry servers transmit data via UDP  
2. Receiver threads collect data from both servers  
3. Server health is monitored using heartbeat timing  
4. Active server failure is detected  
5. Automatic failover is triggered  
6. Cooldown logic prevents rapid switching  
7. Continuous real-time plotting is maintained  

---

## 🧪 System Validation

The system was tested under multiple scenarios:

- Startup failover condition  
- Runtime server failure  
- Network delay conditions  
- High data-rate buffering scenarios  
- Long-duration continuous operation  

The system maintained **stable real-time visualization without GUI freezing or thread failures**.

---

## 🛠 Technology Stack

- Python  
- Matplotlib  
- NumPy  
- Threading  
- Queue  
- UDP Socket Programming  
- Dewesoft  

---

## 📂 Project Structure

```
Telemetry Monitoring System/
│
├── main_app.py
├── DAS_Server_UDP_10_15_1.py
├── DAS_Redn_Sim.py
├── DAS_CDT_Reception10_9.py
├── csv_read_10_9.py
│
├── tg_7.csv
├── info_7.csv
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## ▶ Installation

```bash
pip install matplotlib numpy pandas
```

---

## ▶ Running the System

```bash
python main_app.py
```

---

## 📊 System Demonstration

### AUTO MODE – Before Switching  
System operating in automatic mode before failover.  
![AUTO MODE BEFORE SWITCHING](AUTO%20MODE-BEFORE%20SWITCHING.png)

### AUTO MODE – After Switching  
Automatic failover triggered after server failure.  
![AUTO MODE AFTER SWITCHING](AUTO%20MODE-AFTER%20SWITCHING.png)

### MANUAL MODE – Before Switching  
Manual monitoring before switching servers.  
![MANUAL MODE BEFORE SWITCHING](MANUAL%20MODE-BEFORE%20SWITCHING.png)

### MANUAL MODE – After Switching  
Manual switching executed while maintaining visualization continuity.  
![MANUAL MODE AFTER SWITCHING](MANUAL%20MODE-AFTER%20SWITCHING.png)

---

## ⚠ Security Note

Sensitive details such as IP addresses, ports, and internal configurations have been anonymized.

---

## 👨‍💻 Author

**Dhanush K**

- GitHub: (http://github.com/DHANUSH15-c)
- LinkedIn: (http://linkedin.com/in/dhanush33)

---

## 🤝 Contribution

This project was developed as part of a collaborative work in real-time telemetry monitoring systems.

---

⭐ If you found this project useful, consider giving the repository a star.
