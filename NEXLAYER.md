# Nexlayer — cyberpunk-pong-game

<!-- nexlayer:meta version=1 analyzed=2026-06-16T18:34:56Z repo=https://github.com/KatieHarris2397/cyberpunk-pong-game branch=main -->

> **For AI agents (Claude Code, Cursor, Gemini CLI, Copilot):**
> This file is the **project context** for this Nexlayer deployment — tech stack, env vars, secrets, live URL.
> For full platform detail (nexlayer.yaml schema, Dockerfile rules, CI/CD, task recipes) read **`nexlayer.skills`** in this repo.
>
> **Critical rules (full detail in `nexlayer.skills`):**
> - Inter-pod refs: `${podName:port}` only — never `localhost` or bare hostnames
> - Docker Hub images: prefix with `mirror.gcr.io/library/` — bare tags fail on the cluster
> - Secrets: set in the Nexlayer dashboard — never commit to `nexlayer.yaml` or Dockerfile
>
> **This file:** `agent-managed` sections update automatically. `user-editable` sections (Local Development Setup, Nexlayer Deployment Plan, Build Notes) are yours — preserved across re-analysis.

## Project Summary
<!-- nexlayer:section agent-managed=project_summary -->
A cyberpunk-themed Pong game featuring neon aesthetics, particle effects, and an AI opponent, built using vanilla JavaScript and HTML5 Canvas.
<!-- nexlayer:end -->

## Technology Stack
<!-- nexlayer:section agent-managed=tech_stack -->
| Name | Kind | Version | Detected From |
|------|------|---------|---------------|
| HTML5 | language | 5 | index.html |
| CSS3 | language | 3 | style.css |
| JavaScript | language | ES6+ | script.js |
| Nginx | infra | alpine | Dockerfile |
<!-- nexlayer:end -->

## Repository Structure
<!-- nexlayer:section agent-managed=structure_map -->
- root — Project root containing static assets and configuration
- index.html — Main entry point and game canvas layout
- style.css — Cyberpunk styling and neon animations
- script.js — Core game logic, AI, and rendering engine
- Dockerfile — Containerization for Nginx static hosting
<!-- nexlayer:end -->

## External Services Required
<!-- nexlayer:section agent-managed=external_deps -->
_No external services detected._
<!-- nexlayer:end -->

## Local Development Setup
<!-- nexlayer:section user-editable=local_setup -->
### Prerequisites

- Modern Web Browser

### Steps

1. `open index.html` — Launch the game directly in any modern browser

<!-- nexlayer:end -->

## Nexlayer Setup
<!-- nexlayer:section agent-managed=nexlayer_setup -->
### nexlayer.yaml

```yaml
application:
  name: cyberpunk-pong-game
  pods:
    - name: "web"
      image: "registry.nexlayer.io/nexlayer-mcp/katieharris2397/cyberpunk-pong-game:38e30e1"
      path: "/"
      servicePorts: [80]
```
<!-- nexlayer:end -->

## Nexlayer Deployment Plan
<!-- nexlayer:section user-editable=deployment_plan -->
### Pod Topology

| Pod | Image | Port | Role |
|-----|-------|------|------|
| game-frontend | mirror.gcr.io/library/nginx:alpine | 80 | web |

### Deployment notes

- Static assets are served via Nginx; no backend or database required for this application.

<!-- nexlayer:end -->

## Build Notes
<!-- nexlayer:section user-editable=build_notes -->
<!-- Add notes for future builds here — preserved across re-analysis -->
<!-- nexlayer:end -->

## Nexlayer Configuration
<!-- nexlayer:section agent-managed=nexlayer_config -->
**Last deployed:** 2026-06-17T23:26:36Z  
**Live URL:** https://kitbear-studio-cyberpunk-pong-game.cloud.nexlayer.ai  
**Runtime:**  · **Port:** auto-detected  
**Deploy branch:** nexlayer  

```yaml
application:
  name: cyberpunk-pong-game
  pods:
    - name: "web"
      image: "registry.nexlayer.io/nexlayer-mcp/katieharris2397/cyberpunk-pong-game:38e30e1"
      path: "/"
      servicePorts: [80]
```
<!-- nexlayer:end -->

## Build History
<!-- nexlayer:section agent-managed=build_history -->
| Date | Status | Notes |
|------|--------|-------|
| 2026-06-17T23:25:48Z | analyzed | initial repo analysis |
| 2026-06-17T23:26:36Z | success | deployed https://kitbear-studio-cyberpunk-pong-game.cloud.nexlayer.ai |
<!-- nexlayer:end -->

