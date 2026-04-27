---
title: Sincronizar com um vault grande (Obsidian)
tags:
  - estudo/rust-study
  - meta/obsidian
---

# Sincronizar com um vault grande

Objetivo: manter **este estudo** como unidade própria (Git, pastas) e ainda
**aparecer no vault principal** agrupado por **tema**.

## Convenção de tags

Use sempre estes prefixos nas notas deste estudo:

- `#estudo/rust-study` — tudo que pertence a este repo
- `#tema/rust` — agrupa no vault grande por assunto

No vault principal, uma consulta ou MOC por `#tema/rust`
lista o que você estudou nesse tema.

## Opção A — Pasta dentro do vault (recomendado)

1. No vault grande, crie algo como `Estudos/rust-study/`.
2. **Copie** ou **sincronize** (rsync, script) o conteúdo deste repositório para
   essa pasta.
3. Ou use **submodule Git** / **subtree** se o vault também é um repo.

Vantagem: um único Obsidian; busca global; grafo unificado.

## Opção B — Link simbólico

Se o vault grande está em disco local:

```bash
ln -s /caminho/para/rust-study \
  /caminho/do/vault-grande/Estudos/rust-study
```

Cuidado: caminhos absolutos e backups (alguns syncers não seguem symlink).

## Opção C — Vault separado + Obsidian

Abra esta pasta como vault **ou** use o plugin **Obsidian Git** só aqui.
No vault grande, mantenha um MOC que **linka** para exportações (PDF/HTML) ou
para o repositório remoto — menos integração, mais isolamento.

## Mapa no vault grande

Crie uma nota `MOC — tema rust` no vault grande e
liste links para `[[../Estudos/rust-study/00-Dashboard]]`
(ajuste o caminho relativo conforme a estrutura).
