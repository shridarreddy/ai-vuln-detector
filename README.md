# AI-Augmented Vulnerability Detection 🚨🤖

This project is a lightweight, ML-powered prototype that detects anomalous traffic behavior and prioritizes it using customizable risk scoring. Built in a local lab environment using Kali Linux and Windows Server on VirtualBox.

## 🔍 Use Case

Modern Security Operations Centers (SOCs) are overwhelmed by false alerts. This notebook prototype demonstrates:
- Isolation Forest-based anomaly detection
- Rule-based contextual risk scoring
- Flow-level alert triage
- Visual analytics of suspicious traffic

## 🧪 Lab Setup

- **Attacker**: Kali Linux (running `nmap`, `hping3`)
- **Target**: Windows Server 2022
- **Monitoring**: Wireshark + Zeek + tshark for `.pcap → CSV`

## 📊 Features

- Data cleaning and feature extraction on Zeek-like traffic logs
- Anomaly detection using Isolation Forest (unsupervised)
- Domain-specific risk scoring based on port + frame size
- Output of critical alerts: `anomaly == -1 && risk_level != 'Low'`
- Unified visualizations for analysis

## 🔍 Anomaly Detection Visualization

![image](https://github.com/user-attachments/assets/3c21f408-d34b-477c-800b-3174b547ed7c)


## ⚠️ Critical Alerts (Anomalous + High Risk)

![image](https://github.com/user-attachments/assets/7478df47-5031-4504-a443-23d7657dbcd6)


## 📊 Risk Level Distribution

![image](https://github.com/user-attachments/assets/53683012-531a-4433-821e-34c583527cc3)


## 🚀 How to Run

Install dependencies:

```bash
pip install -r requirements.txt
