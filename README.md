# MERN Application Monitoring Setup with Grafana & Prometheus

## 📁 Repository Link


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

## 📎 Submission
- [x] Code pushed to GitHub
- [x] Dashboards, Logs, Traces visualized in Grafana
- [x] Report documented with screenshots
- [x] Performance analysis included
