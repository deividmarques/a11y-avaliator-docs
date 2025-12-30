# A11y Avaliator Web

Extensão Chrome para avaliação completa de acessibilidade web com análise automática baseada em WCAG 2.2, testes de teclado e leitor de tela.

## 🎯 Funcionalidades

- ✅ **Análise automática de acessibilidade** com base nos níveis WCAG (A, AA, AAA) usando axe-core
- 🔍 **Detecção de violações** de acessibilidade em páginas web com impacto (crítico, sério, moderado, menor)
- ⌨️ **Teste de navegação por teclado**: detecta elementos sem indicador de foco, tabindex problemático e possíveis keyboard traps
- 🗣️ **Teste de leitor de tela** com 4 modos:
  - **Minimalista**: apenas problemas críticos
  - **Conservadora**: críticos, sérios e moderados (recomendada)
  - **Abrangente**: todos os problemas automáticos
  - **Educativa**: inclui dicas e boas práticas
- 🎨 **Teste de contraste interativo**: valida contraste em ícones, bordas e estados hover/focus/active/disabled
- 📊 **Score de acessibilidade** que considera axe-core + testes de teclado, leitor de tela e contraste
- 📥 **Exportação de relatórios** em JSON e PDF com layout profissional
- 🎨 Interface moderna e responsiva construída com React + TypeScript
- 📖 Documentação detalhada sobre cada teste e modo disponível

## 🛠️ Tecnologias Utilizadas

- **Vite**: Build tool moderna e rápida
- **React 19**: Biblioteca para construção de interfaces
- **TypeScript**: Tipagem estática para maior segurança
- **axe-core**: Engine de teste de acessibilidade da Deque Systems
- **Chrome Extension Manifest V3**: Para integração com o navegador Chrome
- **CSS Variables**: Sistema de cores preparado para temas

## 📚 Documentação

### 📖 Documentação Online

Acesse a documentação completa e interativa em:

**🌐 [https://deividmarques.github.io/a11y-avaliator-docs/](https://deividmarques.github.io/a11y-avaliator-docs/)**

A documentação inclui:
- 📦 Guia de instalação completo
- 🚀 Tutorial passo a passo de uso
- ✨ Detalhes de todos os recursos
- 🔧 API do @a11y/core package
- 🤝 Guia para contribuidores

### 📁 Documentação Local

- [`TESTE_LEITOR_DE_TELA.md`](./TESTE_LEITOR_DE_TELA.md): Guia completo sobre o teste de leitor de tela, os 4 modos disponíveis e como interpretar os resultados
- [`TESTE_CONTRASTE.md`](./TESTE_CONTRASTE.md): Guia detalhado sobre o teste de contraste interativo, estados validados e critérios WCAG
- [`COMO_FUNCIONA_A_ANALISE.md`](./COMO_FUNCIONA_A_ANALISE.md): Detalhes técnicos sobre como a análise é executada
- [`PROJECT_SUMMARY.md`](./PROJECT_SUMMARY.md): Resumo do projeto e arquitetura
- [`USAGE_GUIDE.md`](./USAGE_GUIDE.md): Guia de uso detalhado

### 🛠️ Desenvolvendo a Documentação

```bash
# Editar arquivos fonte em docs-src/
# Gerar build da documentação
npm run build:docs

# Deploy para GitHub Pages
npm run deploy:docs
```

## 📦 Instalação e Desenvolvimento

### Pré-requisitos

- Node.js 18+ e npm

### Passos

1. Clone o repositório:
```bash
git clone https://github.com/deividmarques/a11y-avaliator-web.git
cd a11y-avaliator-web
```

2. Instale as dependências:
```bash
npm install
```

3. Execute em modo de desenvolvimento:
```bash
npm run dev
```

4. Para fazer build da extensão:
```bash
npm run build
```

## 🔧 Carregar a Extensão no Chrome

1. Execute o build da extensão:
```bash
npm run build
```

2. Abra o Chrome e vá para `chrome://extensions/`

3. Ative o "Modo do desenvolvedor" no canto superior direito

4. Clique em "Carregar sem compactação"

5. Selecione a pasta `dist` que foi gerada pelo build

6. A extensão "A11y Avaliator" aparecerá na barra de extensões!

## 🎮 Como Usar

1. Navegue até qualquer página web que você deseja analisar

2. Clique no ícone da extensão "A11y Avaliator" na barra de ferramentas

3. Configure os testes desejados:
   - Selecione o nível WCAG (A, AA ou AAA)
   - ✅ **Incluir teste de teclado**: verifica navegação por teclado
   - ✅ **Incluir teste de leitor de tela**: escolha o modo (conservadora, abrangente, educativa ou minimalista)
   - ✅ **Incluir teste de contraste interativo**: valida contraste em estados hover/focus/disabled

4. Clique em "Analisar Página Atual"

5. Visualize o relatório completo com:
   - **Score de acessibilidade** (0-100) com código de cores
   - **Violações do axe-core** com impacto, descrição e elementos afetados
   - **Teste de teclado** (se habilitado): elementos sem foco, tabindex e traps
   - **Teste de leitor de tela** (se habilitado): nomes acessíveis, aria-hidden, refs quebradas, landmarks e alt
   - **Teste de contraste** (se habilitado): contraste de texto, ícones, bordas e estados interativos
   - Links para documentação WCAG e ARIA

6. Exporte o relatório:
   - **📥 Exportar JSON**: dados estruturados para análise
   - **📝 Exportar PDF**: relatório visual formatado

## 📋 Estrutura do Projeto

```
├── public/
│   ├── manifest.json      # Manifesto da extensão Chrome (MV3)
│   └── icon-*.png         # Ícones da extensão
├── docs/                  # Documentação GitHub Pages (gerado)
├── docs-src/              # Fonte da documentação
│   ├── index.html         # Página principal da documentação
│   └── styles.css         # Estilos da documentação
├── scripts/
│   ├── update-version.js  # Script de versionamento automático
│   ├── build-docs.js      # Build da documentação
│   └── deploy-docs.sh     # Deploy automático para GitHub Pages
├── src/
│   ├── components/        # Componentes React
│   │   ├── ConfigForm.tsx       # Formulário de configuração e testes
│   │   ├── ConfigForm.css       # Estilos do formulário
│   │   ├── ResultsDisplay.tsx   # Exibição completa de resultados
│   │   └── ResultsDisplay.css   # Estilos dos resultados e PDF
│   ├── analyzer.ts        # Lógica de análise com axe-core, testes de teclado e leitor de tela
│   ├── background.ts      # Service worker (background script)
│   ├── content.ts         # Content script para injeção
│   ├── types.ts           # Definições de tipos TypeScript
│   ├── App.tsx            # Componente principal do popup
│   └── main.tsx           # Ponto de entrada
├── build-version.txt      # Versão atual do build
├── vite.config.ts         # Configuração do Vite
└── package.json           # Dependências e scripts
```

## 🚀 Roadmap

### ✅ Implementado
- [x] Análise básica de acessibilidade WCAG 2.2 (A, AA, AAA)
- [x] Interface de usuário responsiva com React + TypeScript
- [x] Relatórios detalhados de violações com impacto e documentação
- [x] **Testes de navegação por teclado** (foco, tabindex, traps)
- [x] **Testes com leitores de tela** (4 modos: minimalista, conservadora, abrangente, educativa)
- [x] **Teste de contraste interativo** (ícones, bordas, estados hover/focus/active/disabled)
- [x] **Score de acessibilidade** integrado (axe + teclado + leitor de tela + contraste)
- [x] **Exportação de relatórios** (JSON e PDF com layout profissional)
- [x] **Temas dark/light mode** com persistência no navegador
- [x] Documentação completa dos testes (`TESTE_LEITOR_DE_TELA.md`)
- [x] Sistema de versionamento automático
- [x] Variáveis CSS para suporte a temas

### 🔜 Próximas Funcionalidades
- [ ] Histórico de análises com armazenamento local
- [ ] Análise de múltiplas páginas (batch)
- [ ] Sugestões de correção automatizadas com snippets de código
- [ ] Comparação entre análises (antes/depois)
- [ ] Integração com CI/CD para testes automatizados
- [ ] Extensão para Firefox

## 📄 Licença

Este projeto está sob a licença MIT.

## 👥 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## 📞 Contato

Para dúvidas ou sugestões, abra uma issue no GitHub.

