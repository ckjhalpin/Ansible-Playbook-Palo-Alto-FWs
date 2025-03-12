# Palo Alto Firewall Ansible Automation 🔥

## 📌 Overview
This **Ansible playbook** automates **Palo Alto Firewall policy management**.  
It helps **Network Security Engineers** to:
- **Apply security rules** automatically.
- **Enforce compliance** across multiple firewalls.
- **Eliminate manual errors** in firewall rule changes.

## ⚙️ How It Works
1. Uses **Ansible PAN-OS module** to connect to a firewall.
2. Deploys predefined **security policies**.
3. Verifies **policy enforcement** via API calls.

## 🏗️ Prerequisites
- Ansible installed (`pip install ansible`)
- Palo Alto Firewall API access
- Install Ansible PAN-OS module:
  ```bash
  ansible-galaxy collection install paloaltonetworks.panos

## 🚀 Usage
ansible-playbook palo_alto_firewall.yaml --extra-vars "firewall_ip=10.0.0.1"

## 🛠️ Issues & Troubleshooting
- paloaltonetworks.panos not found
Run - ansible-galaxy collection install paloaltonetworks.panos
- connection timeout
Ensure firewall API access is enabled. - curl -k -X GET 'https://<FIREWALL_IP>/api/?type=op&cmd=<show><system><info></info></system></show>&key=<API-KEY>'
- Policy Not Applied
- Check firewall logs:- tail -f /var/log/pan_config.log

## 📜 Sample Output
PLAY [Deploy Palo Alto Firewall Policy] *****************************************

TASK [Apply security policies] *************************************************
✔ Success: Policy "Allow Web Traffic" added
✔ Success: Policy "Block SSH Traffic" added

## 🔗 Future Enhancements
✅ Automate firewall backups
✅ Enforce Zero Trust security rules
✅ Deploy via CI/CD pipeline


---

### **🛠 Final Steps for GitHub**
1. **Upload `README.md`** files to **each repo**.
2. Add **screenshots/logs** for better visibility.
3. **Structure your GitHub** as follows:



