# Changelog

## 0.1.0 — 2026-11-13

**Base do projeto no ar na VPS**

### Entregues

- App Next.js 16 com React 19 e TypeScript 5.6, usando App Router
- Página inicial "Reforma Fácil — em breve" (mobile-first, sem largura fixa, fonte legível)
- Configuração Next.js com output `standalone` para Docker
- ESLint com flat config (next/core-web-vitals e next/typescript)
- Script `type-check` com `tsc --noEmit`
- Dockerfile multi-stage (deps, builder, runner em node:22-alpine) com usuário não-root, porta 3000
- `.gitignore` cobrindo node_modules/, .next/, out/, *.tsbuildinfo, .env*
- `.dockerignore` excluindo node_modules, .git, .github, .env*, docs e .md
- `.nvmrc` fixando Node 22 (LTS)
- `tsconfig.json` com strict mode, moduleResolution bundler, paths @/*
- HTML com `lang="pt-BR"` e viewport de celular

### Infraestrutura

- Deploy via Dokploy com provider GitHub (branch main, Build Type Dockerfile, deploy automático a cada push)
- Sem workflows no CI ainda
- Sem banco de dados, login ou Prisma

### Remissões

- Não há imagem publicada no GHCR
- Não há webhook de deploy ou secret DOKPLOY_WEBHOOK_URL (será implementado em entrega futura)
