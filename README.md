# Diretório de Documentação (GitHub Pages)

Este diretório contém os arquivos estáticos gerados para o GitHub Pages.

**⚠️ NÃO EDITE ARQUIVOS AQUI DIRETAMENTE**

Os arquivos são gerados automaticamente a partir de `docs-src/` usando:

```bash
npm run build:docs
```

## Configuração do GitHub Pages

No repositório `a11y-avaliator-docs`:

1. Acesse **Settings** > **Pages**
2. Em **Source**, selecione:
   - Branch: `gh-pages`
   - Folder: `/ (root)`
3. Clique em **Save**

A documentação estará disponível em:
```
https://deividmarques.github.io/a11y-avaliator-docs/
```

## Estrutura

```
docs/
├── index.html          # Página principal
├── styles.css          # Estilos
├── README.md           # Este arquivo
├── CHANGELOG.md        # Histórico de versões
├── .nojekyll           # Desabilita processamento Jekyll
└── assets/             # Recursos (imagens, etc)
```
