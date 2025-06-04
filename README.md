# MERN Application Monitoring Setup with Grafana & Prometheus

## 📁 Repository Link
[GitHub Repository: MERN Monitoring Setup](https://github.com/your-username/mern-monitoring-setup)

---

## 🚀 Project Overview
A comprehensive monitoring solution for a full-stack MERN application using **Grafana**, **Prometheus**, **Loki**, and **Jaeger**. This setup provides metrics, log aggregation, and tracing for frontend, backend, and database layers.

---

## 📦 Components
- **MERN Stack App** (Travel Memory App)
- **Prometheus** – Metrics collection
- **Grafana** – Visualization
- **MongoDB Exporter** – Database metrics
- **Loki + Promtail** – Log aggregation
- **Jaeger** – Distributed tracing

---

## 🛠️ Setup Instructions

### 1. Clone and Run the App
```bash
git clone https://github.com/your-username/mern-monitoring-setup.git
cd mern-monitoring-setup
npm install
npm start
```

### 2. Prometheus Metrics in Node.js Backend
- Installed `prom-client`
- Created `/metrics` endpoint with custom histogram for HTTP duration

### 3. MongoDB Exporter
- Used `mongodb_exporter` Docker image
- Configured to point to MongoDB URI

### 4. Grafana Dashboards
- Imported JSON dashboards
- Metrics shown:
  - Request count, errors, latency
  - MongoDB memory usage, ops/sec
  - Log patterns via Loki

### 5. Log Aggregation (Loki + Promtail)
- Installed Loki and Promtail
- Promtail scraped logs from `mern-backend.log`
- Added Loki as a datasource in Grafana

### 6. Tracing with Jaeger
- Installed `jaeger-client`
- Initialized tracer for backend
- Integrated Jaeger with Grafana

### 7. Alerts
- Created alerts for:
  - High latency
  - High error rate
  - Database CPU usage

---

## 📊 Grafana Dashboards
### ✅ Application Metrics
![App Metrics](screenshots/app_metrics.png)

### ✅ MongoDB Health
![Mongo Metrics](screenshots/mongo_metrics.png)

### ✅ Logs
![Logs](screenshots/logs.png)

### ✅ Tracing
![Tracing](screenshots/tracing.png)

---

## 📈 Performance Analysis
- Observed slow API calls during peak hours (8-9 PM)
- Spikes in DB connections resolved by index optimization
- Logs revealed frequent 404 errors on `/api/photos`
- Traces highlighted long hops between frontend → backend → DB

---

## 📄 Challenges & Fixes
- ❌ MongoDB exporter connection issues
  - ✅ Fixed with `authMechanism=SCRAM-SHA-1`
- ❌ Missing logs from Promtail
  - ✅ Corrected file path and access rights
- ❌ Jaeger UI not accessible
  - ✅ Exposed port `16686` in Docker

---

## 🎁 Bonus Implementations
- 🔁 Kubernetes HPA setup based on CPU metrics (optional branch)
- 🌐 Istio service mesh tested on separate microservice demo

---

## ✅ Conclusion
This project successfully integrates monitoring, log aggregation, and tracing in a full MERN stack. The setup improves observability and helps detect performance issues early.

---

## 📎 Submission
- [x] Code pushed to GitHub
- [x] Dashboards, Logs, Traces visualized in Grafana
- [x] Report documented with screenshots
- [x] Performance analysis included
