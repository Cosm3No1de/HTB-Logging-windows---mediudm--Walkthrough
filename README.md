# 🛡️ HTB Logging – Walkthrough

[![HTB](https://img.shields.io/badge/HackTheBox-Logging-blue?style=flat-square&logo=hackthebox)](https://www.hackthebox.com/)
[![Difficulty](https://img.shields.io/badge/Difficulty-Medium-orange?style=flat-square)](https://www.hackthebox.com/)
[![OS](https://img.shields.io/badge/OS-Windows-informational?style=flat-square&logo=windows)](https://www.microsoft.com/)
[![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

> **Máquina:** Logging · **Plataforma:** Hack The Box · **Dificultad:** Medium · **SO:** Windows

---

## 📋 Resumen

Este repositorio contiene un **walkthrough completo y documentado** de la máquina **Logging** de Hack The Box (Season 10). Cubre desde la enumeración inicial hasta la obtención de la flag de root, incluyendo el análisis de cada vector de ataque, los comandos ejecutados y la lógica detrás de cada decisión.

El contenido está diseñado para ser útil tanto para principiantes que deseen aprender técnicas de pentesting en Active Directory como para profesionales que busquen un repaso estructurado.

---

## 🎯 Objetivos alcanzados

- ✅ **Revshell estable** – a través de **DLL Hijacking** sobre la tarea programada `UpdateMonitor`.
- ✅ **User flag** – capturada en el escritorio de `jaylee.clifton`.
- ✅ **Root flag** – capturada en el escritorio de `toby.brynleigh` mediante **WSUS Spoofing**.
- ✅ **Escalada de privilegios** – desde `wallace.everette` → `svc_recovery` → `msa_health$` → `jaylee.clifton` → `NT AUTHORITY\SYSTEM`.

---

## 🧰 Técnicas y herramientas utilizadas

| Técnica | Herramientas |
|---------|--------------|
| **Shadow Credentials** | Certipy, BloodHound, impacket-getTGT |
| **Kerberos autenticación** | getTGT.py, KRB5CCNAME |
| **DLL Hijacking** | msfvenom, evil-winrm, tareas programadas |
| **ADCS ESC1** | Certipy (template `UpdateSrv`) |
| **WSUS Spoofing** | wsuks, dnstool.py, Python HTTPServer |
| **Enumeración** | nmap, smbclient, BloodHound, ldapsearch |

---

## 📁 Estructura del repositorio
