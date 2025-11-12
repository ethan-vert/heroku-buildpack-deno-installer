# Deno Installer Buildpack

A minimal Heroku buildpack that installs Deno for use as a JavaScript runtime dependency (e.g., for yt-dlp).

## Usage

Add this buildpack **before** your Python buildpack:

```bash
heroku buildpacks:add --index 1 https://github.com/YOUR_USERNAME/heroku-buildpack-deno-installer.git
```

Or if hosting elsewhere, replace the URL.

## What It Does

1. Downloads and installs Deno to `/app/.deno`
2. Creates `/app/.profile.d/deno.sh` to add Deno to PATH at runtime
3. Verifies the installation

## Requirements

- Heroku stack: heroku-20 or later
- Works with any language buildpack (Python, Node.js, etc.)

## Installation Location

- Deno binary: `/app/.deno/bin/deno`
- Available in PATH via `.profile.d/deno.sh`

