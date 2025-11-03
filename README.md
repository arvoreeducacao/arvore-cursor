# 🌳 Árvore Cursor Configuration

Configuração do Cursor/AI usada pela equipe de engenharia da Árvore. Este repositório contém nossas user rules e configurações de MCPs (Model Context Protocol) para aumentar produtividade e padronizar o desenvolvimento assistido por IA.

## 📦 O que tem aqui

- **`rules.md`** - User rules que definem como a IA deve se comportar durante o desenvolvimento
- **`mcp.json`** - Configuração dos MCPs integrados (GitHub, Slack, Linear, SonarQube, etc.)
- **`env.template`** - Template das variáveis de ambiente necessárias

## 🚀 Como usar

1. Clone este repositório
2. Copie `env.template` para `.env` e configure suas credenciais
3. No Cursor, vá em **Settings → MCP** e cole o conteúdo de `mcp.json`
4. No Cursor, vá em **Settings → Rules** e referencie ou cole o conteúdo de `rules.md`
5. Customize as variáveis `<linear_name>` e `<squad_name>` no `rules.md`

## 🔌 MCPs Incluídos

- **Context7** - Documentação de bibliotecas
- **SonarQube** - Análise de código
- **GitHub** - PRs e workflows
- **Slack** - Notificações
- **Linear** - Gestão de tasks
- **MySQL** - Acesso ao banco ([@arvoretech/mysql-mcp](https://www.npmjs.com/package/@arvoretech/mysql-mcp))
- **NPM Registry** - Validação de pacotes ([@arvoretech/npm-registry-mcp](https://www.npmjs.com/package/@arvoretech/npm-registry-mcp))
- **AWS Secrets** - Gerenciamento de secrets ([@arvoretech/aws-secrets-manager-mcp](https://www.npmjs.com/package/@arvoretech/aws-secrets-manager-mcp))
- **Datadog** - Observabilidade ([@arvoretech/datadog-mcp](https://www.npmjs.com/package/@arvoretech/datadog-mcp))
- **Playwright** - Testes E2E
- **Figma** - Design
- **Notion** - Documentação
- **DeepWiki** - Docs de projetos OSS
- **Console Ninja** - Debug

## 🤝 Contribuindo

Contribuições são bem-vindas! Abra um PR com suas sugestões de melhorias.

## 📄 Licença

MIT

---

**Desenvolvido com 🌳 pela equipe de engenharia da Árvore**
