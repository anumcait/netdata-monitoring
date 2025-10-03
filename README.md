# Monitor System Resources Using Netdata

## 🎯 Objective

Install and run Netdata (a lightweight monitoring tool) to visualize system & application performance metrics in real-time.

## ⚙️ Steps

### 1. Run Netdata in Docker
```bash
docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
```
### 2. Access Dashboard

Open your browser:
👉 http://localhost:19999

### 3. Explore Metrics

- CPU usage (per-core & overall)
- Memory usage (RAM, cache, swap)
- Disk I/O (read/write speeds, latency)
- Docker containers (resource usage of each container)
- Network traffic (packets in/out, bandwidth)

### 4. Explore Alerts

- Netdata ships with predefined health checks (CPU spikes, memory leaks, etc).
- Alerts show up as warnings/critical in the dashboard.

### 5. Logs
```bash
docker logs netdata
```
Or check inside container:
```bash
docker exec -it netdata bash
cat /var/log/netdata/error.log
```
## 📸 Screenshots
<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/c1540594-83af-4be0-bee6-8c50c8e74863" />
<img width="7000" height="500" alt="image" src="https://github.com/user-attachments/assets/59c3af9e-0622-42d3-aec6-79d67122af97" />
<img width="7000" height="500" alt="image" src="https://github.com/user-attachments/assets/c11c14a0-a4b7-4c4c-8957-00007dea6e94" />
<img width="7000" height="500" alt="image" src="https://github.com/user-attachments/assets/08f4f4d6-32a4-4602-8aa5-baf8c49c6e64" />
<img width="7000" height="500" alt="image" src="https://github.com/user-attachments/assets/ce7719a8-6ed2-496f-a8a9-e1f0013fad82" />






