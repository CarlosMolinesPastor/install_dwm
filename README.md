# 🍚 Rice Setup Script — dwm + st + Gazelle TUI

Script de instalación automática para un entorno **dwm** minimalista y funcional en **Arch Linux** (y derivados). Instala dependencias, fuentes Nerd, plugins de Zsh, y compila **dwm** y **st** desde el código fuente.

> ⚠️ **Experimental** — Úsalo bajo tu propio riesgo. Siempre puedes revisar el código antes de ejecutarlo.

---

## 📋 Tabla de contenidos

- [Características](#-características)
- [Requisitos](#-requisitos)
- [Instalación rápida](#-instalación-rápida)
- [¿Qué hace el script?](#-qué-hace-el-script)
- [Dependencias instaladas](#-dependencias-instaladas)
- [Post-instalación](#-post-instalación)
- [Personalización](#-personalización)
- [Atajos de dwm](#-atajos-de-dwm)
- [Créditos](#-créditos)
- [Licencia](#-licencia)

---

## ✨ Características

- ✅ Instala **paru** (AUR helper) si no está presente.
- ✅ Instala todas las dependencias necesarias vía `pacman` y `paru`/`yay`.
- ✅ Descarga e instala **Nerd Fonts** (JetBrainsMono, CascadiaCode, Iosevka, Noto).
- ✅ Clona y sincroniza los **dotfiles** desde `linuxmobile/dwm-dots`.
- ✅ Compila e instala **dwm** y **st** desde el código fuente.
- ✅ Configura **Oh-My-Zsh** con plugins (autosuggestions, syntax-highlighting, completions).
- ✅ Instala **Gazelle TUI** para gestionar redes WiFi desde la terminal.
- ✅ Añade **NetworkManager** y **nm-applet** para notificaciones de red.
- ✅ Usa **st** como terminal principal (ligero, minimalista, Xorg).

---

## 📦 Requisitos

- **Distribución:** Arch Linux, Artix, EndeavourOS o Manjaro (basadas en Arch).
- **Usuario con sudo:** El script usará `sudo` para instalar paquetes y copiar fuentes.
- **Conexión a Internet:** Necesaria para descargar dependencias, fuentes y repositorios.
- **Git:** Debe estar instalado (`sudo pacman -S git`).
- **whiptail** (libnewt): El script lo instala automáticamente si no está.

---

## 🚀 Instalación rápida

Puedes clonar el repositorio y ejecutar el script manualmente:

```bash
git clone https://github.com/CarlosMolinesPastor/install_dwm.git
cd install_dwm
chmod +x install.sh
./install.sh
