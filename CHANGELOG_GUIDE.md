# Sistema de Changelog Automático

Este projeto utiliza um sistema automatizado de changelog que é atualizado a cada build.

## Como Funciona

### 1. Build Automático

Quando você executa `npm run build`, o sistema:

1. ✅ Compila TypeScript
2. ✅ Gera o build com Vite
3. ✅ Copia manifest e recursos
4. ✅ **Incrementa a versão** (0.1.59 → 0.1.60)
5. ✅ **Cria entrada no CHANGELOG.md** automaticamente

### 2. Estrutura do CHANGELOG

Cada versão segue o formato:

```markdown
## [0.1.60] - 2025-12-28

### 🚀 Novidades
- Nova funcionalidade X
- Feature Y implementada

### ✨ Melhorias
- Performance otimizada em Z
- UI melhorada

### 🐛 Correções
- Bug A corrigido
- Problema B resolvido

### 📦 Build
- Build automático versão 0.1.60
- Data: 2025-12-28
```

## Uso

### Opção 1: Automático (Recomendado para CI/CD)

```bash
npm run build
```

Gera uma entrada com template básico que pode ser editada depois.

### Opção 2: Interativo (Recomendado para desenvolvimento)

```bash
# 1. Faça o build primeiro
npm run build

# 2. Adicione notas detalhadas
npm run changelog:add
```

O script interativo vai perguntar:
- 🚀 **Novidades**: Features novas
- ✨ **Melhorias**: Otimizações e melhorias
- 🐛 **Correções**: Bugs corrigidos
- 📦 **Build**: Informações técnicas do build

### Opção 3: Manual

Edite diretamente o `CHANGELOG.md`:

```bash
# Após o build, edite o arquivo
vim CHANGELOG.md
```

## Exemplo de Fluxo de Trabalho

```bash
# 1. Desenvolver features
git checkout -b feature/nova-funcionalidade

# 2. Fazer commits
git add .
git commit -m "feat: adiciona nova funcionalidade"

# 3. Build (incrementa versão e cria entrada no changelog)
npm run build

# 4. Adicionar notas detalhadas (opcional)
npm run changelog:add

# 5. Revisar changelog
cat CHANGELOG.md | head -50

# 6. Commit do changelog
git add CHANGELOG.md build-version.txt
git commit -m "docs: atualiza changelog para v0.1.60"

# 7. Merge para develop/main
git push origin feature/nova-funcionalidade
```

## Arquivos Envolvidos

- **`CHANGELOG.md`**: Histórico de mudanças
- **`build-version.txt`**: Versão atual (auto-incrementada)
- **`scripts/update-version.js`**: Incrementa versão
- **`scripts/update-changelog.js`**: Adiciona entrada no changelog
- **`scripts/add-release-notes.js`**: Script interativo para notas

## Integração com GitHub Actions

O changelog é automaticamente atualizado em cada build do CI/CD:

```yaml
# .github/workflows/build.yml
- name: Build project
  run: npm run build
  
# Changelog é atualizado automaticamente
```

## Padrão Keep a Changelog

Seguimos o padrão [Keep a Changelog](https://keepachangelog.com/pt-BR/1.0.0/):

- **🚀 Novidades** (`Added`): Novas features
- **✨ Melhorias** (`Changed`): Mudanças em funcionalidades existentes
- **🐛 Correções** (`Fixed`): Correções de bugs
- **🗑️ Removido** (`Removed`): Features removidas
- **🔒 Segurança** (`Security`): Vulnerabilidades corrigidas

## Versionamento Semântico

Versão: `MAJOR.MINOR.PATCH`

- **MAJOR** (0.x.x): Mudanças incompatíveis
- **MINOR** (x.1.x): Novas features (compatíveis)
- **PATCH** (x.x.60): Correções de bugs

Atualmente incrementamos apenas o **PATCH** automaticamente.

## Dicas

✅ **Faça**: Commits pequenos e frequentes com changelog atualizado
✅ **Faça**: Use `npm run changelog:add` para releases importantes
✅ **Faça**: Revise o changelog antes de fazer merge

❌ **Evite**: Editar versões antigas no changelog
❌ **Evite**: Builds sem documentar as mudanças
❌ **Evite**: Incrementar versão manualmente
