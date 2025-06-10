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

## 🚀 How to Run

Install dependencies:

```bash
pip install -r requirements.txt