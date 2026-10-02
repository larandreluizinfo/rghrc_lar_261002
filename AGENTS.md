# AGENTS.md — Regras obrigatórias para agentes

## 1. Regra de commit + push automático (OBRIGATÓRIA)

Toda alteração feita neste repositório — criar, editar, renomear, mover ou excluir arquivos — DEVE ser commitada e pushada.

Fluxo obrigatório ao final de qualquer tarefa com alteração em arquivos:

1. `git status` para conferir o que mudou
2. `git add -A`
3. `git commit -m "<tipo>: <descrição curta>"` (ex: `feat: ...`, `fix: ...`, `docs: ...`, `chore: ...`)
4. `git push origin main` (ou para a branch atual, se diferente de `main`)
5. Confirmar com `git status` que a working tree está limpa

Proibido:
- Deixar alterações apenas locais sem commit/push
- Acumular várias tarefas sem commitar entre elas — commite ao concluir cada unidade de trabalho
- Usar `git push --force` sem autorização explícita do usuário

Se o push falhar (ex: remote divergiu), faça `git pull --rebase origin main`, resolva conflitos e repita commit/push. Se não conseguir resolver, reporte o erro ao usuário.

## 2. Convenções

- Branch principal: `main`
- Commits em português ou inglês, curtos e descritivos
- Nunca commitar segredos (`.env`, tokens, senhas)
- Respeitar o `.gitignore`
