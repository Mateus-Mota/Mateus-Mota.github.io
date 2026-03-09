---
title: "Visualizing our Dockerized Dev Environment"
date: 2026-03-09 02:00:00 -0300
categories: [DevOps, Docker]
tags: [mermaid, infrastructure, containers]
mermaid: true
---

## Cloud vs Local Workflow
Este diagrama confirma se o motor Mermaid está ativo no servidor:

```mermaid
graph TD
    A[Git Push] --> B{GitHub Actions}
    B -->|Build| C[GitHub Pages]
    C -->|Render| D["mateusmota.com.br"]