When I ask to generate a "PR-DESC", do this:

1. Analyze the current branch and identify what changes were made
2. Generate a PR description using the provided template below
3. Fill in the template with specific information about the changes in this branch
4. If information is not available or not applicable, use "N/A"
5. Return the complete description in markdown format for me to copy and paste

Template to use (keep in Portuguese):

<!--- **Por favor, escreva sua descrição e responda a todas as seções abaixo em português.** -->

<!--- Forneça um resumo geral das suas mudanças no título acima -->

<!--- Todos os seguintes tópicos DEVEM ser preenchidos (escreva N/A se não for apropriado) -->

## Descrição

<!--- Descreva suas mudanças em detalhes -->

## Etiquetas (Labels)

<!--- Por favor, lembre-se de adicionar labels apropriadas de acordo com o tipo de PR selecionado acima. Isso garantirá que nosso changelog seja detalhado e completo. -->

<!--- Adicione aqui e principalmente na barra lateral a direita >>> -->

<!--- Utilizamos:

  - feat/feature: novas funcionalidades;
  - fix/bug/hotfix: correções gerais e de bugs;
  - dependencies/deps/chore: estrutura,  dependencias, etc;
  - test: testes, aumento de coverage, etc
  - other: melhorias de performance, releases, refatoração, etc

>>> -->

- [ ] 🍕 Nova Funcionalidade
- [ ] 🐛 Correção de Bug
- [ ] 🤖 Estrutura
- [ ] ✅ Testes
- [ ] 💬 Outros

## História Relacionada

<!--- Este projeto aceita apenas pull requests relacionados a histórias abertas -->
<!--- Se estiver sugerindo uma nova funcionalidade ou mudança, discuta primeiro em uma história -->
<!--- Se estiver corrigindo um bug, deve haver uma história descrevendo-o com passos para reproduzir -->
<!--- Por favor, vincule a história aqui: -->

<!--- Exemplo: [JOR-178](link da história no Jira aqui) -->

## Motivação e Contexto

<!--- Por que essa mudança é necessária? Qual problema ela resolve? -->

## Como Isso Foi Testado?

<!--- Descreva detalhadamente como você testou suas mudanças. -->
<!--- Inclua detalhes sobre seu ambiente de teste e os testes que você executou para -->
<!--- ver como sua mudança afeta outras áreas do código, etc. -->

- [ ] Testes Unitários
- [ ] Testes de Integração
- [ ] Testes e2e (playwright)
- [ ] Testes de Aceitação (QA)
- [ ] Testes de Performance
- [ ] Outros (quais?)
- [ ] Nenhum (por quê? 🤔)

## Análise de Risco e Impacto

<!--- Qual é o risco e o impacto deste PR? -->
<!--- Se alto, este PR deve ter um deployment assistido para Prod. -->
<!--- Além disso: se alto, este PR deveria ter sido deployado primeiro para staging 🙂 -->

- [ ] Baixo
- [ ] Alto

<!--- Nota: Um PR é considerado arriscado quando ele altera o núcleo de -->
<!--- alguma funcionalidade, se o deploy depende da infraestrutura em nuvem anterior ou -->
<!--- se você não tem certeza sobre o impacto que pode causar aos nossos usuários. -->
<!--- Também vamos usar isso para PRs que exigem migração de banco de dados. -->

## Capturas de Tela ou Auxílios Visuais (se apropriado)

<!--- Capturas de tela antes/depois, mockups, links para o Figma, etc. -->

Additional guidelines:
- Always follow the template exactly - do not modify, remove, or delete any existing content. Only add the required information and select relevant checkboxes. Follow the template strictly.
- Analyze git diff to understand what files were changed
- Check commit messages for context about the changes
- Look for Linear task references in commit messages or branch names
- If multiple types of changes were made, mark multiple checkboxes as appropriate
- Be specific about what was tested and how
- Assess risk level based on the scope and type of changes
- If no Linear task is referenced, leave the "História Relacionada" section as N/A
- Always provide a clear, concise description of what was changed

