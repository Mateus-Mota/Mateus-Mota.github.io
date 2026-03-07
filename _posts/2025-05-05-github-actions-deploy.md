---
layout: post
title: "Automatizando Deploys com GitHub Actions: Um Guia Prático para Projetos Pessoais"
date: 2025-05-05 20:00:00 +0000
categories: [DevOps, GitHub]
tags: [github-actions, ci-cd, automação, deploy]
---

Você já quis automatizar o deploy do seu projeto sem depender de ferramentas externas? Com o **GitHub Actions**, isso é possível — de forma gratuita e integrada ao seu repositório. Neste artigo, vamos criar uma pipeline básica para rodar testes e publicar seu site automaticamente no GitHub Pages, com exemplos práticos e visuais.

---

## 🚀 O que é o GitHub Actions?

O **GitHub Actions** é uma plataforma de automação nativa do GitHub que permite executar tarefas como build, testes e deploy com base em gatilhos (push, pull request, etc.).

Você cria fluxos de trabalho (workflows) usando arquivos `.yml` no diretório `.github/workflows/` do seu repositório.

---

## 🧱 Estrutura de um Workflow

Um workflow é dividido em:

- **`on`**: evento que dispara a ação
- **`jobs`**: grupos de etapas
- **`steps`**: comandos executados

Exemplo:

```yaml
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Rodar script
        run: echo "Olá, GitHub Actions!"
