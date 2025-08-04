# 🐳 ELK + Filebeat + Realistic Log Generator (Docker)

This project sets up a complete **ELK stack** (Elasticsearch + Logstash + Kibana) with **Filebeat** and a **log-generating Linux container**, all running in **Docker Compose**.

> ✅ No local installations  
> ✅ Works entirely inside Docker  
> ✅ Real-time log simulation for SOC, DevSecOps, and analysis labs

---

## 📦 Components

| Service       | Purpose                                     |
|---------------|---------------------------------------------|
| Elasticsearch | Stores indexed logs                         |
| Logstash      | Parses and forwards logs                    |
| Kibana        | Web UI to search and visualize logs         |
| Filebeat      | Reads log files and sends to Logstash       |
| Log Generator | Simulates a real VM writing logs to disk    |

---

## 🛠️ Folder Structure

```
elk-docker/
├── docker-compose.yml
├── filebeat/
│   └── filebeat.yml
├── logstash/
│   └── logstash.conf
├── .gitignore
└── README.md
```

---

## 🚀 How to Run

```
1. Clone or download this repository

2. From inside the project folder, run:

   docker-compose up -d

3. Wait about 1–2 minutes for everything to start

4. Visit:
   http://localhost:5601
```

---

## 🔍 Setup in Kibana

```
1. Open your browser:
   http://localhost:5601

2. Go to:
   Stack Management → Data Views (or Index Patterns)

3. Click:
   "Create data view" or "Create index pattern"

4. Name it:
   filebeat-logs-*

5. Time field:
   Select @timestamp

6. Click:
   Create data view

7. Go to:
   Discover → Select filebeat-logs-* in top-left

8. Start searching:
   Try filtering for fields like "message", "host.name", "log.offset"
```

---

## 👨‍💻 Author

Created by Chen Bracha
For personal learning, threat hunting, and SIEM/DevSecOps practice.

