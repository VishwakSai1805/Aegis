# 🛡️ Aegis: Agentic Edge-IoT Security Node

**Team:** SudoShield  
**Event:** eRaksha Hackathon 2026  
**Status:** 🚧 Prototype Under Active Development

## 📖 Overview
Aegis is an **Agentic AI-powered security appliance** designed to protect home IoT environments. Unlike passive firewalls, Aegis employs an **Active Defence** strategy using autonomous deception (honeypots) and heuristic baseline profiling to detect and neutralize threats in real-time.

It runs on low-cost edge hardware (Raspberry Pi / Linux Gateway) and requires zero configuration from the end-user.

## 🚀 Key Features
* **🕵️ The Surveyor (Discovery Agent):** Continuously scans the local subnet to catalog devices and assigns dynamic **Risk Scores** based on open ports and anomalous behavior.
* **🪤 The Decoy (Deception Agent):** Deploys lightweight Docker containers acting as "Ghost Nodes" (fake vulnerable devices) to trap botnets and lateral movement attempts.
* **🛡️ The Enforcer (Autonomous Defence):** A Python-based decision engine that instantly updates `iptables` / `UFW` rules to isolate compromised devices upon threat detection.

## 🛠️ Tech Stack
* **Core Logic:** Python 3 (AsyncIO, State Machine)
* **Network Analysis:** Scapy (Packet Sniffing & Injection)
* **Deception:** Docker (Containerized Honeypots)
* **Firewall:** Linux iptables/nftables
* **Hardware Target:** Raspberry Pi 4 / Ubuntu Edge Server

## 🧩 Architecture
1.  **Listener:** Monitors network traffic for interaction with Decoy nodes.
2.  **Analyzer:** Compares traffic against device baselines.
3.  **Responder:** Executes blocking commands via the OS shell.

## ⚠️ Disclaimer
This project is developed strictly for **defensive cybersecurity purposes** and educational demonstration during the eRaksha Hackathon.
