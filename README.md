# clawd-note
Clawdnote es un mini notion para Linux, pero mas sencillo y con varios presets visuales. basado en la mascota "Claw'd" de anthropic.
# Tutorial — Instalar Clawdnote con Chromium (sin npm, sin Electron)

## Requisitos

Un navegador basado en Chromium. Si no tienes ninguno, instálalo según tu distro:

**Arch / Manjaro / EndeavourOS**
```bash
sudo pacman -S chromium
```

**Debian / Ubuntu / Linux Mint / Pop!_OS**
```bash
sudo apt update && sudo apt install -y chromium
```

**Kali Linux**
```bash
sudo apt update && sudo apt install -y chromium
```

**Fedora**
```bash
sudo dnf install -y chromium
```

**openSUSE Leap / Tumbleweed**
```bash
sudo zypper install -y chromium
```

> También funciona con Chrome, Brave, Vivaldi o Edge si ya los tienes instalados.

---

## Instalación

```bash
cd ~/Downloads/clawdnote-app
./install.sh
clawdnote
```

Eso es todo. El script:
- Copia la app a `~/.local/share/clawdnote-app`
- Crea el comando `clawdnote` en `~/.local/bin`
- Registra el ícono y la entrada en el menú de aplicaciones

---

## Si `clawdnote` no se reconoce

Significa que `~/.local/bin` no está en tu PATH. Un solo comando lo arregla:

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc && source ~/.bashrc
clawdnote
```

---

## Desinstalar

```bash
cd ~/Downloads/clawdnote-app
./uninstall.sh
```

Tus datos se guardan en `~/.local/share/clawdnote/` y **no se borran** al desinstalar.
Para borrarlos también:

```bash
rm -rf ~/.local/share/clawdnote
```
