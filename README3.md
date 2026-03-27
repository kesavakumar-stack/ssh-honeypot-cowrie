# 🐝 SSH Honeypot Lab using Cowrie

## 📌 Overview
This project demonstrates how to build a Home Lab SSH Honeypot using Cowrie to simulate a vulnerable SSH server and monitor attacker behavior.

## 🎯 Objective
To deploy a honeypot that captures attacker login attempts and commands for analysis.

## 🛠 Tools Used
- Ubuntu Server  
- Kali Linux  
- Cowrie Honeypot  
- VirtualBox  
- Python  
- SSH  

## 🏗 Lab Architecture
Kali Linux (Attacker)
        ↓
SSH Attack (Port 2222)
        ↓
Ubuntu Server (Cowrie Honeypot)
        ↓
Logs stored in cowrie.log

## ⚙️ Installation Steps

### 1. Update System
sudo apt update

### 2. Install Dependencies
sudo apt install git python3 python3-venv python3-pip -y

### 3. Clone Cowrie
git clone https://github.com/cowrie/cowrie.git  
cd cowrie  

### 4. Create Virtual Environment
python3 -m venv cowrie-env  
source cowrie-env/bin/activate  

### 5. Install Requirements
pip install -r requirements.txt  

### 6. Start Cowrie
bin/cowrie start  

## 🧪 Attack Simulation
ssh root@<honeypot_ip> -p 2222

## 📊 Log Monitoring
tail -f ~/cowrie/var/log/cowrie/cowrie.log

## 📂 Project Structure
- src/ → core files  
- honeyfs/ → fake system  
- var/ → logs  
- etc/ → config  

## 🎯 Outcome
- Captured attacker login attempts  
- Monitored commands executed  
- Learned honeypot and log analysis  

## 📸 Screenshots
(Add your screenshots here)

## 👨‍💻 Author
Kesavakumar
