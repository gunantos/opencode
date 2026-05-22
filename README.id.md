# OpenCode

<p align="center">
  <a href="https://opencode.ai">
    <picture>
      <source srcset="packages/console/app/src/asset/logo-ornate-dark.svg" media="(prefers-color-scheme: dark)">
      <source srcset="packages/console/app/src/asset/logo-ornate-light.svg" media="(prefers-color-scheme: light)">
      <img src="packages/console/app/src/asset/logo-ornate-light.svg" alt="Logo OpenCode">
    </picture>
  </a>
</p>

<p align="center">
  Agen AI open source untuk coding.
</p>

<p align="center">
  <a href="https://opencode.ai/discord">
    <img alt="Discord" src="https://img.shields.io/discord/1391832426048651334?style=flat-square&label=discord" />
  </a>
  <a href="https://www.npmjs.com/package/opencode-ai">
    <img alt="npm" src="https://img.shields.io/npm/v/opencode-ai?style=flat-square" />
  </a>
  <a href="https://github.com/anomalyco/opencode/actions/workflows/publish.yml">
    <img alt="Status Build" src="https://img.shields.io/github/actions/workflow/status/anomalyco/opencode/publish.yml?style=flat-square&branch=dev" />
  </a>
</p>

---

[![OpenCode Terminal UI](packages/web/src/assets/lander/screenshot.png)](https://opencode.ai)

---

## Instalasi

```bash
# Cara cepat (YOLO)
curl -fsSL https://opencode.ai/install | bash

# Menggunakan package manager
npm i -g opencode-ai@latest        # atau bun/pnpm/yarn
scoop install opencode             # Windows
choco install opencode             # Windows
brew install anomalyco/tap/opencode # macOS dan Linux (direkomendasikan, selalu terbaru)
brew install opencode              # macOS dan Linux (formula resmi brew, update lebih lambat)
sudo pacman -S opencode            # Arch Linux (Stable)
paru -S opencode-bin               # Arch Linux (Versi terbaru dari AUR)
mise use -g opencode               # Semua OS
nix run nixpkgs#opencode           # atau github:anomalyco/opencode untuk branch dev terbaru
```

> [!TIP]
> Hapus versi di bawah `0.1.x` sebelum melakukan instalasi.

---

## Aplikasi Desktop (BETA)

OpenCode juga tersedia sebagai aplikasi desktop.
Unduh langsung melalui:

* [https://github.com/anomalyco/opencode/releases](https://github.com/anomalyco/opencode/releases)
* [https://opencode.ai/download](https://opencode.ai/download)

| Platform              | File Download                      |
| --------------------- | ---------------------------------- |
| macOS (Apple Silicon) | `opencode-desktop-mac-arm64.dmg`   |
| macOS (Intel)         | `opencode-desktop-mac-x64.dmg`     |
| Windows               | `opencode-desktop-windows-x64.exe` |
| Linux                 | `.deb`, `.rpm`, atau `.AppImage`   |

```bash
# macOS (Homebrew)
brew install --cask opencode-desktop

# Windows (Scoop)
scoop bucket add extras
scoop install extras/opencode-desktop
```

---

## Direktori Instalasi

Script instalasi menggunakan prioritas lokasi berikut:

1. `$OPENCODE_INSTALL_DIR` — Direktori instalasi custom
2. `$XDG_BIN_DIR` — Path sesuai standar XDG Base Directory
3. `$HOME/bin` — Direktori binary user standar
4. `$HOME/.opencode/bin` — Lokasi default fallback

Contoh:

```bash
OPENCODE_INSTALL_DIR=/usr/local/bin curl -fsSL https://opencode.ai/install | bash

XDG_BIN_DIR=$HOME/.local/bin curl -fsSL https://opencode.ai/install | bash
```

---

## Agents

OpenCode memiliki dua agent bawaan yang dapat diganti menggunakan tombol `Tab`.

### build

Agent default dengan akses penuh untuk pekerjaan development.

### plan

Agent read-only untuk analisis dan eksplorasi kode.

Fitur:

* Menolak edit file secara default
* Meminta izin sebelum menjalankan perintah bash
* Cocok untuk mempelajari codebase atau merencanakan perubahan

---

Selain itu tersedia juga sub-agent:

### general

Digunakan untuk pencarian kompleks dan tugas multi-step.

Bisa dipanggil menggunakan:

```text
@general
```

Pelajari lebih lanjut tentang agents:

[https://opencode.ai/docs/agents](https://opencode.ai/docs/agents)

---

## Dokumentasi

Untuk informasi konfigurasi dan penggunaan lebih lanjut:

[https://opencode.ai/docs](https://opencode.ai/docs)

---

## Kontribusi

Jika ingin berkontribusi ke OpenCode, baca dokumentasi kontribusi terlebih dahulu sebelum membuat pull request:

```text
./CONTRIBUTING.md
```

---

## Membangun di Atas OpenCode

Jika Anda membuat project yang menggunakan nama “opencode” seperti:

* opencode-dashboard
* opencode-mobile

mohon tambahkan catatan pada README bahwa project tersebut:

* bukan dibuat oleh tim OpenCode
* tidak memiliki afiliasi resmi dengan OpenCode

---

## Bergabung dengan Komunitas

* Discord: [https://discord.gg/opencode](https://discord.gg/opencode)
* X / Twitter: [https://x.com/opencode](https://x.com/opencode)
