# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal website for **pcdkd.fyi**, hosted on GitHub Pages. It serves as Daniel Dewar's personal site with Lightning Network and Nostr protocol integrations.

## Architecture

- **Hosting**: GitHub Pages with a custom domain (`pcdkd.fyi` via `CNAME`)
- **Static HTML**: Single-page site (`index.html`) — inline CSS with Emotion-style class names, originally generated from a Next.js/Hugo build but now maintained as static HTML
- **Jekyll config**: `_config.yml` includes the `.well-known` directory so GitHub Pages serves it (Jekyll ignores dotfiles by default)
- **`.nojekyll`**: Present but `_config.yml` is also used — both exist to ensure `.well-known` files are served correctly

## Well-Known Endpoints

- **`.well-known/lnurlp/pcdkd`**: LNURL-pay endpoint (proxied from Alby) enabling Lightning Address `pcdkd@pcdkd.fyi`
- **`.well-known/nostr.json`**: NIP-05 Nostr verification mapping `pcdkd` to a Nostr public key

## Development

No build step — edit files directly. To preview locally, serve the directory with any static file server (e.g., `python3 -m http.server`).
