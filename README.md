# pfSense-lab-basic
Laboratorio de ciberseguridad montado con VMware Workstation, incluyendo pfSense, endpoint Windows y Kali.
## 🧱 Estructura de carpetas del repositorio
```
/
├── README.md
├── capturas/
│   ├── topologia.png
│   ├── reglas-fw.png
│   └── alertas-sysmon.png
├── config/
│   ├── reglas-pfsense.txt
│   └── ip-plan.md
├── notas/
│   └── lecciones-aprendidas.md
```
# 🛡️ Laboratorio de Ciberseguridad - pfSense + VMware + Endpoint
## 🎯 Objetivo
Simular un entorno básico de red con firewall pfSense, un endpoint Windows y un atacante Kali Linux, con el fin de practicar monitoreo, segmentación de red y reglas defensivas.

## 🔧 Infraestructura
- VMware Workstation 17.6.3
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
```
nmap -sS 192.168.10.0/24
```
pfSense bloqueó el tráfico según reglas predefinidas.

## ✅ Resultados
Se comprobó funcionamiento de reglas, se registró el evento en el log, y el endpoint mantuvo conectividad solo a servicios permitidos.

## 📚 Lecciones aprendidas
Revisar notas/lecciones-aprendidas.md
