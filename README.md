# pfSense-lab-basic
Laboratorio de ciberseguridad montado con VMware Workstation, incluyendo pfSense, endpoint Windows y Kali.
# 🛡️ Laboratorio de Ciberseguridad - pfSense + VMware + Endpoint

## 🎯 Objetivo
Simular un entorno básico de red con firewall pfSense, un endpoint Windows y un atacante Kali Linux, con el fin de practicar monitoreo, segmentación de red y reglas defensivas.

## 🔧 Infraestructura
- VMware Workstation 17
- pfSense 2.7.2
- Windows 10 Pro (endpoint)
- Kali Linux (atacante)
- 2 adaptadores virtuales por VM

## 🌐 Topología
![topología de red](capturas/topologia.png)

## ⚙️ Reglas de Firewall
- Bloqueo total de ICMP desde LAN a WAN
- Permitir solo HTTP/HTTPS y DNS saliente desde el endpoint
- Regla extra: bloqueo de escaneo SYN desde Kali

## 🚨 Simulación de Ataque
Desde Kali se ejecutó:
```bash
nmap -sS 192.168.10.0/24
