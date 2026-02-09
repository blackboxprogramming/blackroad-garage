# BlackRoad Fleet Inventory

Last updated: 2026-02-09

## Human in the Loop

### alexandria (Mac)
- **Role**: Control Center, Human Operator
- **Local IP**: 192.168.4.28
- **Tailscale**: 100.91.90.68
- **User**: alexa
- **Purpose**: Development workstation, fleet orchestration

---

## AI Compute Nodes (Pironman Pi 5 + Hailo-8)

### octavia
- **Hardware**: Raspberry Pi 5 in Pironman 5 case
- **Local IP**: 192.168.4.81
- **Tailscale**: 100.83.149.86
- **User**: pi
- **AI Accelerator**: Hailo-8 (26 TOPS)
  - Serial: HLLWM2B233704606
  - Firmware: 4.23.0
- **Storage**:
  - SD Card: 128GB (boot)
  - NVMe: 1TB @ /mnt/nvme (870GB free)
- **RAM**: 8GB
- **Docker**: Yes (v29.1.3)
- **Fan Service**: pironman5 running

### cecilia
- **Hardware**: Raspberry Pi 5 in Pironman 5 case
- **Local IP**: 192.168.4.89
- **Tailscale**: 100.72.180.98
- **User**: cecilia
- **AI Accelerator**: Hailo-8 (26 TOPS)
  - Serial: HLLWM2B233704667
  - Firmware: 4.23.0
- **Storage**:
  - NVMe: 500GB (BOOT DRIVE - 420GB free)
- **RAM**: 8GB
- **Docker**: Yes
- **Services**: Ollama, CECE Net Gateway
- **Fan Service**: pironman5 running
- **Benchmark**: ResNet-50 @ 24 FPS

---

## Compute Cluster (Raspberry Pi)

### alice
- **Hardware**: Raspberry Pi 4
- **Local IP**: 192.168.4.49
- **Tailscale**: 100.77.210.18
- **User**: pi
- **Role**: Headscale mesh server
- **Docker**: 7 containers
- **Disk**: 97% used (NEEDS CLEANUP!)
- **RAM**: 4GB
- **Uptime**: 27+ days

### lucidia
- **Hardware**: Raspberry Pi 4
- **Local IP**: 192.168.4.38
- **Tailscale**: 100.66.235.47
- **User**: pi
- **Role**: Mesh node
- **Docker**: 15 containers
- **Disk**: 92% used
- **RAM**: 8GB
- **Uptime**: 27+ days

### aria
- **Hardware**: Raspberry Pi 5
- **Local IP**: 192.168.4.82
- **Tailscale**: 100.109.14.17
- **User**: pi
- **Role**: PRIMARY Docker host
- **Docker**: 142 containers
- **Disk**: 44% used (16GB free)
- **RAM**: 8GB
- **Uptime**: 27+ days

---

## Cloud Servers (DigitalOcean)

### codex-infinity
- **Provider**: DigitalOcean
- **Region**: NYC3
- **Public IP**: 159.65.43.12
- **Tailscale**: 100.108.132.8
- **User**: root
- **Specs**: 8GB RAM, 4 vCPU, 80GB disk
- **Disk**: 26% used (58GB free)
- **Uptime**: 28+ days

### shellfish
- **Provider**: DigitalOcean
- **Region**: NYC1
- **Public IP**: 174.138.44.45
- **Tailscale**: 100.94.33.37
- **User**: root
- **Specs**: 1GB RAM, 1 vCPU, 25GB disk
- **Disk**: 52% used (13GB free)
- **Uptime**: 44+ days

---

## Offline/Pending

### anastasia
- **Hardware**: Pironman Pi 5 (needs setup)
- **Expected IP**: 192.168.4.90
- **Status**: Not located

### olympia
- **Hardware**: PiKVM V3 HAT on Pi 4B
- **Hostname**: pikvm.local
- **Status**: Unknown

---

## Fleet Totals

| Metric | Value |
|--------|-------|
| Total Devices | 8 (online) |
| Local Pis | 5 |
| Cloud Servers | 2 |
| AI Accelerators | 2x Hailo-8 |
| Total AI TOPS | 52 |
| Docker Containers | 167 |
| Total RAM | ~35GB |
| Tailscale Nodes | 8/8 connected |
