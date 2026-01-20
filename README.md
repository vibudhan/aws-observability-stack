# AWS Observability Stack 🚀 (Prometheus + Grafana + Alertmanager)

A complete **Monitoring & Alerting (Observability) stack** deployed on **AWS EC2 (Free Tier eligible)** using **Docker Compose**.  
This setup collects Linux server metrics using **Node Exporter**, stores time-series data in **Prometheus**, visualizes everything in **Grafana**, and enables alerting using **Grafana Alert Rules** + **Alertmanager**.

---

## ✅ Tech Stack
- **AWS EC2 (Amazon Linux 2023)**
- **Docker + Docker Compose**
- **Prometheus**
- **Node Exporter**
- **Grafana**
- **Alertmanager**

---

## 🎯 Key Highlights
✅ Deployed full monitoring stack on AWS EC2 using Docker Compose  
✅ Prometheus configured to scrape Node Exporter metrics  
✅ Grafana configured with Prometheus as datasource  
✅ Imported dashboards:
- **Node Exporter Full (Dashboard ID: 1860)**
- **Prometheus Overview Dashboard**

✅ Configured Grafana Alert Rule:
- **High CPU Usage Alert** (Resume-ready real-world alert)

✅ Verified Prometheus Target Health:
- `prometheus` ✅ UP
- `node-exporter` ✅ UP

---

## 🏗️ Architecture

# AWS Observability Stack 🚀 (Prometheus + Grafana + Alertmanager)

A complete **Monitoring & Alerting (Observability) stack** deployed on **AWS EC2 (Free Tier eligible)** using **Docker Compose**.  
This setup collects Linux server metrics using **Node Exporter**, stores time-series data in **Prometheus**, visualizes everything in **Grafana**, and enables alerting using **Grafana Alert Rules** + **Alertmanager**.

---

## ✅ Tech Stack
- **AWS EC2 (Amazon Linux 2023)**
- **Docker + Docker Compose**
- **Prometheus**
- **Node Exporter**
- **Grafana**
- **Alertmanager**

---

## 🎯 Key Highlights
✅ Deployed full monitoring stack on AWS EC2 using Docker Compose  
✅ Prometheus configured to scrape Node Exporter metrics  
✅ Grafana configured with Prometheus as datasource  
✅ Imported dashboards:
- **Node Exporter Full (Dashboard ID: 1860)**
- **Prometheus Overview Dashboard**

✅ Configured Grafana Alert Rule:
- **High CPU Usage Alert** (Resume-ready real-world alert)

✅ Verified Prometheus Target Health:
- `prometheus` ✅ UP
- `node-exporter` ✅ UP

---

## 🏗️ Architecture

User / Browser
|
|--> Grafana (3000)
|
|--> Prometheus (9090)
|
|--> Node Exporter (9100)
|
|--> Alertmanager (9093)

---

## 🔐 AWS Security Group (Inbound Rules)

Recommended inbound rules (for safety keep source = **My IP only**)

| Service | Port | Source |
|--------|------|--------|
| SSH | 22 | My IP |
| Grafana | 3000 | My IP |
| Prometheus | 9090 | My IP |
| Node Exporter | 9100 | My IP |
| Alertmanager | 9093 | My IP |

✅ Best Practice: Never keep these ports open to `0.0.0.0/0` in production.

---

## ⚙️ Project Setup (Step-by-Step)

### 1️⃣ Install Docker (EC2)
```bash
sudo yum update -y
sudo yum install -y docker
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker ec2-user
newgrp docker
docker --version

---

## 🔐 AWS Security Group (Inbound Rules)

Recommended inbound rules (for safety keep source = **My IP only**)

| Service | Port | Source |
|--------|------|--------|
| SSH | 22 | My IP |
| Grafana | 3000 | My IP |
| Prometheus | 9090 | My IP |
| Node Exporter | 9100 | My IP |
| Alertmanager | 9093 | My IP |

✅ Best Practice: Never keep these ports open to `0.0.0.0/0` in production.

---

## ⚙️ Project Setup (Step-by-Step)

### 1️⃣ Install Docker (EC2)
```bash
sudo yum update -y
sudo yum install -y docker
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker ec2-user
newgrp docker
docker --version

###2️⃣ Install Docker Compose Plugin
sudo yum install -y docker-compose-plugin
docker compose version

###3️⃣ Clone Repository
git clone https://github.com/vibudhan/aws-observability-stack.git
cd aws-observability-stack

###4️⃣ Start the Observability Stack
docker compose up -d

###5️⃣ Verify Running Containers
docker ps

🌐 Access URLs

Replace <EC2_PUBLIC_IP> with your EC2 Public IPv4:

✅ Grafana UI
http://<EC2_PUBLIC_IP>:3000

✅ Prometheus UI
http://<EC2_PUBLIC_IP>:9090

✅ Prometheus Targets (Health Check)
http://<EC2_PUBLIC_IP>:9090/targets

✅ Node Exporter Metrics
http://<EC2_PUBLIC_IP>:9100/metrics

✅ Alertmanager UI
http://<EC2_PUBLIC_IP>:9093

🔑 Grafana Login

Default credentials:

Username: admin
Password: admin

## 📸 Output Screenshots

### ✅ 1) Prometheus Targets (UP Status)
![Output 1](screenshots/output1.png)

### ✅ 2) Grafana Dashboard (Node Exporter Full)
![Output 2](screenshots/output2.png)

### ✅ 3) Prometheus Overview / Metrics
![Output 3](screenshots/output3.png)

### ✅ 4) Alert Rule Created (CPU Alert)
![Output 4](screenshots/output4.png)

### ✅ 5) Alert / Contact Point Setup
![Output 5](screenshots/output5.png)

### ✅ 6) Full Monitoring Stack View
![Output 6](screenshots/output6.png)



👤 Author

Vibudhan Dubey
GitHub: https://github.com/vibudhan




