# A11y Avaliator Web

[![Licença MIT](https://img.shields.io/badge/Licen%C3%A7a-MIT-blue.svg)](LICENSE)
[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-green.svg)](https://chrome.google.com/webstore)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue.svg)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-19-61dafb.svg)](https://react.dev/)

Extensão Chrome para avaliação completa de acessibilidade web com análise automática baseada em WCAG 2.2, testes de teclado, leitor de tela e contraste de cores.

## 🎯 Funcionalidades

- ✅ **Análise automática WCAG** usando axe-core para níveis A, AA e AAA
- 🔍 **Detecção inteligente de violações** com classificação por impacto (crítico, sério, moderado, menor)
- ⌨️ **Teste de navegação por teclado**: detecta elementos sem indicador de foco, tabindex problemático e keyboard traps
- 🗣️ **Teste de leitor de tela** com 4 modos especializados:
  - **Minimalista**: apenas problemas críticos
  - **Conservadora**: críticos, sérios e moderados (recomendada)
  - **Abrangente**: análise completa automática
  - **Educativa**: inclui dicas e boas práticas
- 🎨 **Teste de contraste interativo**: valida contraste em texto, ícones, bordas e estados (hover/focus/active/disabled)
- 📊 **Score de acessibilidade** (0-100) que integra todos os testes com pesos por severidade
- 📥 **Exportação profissional** em JSON e PDF com layout otimizado
- 🎨 **Interface moderna** construída com React 19 + TypeScript + Vite
- 🌐 **Documentação completa** online com 17 páginas de conteúdo

## 📚 Documentação Completa

### 🌐 Documentação Online

Acesse a documentação interativa com busca, navegação e exemplos práticos:

**📖 [https://deividmarques.github.io/a11y-avaliator-web-docs/](https://deividmarques.github.io/a11y-avaliator-web-docs/)**

#### 📑 Conteúdo da Documentação:

**Introdução & Conceitos**
- [Introdução à Acessibilidade Web](https://deividmarques.github.io/a11y-avaliator-web-docs/introducao-a11y.html) - Fundamentos, tipos de deficiência e princípios WCAG
- [Glossário de Termos](https://deividmarques.github.io/a11y-avaliator-web-docs/glossario.html) - 19 termos essenciais explicados

**Sobre o Plugin**
- [Sobre o A11y Avaliator](https://deividmarques.github.io/a11y-avaliator-web-docs/sobre-plugin.html) - Funcionalidades, tecnologias e privacidade
- [Como Usar](https://deividmarques.github.io/a11y-avaliator-web-docs/como-usar.html) - Guia completo passo a passo

**Testes Disponíveis**
- [Análise WCAG Automática](https://deividmarques.github.io/a11y-avaliator-web-docs/teste-wcag.html) - Como funciona o axe-core
- [Teste de Teclado](https://deividmarques.github.io/a11y-avaliator-web-docs/teste-teclado.html) - Navegação e foco visual
- [Teste de Leitor de Tela](https://deividmarques.github.io/a11y-avaliator-web-docs/teste-leitor-tela.html) - ARIA, landmarks e semântica
- [Teste de Contraste](https://deividmarques.github.io/a11y-avaliator-web-docs/teste-contraste.html) - Ratios WCAG e legibilidade
- [Sistema de Score](https://deividmarques.github.io/a11y-avaliator-web-docs/sistema-score.html) - Como é calculada a pontuação

**Guias Práticos**
- [Manual de Teste com Teclado](https://deividmarques.github.io/a11y-avaliator-web-docs/manual-teclado.html) - Passo a passo para testes manuais
- [Manual de Teste com Leitor de Tela](https://deividmarques.github.io/a11y-avaliator-web-docs/manual-leitor-tela.html) - Configuração e uso do NVDA
- [Top 10 Erros Mais Comuns](https://deividmarques.github.io/a11y-avaliator-web-docs/erros-comuns.html) - Problemas frequentes
- [Correções Práticas](https://deividmarques.github.io/a11y-avaliator-web-docs/correcoes.html) - Exemplos de código

**Recursos**
- [Ferramentas de Acessibilidade](https://deividmarques.github.io/a11y-avaliator-web-docs/ferramentas.html) - Lista completa de recursos
- [FAQ](https://deividmarques.github.io/a11y-avaliator-web-docs/faq.html) - Perguntas frequentes
- [Casos de Uso](https://deividmarques.github.io/a11y-avaliator-web-docs/casos-uso.html) - Cenários reais

### 📁 Documentação Local (Markdown)

Para referência offline, veja os arquivos na raiz do projeto:
- [`TESTE_LEITOR_DE_TELA.md`](./TESTE_LEITOR_DE_TELA.md) - Detalhes dos 4 modos de teste
- [`TESTE_CONTRASTE.md`](./TESTE_CONTRASTE.md) - Teste de contraste interativo
- [`COMO_FUNCIONA_A_ANALISE.md`](./COMO_FUNCIONA_A_ANALISE.md) - Arquitetura técnica
- [`PROJECT_SUMMARY.md`](./PROJECT_SUMMARY.md) - Resumo do projeto
- [`USAGE_GUIDE.md`](./USAGE_GUIDE.md) - Guia de uso detalhado

## 🛠️ Tecnologias Utilizadas

### Core Stack
- **[Vite](https://vitejs.dev/)** 6.0 - Build tool ultrarrápida com HMR
- **[React](https://react.dev/)** 19 - UI library com hooks modernos
- **[TypeScript](https://www.typescriptlang.org/)** 5.0 - Type safety e IntelliSense
- **[axe-core](https://github.com/dequelabs/axe-core)** - Engine de teste da Deque Systems

### Arquitetura
- **Chrome Extension Manifest V3** - Service workers e APIs modernas
- **@a11y/core** - Pacote modular extraído para reutilização
- **CSS Variables** - Design system com suporte a temas
- **Vitest** - Testes unitários (91.93% coverage)

### Build & Deploy
- **GitHub Pages** - Hospedagem da documentação
- **ESLint** - Linting e qualidade de código
- **Scripts automatizados** - Versionamento e deploy

## 📦 Instalação

### 🚀 Instalação via Chrome Web Store (Em breve)

A extensão estará disponível na Chrome Web Store em breve. Por enquanto, use a instalação manual.

### 💻 Instalação Manual (Desenvolvedor)

#### Pré-requisitos
- Node.js 18+ e npm
- Google Chrome ou navegador baseado em Chromium

#### Passos

1. **Clone o repositório:**
```bash
git clone https://github.com/deividmarques/a11y-avaliator-web.git
cd a11y-avaliator-web
```

2. **Instale as dependências:**
```bash
npm install
```

3. **Faça o build da extensão:**
```bash
npm run build
```

4. **Carregue no Chrome:**
   - Abra o Chrome e navegue até `chrome://extensions/`
   - Ative o **"Modo do desenvolvedor"** no canto superior direito
   - Clique em **"Carregar sem compactação"**
   - Selecione a pasta `dist` gerada pelo build
   - A extensão aparecerá na barra de ferramentas!

## 🎮 Como Usar

### Análise Básica

1. **Navegue** até qualquer página web que deseja analisar
2. **Clique** no ícone "A11y Avaliator" na barra de extensões
3. **Configure** os testes:
   - Selecione o nível WCAG (A, AA ou AAA)
   - ✅ **Incluir teste de teclado** - Navegação e foco
   - ✅ **Incluir teste de leitor de tela** - Escolha o modo
   - ✅ **Incluir teste de contraste** - Estados interativos
4. **Clique** em "Analisar Página Atual"
5. **Visualize** o relatório completo

### Entendendo o Relatório

#### 📊 Score de Acessibilidade
- **90-100** 🟢 - Excelente acessibilidade
- **70-89** 🟡 - Bom, com algumas melhorias necessárias
- **50-69** 🟠 - Problemas moderados que precisam atenção
- **0-49** 🔴 - Problemas sérios que impedem acessibilidade

#### 🔍 Violações do axe-core
Cada violação mostra:
- **Impacto**: Crítico, Sério, Moderado ou Menor
- **Descrição**: Explicação do problema
- **Elementos afetados**: Lista de seletores CSS
- **Links**: Documentação WCAG e ARIA

#### ⌨️ Teste de Teclado
- Elementos sem indicador de foco visível
- Tabindex positivo (antipadrão)
- Possíveis keyboard traps

#### 🗣️ Teste de Leitor de Tela
Dependendo do modo escolhido:
- Elementos sem nome acessível
- Uso incorreto de aria-hidden
- Referências ARIA quebradas
- Problemas com landmarks
- Imagens sem texto alternativo

#### 🎨 Teste de Contraste
- Contraste de texto vs fundo
- Contraste em ícones e bordas
- Estados hover/focus/active/disabled

### Exportação de Relatórios

- **📥 JSON**: Dados estruturados para análise programática
- **📝 PDF**: Relatório visual formatado e pronto para compartilhar

## 🧪 Desenvolvimento

### Scripts Disponíveis

```bash
# Desenvolvimento com hot reload
npm run dev

# Build para produção
npm run build

# Testes com Vitest
npm test                # Modo watch
npm run test:run        # Execução única
npm run test:coverage   # Com coverage report

# Linting
npm run lint            # Verificar código
npm run lint:fix        # Corrigir automaticamente

# Documentação
npm run build:docs      # Build da documentação
npm run serve:docs      # Preview local em http://localhost:3000
npm run deploy:docs     # Deploy para GitHub Pages
```

### Estrutura de Pastas

```
a11y-avaliator-web/
├── 📁 public/                  # Assets estáticos
│   ├── manifest.json           # Manifesto Chrome MV3
│   └── icon-*.png              # Ícones da extensão
│
├── 📁 src/                     # Código fonte
│   ├── 📁 components/          # Componentes React
│   │   ├── ConfigForm.tsx      # Formulário de configuração
│   │   └── ResultsDisplay.tsx  # Exibição de resultados
│   ├── 📁 utils/               # Utilitários
│   ├── 📁 styles/              # Estilos globais
│   ├── analyzer.ts             # Lógica de análise
│   ├── background.ts           # Service worker
│   ├── content.ts              # Content script
│   ├── types.ts                # TypeScript types
│   └── main.tsx                # Entry point
│
├── 📁 docs-src/                # Fonte da documentação
│   ├── index.html              # Página principal
│   ├── *.html                  # 16 páginas de docs
│   ├── styles.css              # Design system
│   ├── sitemap.xml             # SEO
│   └── robots.txt              # Crawlers
│
├── 📁 docs/                    # Build da documentação (GitHub Pages)
├── 📁 scripts/                 # Scripts de build e deploy
│   ├── build-docs.js           # Build da documentação
│   ├── deploy-docs.sh          # Deploy para gh-pages
│   ├── add-meta-tags.js        # SEO automation
│   └── update-version.js       # Versionamento
│
├── 📄 vite.config.ts           # Configuração Vite
├── 📄 vitest.config.ts         # Configuração testes
├── 📄 tsconfig.json            # TypeScript config
└── 📄 package.json             # Dependencies
```

## 🏗️ Arquitetura

### @a11y/core Package

O núcleo da lógica de análise foi extraído para um pacote modular:

```typescript
import { 
  calculateAccessibilityScore,
  createAxeAnalyzer 
} from '@a11y/core';

const analyzer = createAxeAnalyzer();
const tags = analyzer.getWcagTags('AA');
const result = await analyzer.analyze(document);
const score = calculateAccessibilityScore(result);
```

**Casos de uso do @a11y/core:**
- ✅ Extensão Chrome (atual)
- 🤖 Integração com LLMs para sugestões com IA
- 💻 Plugin VS Code para análise em desenvolvimento
- ⚙️ CLI tools para CI/CD pipelines

### Manifest V3

A extensão usa Chrome Manifest V3 com:
- **Service Workers** em vez de background pages persistentes
- **activeTab permission** apenas quando necessário
- **Scripting API** para injeção dinâmica de scripts
- **Storage API** para persistência de configurações

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


## 🚀 Roadmap & Melhorias Futuras

### ✅ Concluído (v0.1.x)
- [x] Análise WCAG 2.2 completa (A, AA, AAA) com axe-core
- [x] Interface responsiva React 19 + TypeScript + Vite
- [x] Relatórios detalhados com classificação de impacto
- [x] **Testes de navegação por teclado** (foco, tabindex, keyboard traps)
- [x] **Testes de leitor de tela** com 4 modos especializados
- [x] **Teste de contraste interativo** para estados hover/focus/active/disabled
- [x] **Score integrado** de acessibilidade (0-100)
- [x] **Exportação profissional** em JSON e PDF
- [x] **Sistema de design** com variáveis CSS para temas
- [x] **Documentação completa** com 17 páginas (GitHub Pages)
- [x] **SEO otimizado** com meta tags para Google e crawlers de IA
- [x] **@a11y/core package** modular e reutilizável
- [x] Cobertura de testes 91.93% com Vitest
- [x] Versionamento automático de builds

### 🎯 Próximas Funcionalidades (v0.2.x)
- [ ] **Histórico de análises** com armazenamento local e comparações
- [ ] **Análise em lote** de múltiplas páginas do mesmo site
- [ ] **Sugestões com IA** integração com LLMs para correções automáticas
- [ ] **Snippets de código** para correções rápidas
- [ ] **Modo CI/CD** para integração em pipelines automatizados
- [ ] **Extensão Firefox** compatível com WebExtensions API

### 🔮 Futuro (v1.0+)
- [ ] **Dashboard web** para gerenciamento de projetos
- [ ] **API pública** para integrações personalizadas
- [ ] **Plugin VS Code** para análise durante desenvolvimento
- [ ] **Testes de performance** e Core Web Vitals
- [ ] **Comparação antes/depois** com visualização de melhorias
- [ ] **Relatórios agendados** para monitoramento contínuo

## 🧪 Testes

### Executar Testes

```bash
# Modo watch (desenvolvimento)
npm test

# Execução única
npm run test:run

# Com coverage report
npm run test:coverage

# UI interativa
npm run test:ui
```

### Cobertura Atual
- **Total**: 91.93%
- **Statements**: 91.93% (182/198)
- **Branches**: 97.22% (70/72)
- **Functions**: 83.33% (35/42)
- **Lines**: 91.93% (182/198)

## 🤝 Contribuindo

Contribuições são muito bem-vindas! Para contribuir:

1. **Fork** o projeto
2. **Crie** uma branch para sua feature: `git checkout -b feature/nova-funcionalidade`
3. **Commit** suas mudanças: `git commit -m 'Adiciona nova funcionalidade'`
4. **Push** para a branch: `git push origin feature/nova-funcionalidade`
5. **Abra** um Pull Request

### Diretrizes

- Mantenha o código TypeScript com tipagem forte
- Adicione testes para novas funcionalidades
- Atualize a documentação quando necessário
- Siga os padrões de código do ESLint
- Escreva commits descritivos

## 📄 Licença

Este projeto está licenciado sob a **Licença MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👥 Autor

**Deivid Marques**
- GitHub: [@deividmarques](https://github.com/deividmarques)
- Repositório: [a11y-avaliator-web](https://github.com/deividmarques/a11y-avaliator-web)

## 📞 Suporte

- 🐛 **Bugs**: Abra uma [issue](https://github.com/deividmarques/a11y-avaliator-web/issues)
- 💡 **Sugestões**: Use as [discussions](https://github.com/deividmarques/a11y-avaliator-web/discussions)
- 📖 **Documentação**: [https://deividmarques.github.io/a11y-avaliator-web-docs/](https://deividmarques.github.io/a11y-avaliator-web-docs/)
- ❓ **FAQ**: [Perguntas Frequentes](https://deividmarques.github.io/a11y-avaliator-web-docs/faq.html)

## 🌟 Agradecimentos

- [axe-core](https://github.com/dequelabs/axe-core) pela engine de testes
- [Deque Systems](https://www.deque.com/) pelos padrões de acessibilidade
- [W3C](https://www.w3.org/WAI/) pelas diretrizes WCAG
- Comunidade open source pela inspiração

---

<div align="center">

**Feito com ❤️ para um web mais acessível**

[⬆ Voltar ao topo](#a11y-avaliator-web)

</div>