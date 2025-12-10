# Security-Lab 01 – Nmap Recon gegen Healthcare-Backend

## 1. Ziel und Kontext

- Projekt: Healthcare OPS – Lernlabor für Pentesting & Blue Team im Gesundheitswesen
- Blue-Team-Zielsystem:
  - Name: Healthcare-Backend
  - OS: Kali Linux
  - IP: 192.168.178.85
  - Rolle: Backend + Frontend + Wazuh-Agent
- Red-Team-System:
  - Name: linuxkali
  - OS: Kali Linux
  - Rolle: Angreifer-VM im gleichen Netzwerk

Ziel dieses Labs:
- Klassische Recon-Phase simulieren (Portscan und Service-Erkennung).
- Überprüfen, ob Wazuh den Scan erkennt und als verdächtige Aktivität meldet.
- Ergebnisse und Alerts als Nachweis für mein Portfolio dokumentieren.

---

## 2. Angriff – Nmap Scan von linuxkali

### 2.1 Vorbereitung

Auf der Red-Team-VM `linuxkali`:


TARGET=192.168.178.85
mkdir -p ~/recon/healthcare-backend
cd ~/recon/healthcare-backend

ping -c 4 $TARGET
Ergebnis:
PING 192.168.178.85 (192.168.178.85) 56(84) bytes of data.
64 bytes from 192.168.178.85: icmp_seq=1 ttl=64 time=0.193 ms
64 bytes from 192.168.178.85: icmp_seq=2 ttl=64 time=0.219 ms
64 bytes from 192.168.178.85: icmp_seq=3 ttl=64 time=0.185 ms
64 bytes from 192.168.178.85: icmp_seq=4 ttl=64 time=0.221 ms




