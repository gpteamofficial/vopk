# VOPK — One Package Command. Any Distro.

> Stop relearning package managers.  
> **VOPK gives you one command that works everywhere.**

Switching between distros?  
Managing multiple machines?  
Tired of remembering `apt` vs `pacman` vs `dnf` syntax?

**VOPK fixes that.**

```bash
# Debian, Arch, Fedora, Alpine, Void, Gentoo, macOS, BSD…
vopk install neovim
vopk remove firefox
vopk update
```

Same commands.  
Same behavior.  
No mental context switching.

---

## 🤔 What is VOPK?

**VOPK** is a **unified package manager frontend**.

It does **not** replace your system package manager.  
It **wraps it** with a clean, predictable CLI that works the same everywhere.

Think of it as:

> *“One interface on top of every package manager.”*

---

## 👤 Who is this for?

VOPK is for you if you:

- ✔ Use **multiple Linux distros**
- ✔ Hop between **Arch / Debian / Fedora / Alpine**
- ✔ Manage **servers, containers, VMs**
- ✔ Work across **Linux / macOS / BSD**
- ✔ Are a **beginner** confused by package managers
- ✔ Just want things to **work the same everywhere**

If you only ever use one distro forever — you probably don’t need VOPK.  
If you touch more than one system — **you’ll feel it immediately**.

---

## 😖 The Problem

Every distro reinvents package management:

- `apt` on Debian / Ubuntu
- `pacman` on Arch
- `dnf` on Fedora
- `zypper` on openSUSE
- `apk` on Alpine
- `xbps` on Void
- `emerge` on Gentoo

Same actions.  
Different syntax.  
Different flags.  
Different habits.

Your brain pays the price.

---

## ✅ The Solution

**VOPK gives you one mental model.**

```bash
vopk install htop
vopk remove nginx
vopk update
vopk upgrade
```

That’s it.

Behind the scenes:
- On Debian → uses `apt`
- On Arch → uses `pacman`
- On Fedora → uses `dnf`
- On BSD → uses `pkg`
- On macOS → uses `brew`

You don’t care.  
VOPK handles it.

---

## ✨ Why people like VOPK

- ✅ **Same CLI everywhere**
- ✅ **Automatic backend detection**
- ✅ **Beginner-friendly output**
- ✅ **Safe defaults**
- ✅ **Dry-run mode that actually behaves**
- ✅ **Works on Linux, macOS, and BSD**
- ✅ **Single Bash script — no dependencies**
- ✅ **Does not hide backend errors**
- ✅ **Transparent and predictable**

No magic.  
No abstraction leaks.  
No surprises.

---

## 📦 Supported Backends

| Backend | Platforms |
|------|---------|
| `apt / apt-get` | Debian, Ubuntu, Mint, PopOS, Kali |
| `pacman` | Arch, Manjaro, Endeavour |
| `dnf` | Fedora |
| `yum` | RHEL / CentOS (legacy) |
| `zypper` | openSUSE |
| `apk` | Alpine |
| `xbps-install` | Void |
| `emerge` | Gentoo |
| `brew` | macOS (Homebrew) |
| `pkg` | FreeBSD |
| `pkgin / pkg_add` | NetBSD / OpenBSD |
| `dpkg` | Debian systems without apt |
| `vmpkg` | Optional fallback backend |

VOPK automatically selects the correct backend.

---

## 🚀 Installation

### One-liner (recommended)

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/gpteamofficial/vopk/main/src/installscript.sh)
```

### Without root (alternative)

```bash
curl -fsSL https://raw.githubusercontent.com/gpteamofficial/vopk/main/src/installscript.sh | sudo bash -s -- -y
```

---

## 🧠 Basic Usage

```bash
vopk update
vopk upgrade
vopk install neovim
vopk remove firefox
vopk search docker
vopk show git
```

### Short aliases (optional)

```bash
vopk i  neovim
vopk rm firefox
vopk up
vopk fu
vopk s  nginx
```

---

## 🔍 Dry-run mode (safe preview)

```bash
vopk install docker --dry-run
```

- No changes
- No prompts
- No surprises

---

## 🛠 Power-user mode (raw backend access)

```bash
vopk backend install -y htop
vopk script-v -Syu
```

You get **one entry point**, but **full control** when you need it.

---

## 🧰 Extra Helpers (Optional)

```bash
vopk doctor
vopk sys-info
vopk kernel
vopk disk
vopk mem
vopk fix-dns
vopk install-dev-kit
```

Useful on minimal systems, containers, or fresh installs.

---

## 🧱 Design Philosophy

- **Unified** — one CLI everywhere  
- **Transparent** — never hides what backend does  
- **Safe** — conservative defaults  
- **Predictable** — no distro-specific surprises  
- **Human-friendly** — readable output, sane behavior  

VOPK treats you like someone who wants control — not babysitting.

---

## 🧪 What VOPK is NOT

- ❌ Not a new package format
- ❌ Not a replacement for native package managers
- ❌ Not magic
- ❌ Not a dependency resolver

It’s a **frontend**.  
A good one.

---

## 💚 Project Info

- Developed by **GP Team** with ❤
- Current stable series: **1.x**
- License: **GPL-3.0**

---

## ⭐ Like it?

- ⭐ Star the repo  
- 🐛 Open issues  
- 📣 Share it  
- 📦 Package it for your distro  

If VOPK saved you mental energy — it did its job.

Happy packaging :)
