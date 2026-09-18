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
- ✅ Clona y sincroniza **tus dotfiles** desde `CarlosMolinesPastor/dwm-dots`.
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
```

## 🛠️ ¿Qué hace el script?

El script sigue estos pasos, en orden:

1. **Preflight** — Verifica que estás en una distro basada en Arch e instala `whiptail` si falta.
2. **Aviso y bienvenida** — Muestra diálogos de confirmación con `whiptail`.
3. **Instalación de paru** — Si no está, lo clona desde AUR y lo compila.
4. **Descarga de dependencias** — Instala todos los paquetes necesarios (ver lista abajo).
5. **Instalación de Zsh + Oh-My-Zsh** — Configura Zsh como shell e instala Oh-My-Zsh.
6. **Clonación de plugins de Oh-My-Zsh** — Añade `fast-syntax-highlighting`, `zsh-autosuggestions` y `zsh-completions`.
7. **Descarga de Nerd Fonts** — Baja las fuentes desde GitHub y las descomprime.
8. **Copia de fuentes** — Las instala en `/usr/share/fonts/`.
9. **Sincronización de dotfiles** — Clona `CarlosMolinesPastor/dwm-dots` y copia los archivos a `$HOME`.
10. **Compilación de dwm** — Entra en `~/lnxdwm/` y ejecuta `sudo make install`.
11. **Compilación de st** — Entra en `~/st/` y ejecuta `sudo make install`.
12. **Refresco de caché de fuentes** — Ejecuta `fc-cache -rv`.
13. **Finalización** — Limpia archivos temporales y muestra mensaje de éxito.
