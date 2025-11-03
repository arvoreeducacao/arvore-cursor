# 🌳 Árvore Cursor Configuration

Bem-vindo ao repositório de configuração do Cursor/AI usado pela equipe de engenharia da Árvore! Este repositório contém nossas user rules e configurações de MCPs (Model Context Protocol) que usamos para aumentar a produtividade e padronizar o desenvolvimento assistido por IA.

## 📋 Índice

- [Sobre](#sobre)
- [User Rules](#user-rules)
- [MCPs Configurados](#mcps-configurados)
- [Instalação e Configuração](#instalação-e-configuração)
- [Variáveis de Ambiente](#variáveis-de-ambiente)
- [Contribuindo](#contribuindo)

## 🎯 Sobre

Este repositório documenta as práticas e ferramentas que a Árvore utiliza para trabalhar com IA no desenvolvimento de software. Compartilhamos estas configurações com a comunidade para ajudar outros times a acelerar seu workflow de desenvolvimento.

## 📝 User Rules

Nossas user rules definem como a IA deve se comportar durante o desenvolvimento. Estas regras garantem qualidade, consistência e alinhamento com nossas práticas de engenharia.

### 🗄️ Integração com Banco de Dados

```
Use mysql mcp to see database schema and data to give to you more data and info to create code.
```

### 📦 Gerenciamento de Pacotes

**Package Manager:** Sempre prefira `pnpm` ao rodar ou sugerir comandos. Use npm ou yarn apenas se pnpm não for suportado.

**Instalação de Pacotes:**

1. Sempre verifique o npm MCP registry para número de downloads e sinais de segurança
2. Prefira bibliotecas oficiais ou com número relevante/alto de downloads
3. Evite pacotes obscuros ou com baixa adoção, a menos que explicitamente aprovados

### 🧪 Test-Driven Development (TDD)

Seguimos rigorosamente TDD:

1. Escreva testes significativos primeiro, baseados estritamente no PRD
2. Testes devem refletir lógica de negócio real e edge cases, não asserções triviais
3. Não implemente a feature ainda
4. Testes devem falhar pelos motivos corretos
5. Implemente apenas o necessário para os testes passarem

**Test Runner:** Sempre prefira Vitest. Use outro framework apenas se Vitest não for suportado.

**Idioma:** Sempre escreva testes unitários em inglês.

### 📋 PRD (Product Requirements Document)

Antes de codificar, gere um PRD conciso contendo:

- Problema a resolver
- Scope in / Scope out
- Mudanças na API ou modelo de dados
- Edge cases a considerar
- Plano de testes com critérios de pass/fail

### 🔍 Análise de Código Existente

Antes de implementar, leia os arquivos relevantes e retorne:

1. O que este código faz (overview)
2. Partes desconhecidas ou pouco claras
3. Riscos e dependências
4. Arquivos impactados se mudanças forem feitas
5. Esboço de uma estratégia de testes

### 💻 Estilo de Código

**Comentários:** Não adicione comentários no código a menos que explicitamente solicitado. Prefira código limpo e auto-explicativo sem explicações inline.

### 📚 Documentação

Use o MCP context7 para consultar documentação de bibliotecas e frameworks antes de implementar algo específico.

### 🔄 Workflow Linear

Ao resolver uma task do Linear:

1. Crie um branch com o nome apropriado para integração com Linear
2. Crie um PR com descrições corretas
3. Se tudo estiver OK no PR, mova o card para status de review
4. Envie mensagem para o canal Slack #eng-prs com o formato:
   ```
   👉 [PR](pr_link) para [task_name](task_link)
   ```

### 🚀 Deploy e Releases

Quando um PR for mergeado, envie mensagem para o canal #releases:

```
<(task_link)|(task_name)>
- Status: (indo para produção | em produção)
- Risks: <resumo em uma frase em português dos potenciais riscos de entregar este código>
```

### ✅ Quality Assurance

Quando código for criado ou modificado, execute a suite de testes, eslint, sonarqube e build:

```bash
pnpm test:cov
pnpm lint
pnpm build
```

Corrija quaisquer issues encontrados antes de finalizar.

## 🔌 MCPs Configurados

Nossa configuração utiliza diversos MCPs para integração com ferramentas essenciais:

### 📚 Context7

Acesso a documentação atualizada de bibliotecas e frameworks.

**Uso:** Consulta automática de documentação durante desenvolvimento.

### 🐛 Console Ninja

Logs e erros do runtime da aplicação.

**Uso:** Debug em tempo real de aplicações.

### 🔍 SonarQube

Análise de qualidade de código e segurança.

**Uso:** Verificação automática de code quality e vulnerabilidades.

### 🐙 GitHub

Integração completa com GitHub para gerenciamento de PRs, branches e workflows.

**Uso:** Automação de workflow git, criação de PRs, review de código.

### 💬 Slack

Integração com Slack para notificações e comunicação.

**Uso:** Envio automático de notificações para canais #eng-prs e #releases.

### 🎭 Playwright

Automação de browser para testes end-to-end.

**Uso:** Testes automatizados de interface.

### 🗄️ MySQL

Acesso ao schema e dados do banco de dados.

**Uso:** Consultas ao banco para gerar código mais preciso.

- **Package:** `@arvoretech/mysql-mcp@1.0.4`

### 📦 NPM Registry

Consulta ao registro NPM para verificar pacotes.

**Uso:** Validação de pacotes antes da instalação.

- **Package:** `@arvoretech/npm-registry-mcp@1.0.4`

### 🔐 AWS Secrets Manager

Gerenciamento seguro de secrets.

**Uso:** Acesso a credenciais e configurações sensíveis.

- **Package:** `@arvoretech/aws-secrets-manager-mcp@1.0.4`

### 📋 Linear

Integração com Linear para gerenciamento de tasks.

**Uso:** Automação de workflow de tasks, criação de branches, atualização de status.

### 📖 DeepWiki

Documentação aprofundada de projetos GitHub.

**Uso:** Consulta de documentação de projetos open source.

### 📊 Datadog

Monitoramento e observabilidade.

**Uso:** Consulta de métricas, logs e traces.

- **Package:** `@arvoretech/datadog-mcp@1.0.4`

### 🎨 Figma

Integração com Figma para design.

**Uso:** Acesso a designs e componentes visuais.

### 📝 Notion

Integração com Notion para documentação.

**Uso:** Acesso a documentação e conhecimento da equipe.

## 🚀 Instalação e Configuração

### Pré-requisitos

- [Cursor IDE](https://cursor.sh/)
- Node.js 18+
- pnpm
- Docker (para alguns MCPs)

### Passo a Passo

1. **Clone este repositório**

```bash
git clone https://github.com/arvore/arvore-cursor.git
cd arvore-cursor
```

2. **Configure as variáveis de ambiente**

Crie um arquivo `.env` baseado nas variáveis necessárias (veja seção [Variáveis de Ambiente](#variáveis-de-ambiente)).

3. **Configure o Cursor**

Copie o conteúdo de `mcp.json` para a configuração de MCPs do Cursor:

- Abra Cursor
- Vá em Settings → MCP
- Cole a configuração do `mcp.json`

4. **Configure as User Rules**

Copie o conteúdo de `rules.md` para as user rules do seu projeto:

- Abra Cursor
- Vá em Settings → Rules
- Cole ou referencie o arquivo `rules.md`

5. **Customize para seu contexto**

Edite as configurações necessárias:

- No `rules.md`, substitua `<linear_name>` pelo seu username do Linear
- No `rules.md`, substitua `<squad_name>` pelo nome do seu squad

## 🔐 Variáveis de Ambiente

Configure as seguintes variáveis de ambiente conforme os MCPs que você deseja usar:

```bash
# Context7
CONTEXT7_API_KEY=your_context7_api_key

# SonarQube
SONARQUBE_TOKEN=your_sonarqube_token
SONARQUBE_ORG=your_org_id

# GitHub
GITHUB_PERSONAL_ACCESS_TOKEN=your_github_token

# Slack
SLACK_MCP_XOXP_TOKEN=your_slack_token

# MySQL
MYSQL_HOST=localhost
MYSQL_PORT=3306
MYSQL_USER=root
MYSQL_PASSWORD=your_password
MYSQL_DATABASE=your_database

# AWS
AWS_PROFILE=your_aws_profile
AWS_REGION=us-east-1

# Datadog
DATADOG_API_KEY=your_datadog_api_key
DATADOG_APP_KEY=your_datadog_app_key
DATADOG_SITE=datadoghq.com
```

### Como obter os tokens

- **Context7:** [context7.com](https://context7.com)
- **SonarQube:** Configurações do seu servidor SonarQube
- **GitHub:** Settings → Developer Settings → Personal Access Tokens
- **Slack:** [Slack API](https://api.slack.com/apps)
- **Datadog:** Organization Settings → API Keys

## 🤝 Contribuindo

Contribuições são bem-vindas! Se você tem sugestões de melhorias nas user rules ou novas configurações de MCPs:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/amazing-rule`)
3. Commit suas mudanças (`git commit -m 'Add some amazing rule'`)
4. Push para a branch (`git push origin feature/amazing-rule`)
5. Abra um Pull Request

### Guidelines

- Mantenha as rules claras e concisas
- Documente o propósito de cada rule
- Teste suas configurações de MCP antes de submeter
- Siga o padrão de formatação existente

## 📄 Licença

Este projeto é licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.

## 🌟 Agradecimentos

Agradecemos a toda comunidade de desenvolvedores que contribui para o ecossistema de MCPs e ferramentas de IA para desenvolvimento.

---

**Desenvolvido com 🌳 pela equipe de engenharia da Árvore**
