# my-airdrop

Share files over your network — like AirDrop, but from your terminal.

```
npx my-airdrop
```

Opens a beautiful web interface anyone can access by scanning a QR code. Upload and download files between your computer and any device — no app, no account, no cable.

## Preview

```
  ◆ my-airdrop

  How do you want to share?

  ●  Local   — same WiFi only
  ○  Public  — accessible from anywhere

  ↑↓ to move  ·  Enter to select
```

```
  ◆ my-airdrop

  Serving  ~/Desktop/projects

  Local    http://localhost:3000
  Network  http://192.168.1.5:3000
  Public   https://random-words.trycloudflare.com

  [QR CODE]

  QR → public URL (works outside local network)
  Ctrl+C to stop

  ────────────────────────────────────────────────

  17:22:12  ↓  192.168.1.10     README.md (2.1 KB)
  17:22:45  ↑  192.168.1.10     photo.jpg (3.4 MB)
```

## Features

- **Interactive mode** — arrow key menu to choose Local or Public on startup
- **Download** — browse and download files from any device
- **Upload** — send files from your phone to your computer (tap or drag & drop)
- **Folder download** — zip and download entire folders in one tap
- **Multi-select** — select multiple files and download as a single zip
- **QR code** — instantly connect any device with a camera
- **Public tunnel** — share outside your local network via a public URL
- **Mobile-optimized** — large touch targets, responsive layout, dark UI
- **Safety limits** — warns on large directories, hard stops at 5000 files / 5 GB

## Usage

Just run it and pick an option:

```bash
npx my-airdrop
```

Or pass options directly:

```bash
# Serve a specific folder
npx my-airdrop ./photos

# Share outside local network (generates a public Cloudflare URL)
npx my-airdrop --public

# Custom port
npx my-airdrop --port 8080

# Read-only (disable uploads)
npx my-airdrop --no-upload
```

## Public mode

With `--public`, a Cloudflare Quick Tunnel is created so anyone on the internet can access your files:

```
Public   https://random-words.trycloudflare.com
```

Share the URL with whoever you want to give access. No password required — just open and go.

## Install globally

```bash
npm install -g my-airdrop
my-airdrop
```

## Requirements

- Node.js >= 14
- For local mode: both devices on the same WiFi
- For public mode: internet connection

## License

MIT
