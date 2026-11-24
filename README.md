# 🛡️ Ciberseguridad Labs

Laboratorios prácticos de seguridad defensiva (Blue Team) documentados de principio a fin. Cada práctica sigue el mismo enfoque: **explotar** la vulnerabilidad, **entender** por qué existe y **corregirla / detectarla**.

> Vengo del desarrollo web, así que no me quedo en "esto se rompe así": me interesa el *porqué* a nivel de sistema y de código, y cómo defenderlo.

---

## 🎯 Enfoque

Todo el repositorio gira en torno a la **defensa en profundidad**: cómo un mismo ataque (p. ej. fuerza bruta SSH) se **previene** con bastionado, se **detecta** en el host con un IDS y se **detecta y correlaciona** de forma centralizada en un SIEM.

Entorno de laboratorio: máquinas virtuales aisladas (Kali Linux + Ubuntu Server) en VirtualBox. Todas las técnicas se aplican sobre sistemas propios en redes aisladas.

---

## 📂 Prácticas

| # | Práctica | Herramientas | Qué demuestra |
|---|----------|--------------|---------------|
| 01 | [Hardening de SSH + túneles](./01-ssh-hardening) | OpenSSH, sshd_config | Administración remota segura; autenticación por clave; túneles `-L`/`-R`/`-D` y su doble lectura ofensiva/defensiva |
| 02 | [Firewall con iptables (stateless vs stateful)](./02-iptables-firewall) | iptables, conntrack | Diferencia entre firewall sin estado y con estado; por qué el stateful es más seguro y mantenible |
| 03 | [Bastionado CIS / ENS](./03-bastionado-cis) | Ubuntu Security Guide (USG), CIS Benchmarks | Trabajo con marcos normativos; evidencia de cumplimiento (62% → 95%); tailoring |
| 04 | [Detección de fuerza bruta SSH con Snort](./04-snort-ids) | Snort, Hydra, crunch | Anatomía de una regla de IDS; detección por umbral; reducción de falsos positivos |
| 05 | [SIEM end-to-end con Elastic](./05-siem-elastic) | Elastic Security, Elastic Agent, MITRE ATT&CK | Ingesta de logs, normalización ECS, reglas de detección y mapeo a MITRE |
| 06 | [Hacking Web / OWASP Top 10](./06-hacking-web-owasp) | DVWA, OWASP Juice Shop, Burp Suite | SQLi, XSS, RCE, CSRF, JWT — con la corrección segura en código para cada una |

*(Repositorio en construcción — se irán añadiendo prácticas de forense de memoria con Volatility y firewall NGFW con Fortinet.)*

---

## 🧩 Estructura de cada práctica

Cada carpeta contiene:

- **`README.md`** — objetivo, conceptos clave, pasos y lecciones para entrevista.
- **Artefactos** — scripts, configuraciones comentadas, reglas o informes según el caso.

---

## 🧠 Sobre el autor

Iván Muñoz — Técnico Superior en DAW especializado en Ciberseguridad, en preparación de la **CompTIA Security+ (SY0-701)**. Buscando mi primera oportunidad como Analista SOC o en bastionado de sistemas.

[LinkedIn](https://linkedin.com/in/ivanmunozhernandez) · [Perfil de GitHub](https://github.com/ivicho17)

---

> ⚠️ **Aviso**: todo el contenido es con fines educativos y defensivos, realizado en laboratorios propios y aislados. El uso de estas técnicas fuera de un entorno controlado y autorizado es ilegal.
