# Guia Solo Developer: SaaS 3D de Alta Conversão com Claude Code

## Contexto e Objetivos

Este caderno temático foca na intersecção entre o **desenvolvimento ágil de SaaS por fundadores solo** e a criação de **interfaces imersivas em 3D** que elevam o valor percebido do produto para patamares de "luxo". O principal objetivo é capacitar o desenvolvedor a construir sistemas de alta conversão utilizando a filosofia **Product-Led Growth (PLG)**, onde o produto guia a aquisição e retenção. Simultaneamente, o estudo foca na **eficiência operacional**, ensinando como utilizar o **Claude Code** para codificar essas soluções complexas de forma autônoma, minimizando o desperdício de tokens e mantendo o custo de desenvolvimento baixo.

## Curadoria de Fontes

Para este estudo, foram selecionadas as seguintes fontes fundamentais:

1.  **"Como Economizar Milhões de Tokens no Claude Code" (Alan Nicolas)**: Guia essencial sobre higiene de contexto e arquitetura recursiva de pastas.
2.  **"Build $10,000 Luxury 3D Website... using Claude Code" (Dhiraj S)**: Metodologia da "fórmula de história em 3 atos" para animações de scroll.
3.  **"PLG Strategy: How to Build a Product-Led Growth Engine in 2026" (Wizard Creative Labs)**: Estrutura completa de GTM (Go-To-Market) baseada no produto.
4.  **"Antigravity + Spline: como criar sites 3D INCRÍVEIS" (Matheus Battisti)**: Tutorial técnico sobre integração de assets 3D gratuitos em aplicações React.
5.  **"Melhores práticas para Claude Code" (Anthropic)**: Documentação oficial sobre gerenciamento de sessões, `CLAUDE.md` e verificação de trabalho.

## Engenharia de Prompts e "Cicatrizes"

### Estratégias e Variações de Prompts
A engenharia de prompts evoluiu do simples comando de texto para a **configuração de instruções persistentes**. O uso do arquivo `CLAUDE.md` (gerado via `/init`) é a dica de ouro: ele serve como o "manual de instruções" que o Claude lê em cada mensagem para não esquecer o estilo de código e as regras do projeto.

Testamos a **"Fórmula de 3 Atos"** para prompts de 3D:
*   **Ato 1 (Produto Perfeito):** O produto flutua com iluminação dramática (0-28% de scroll).
*   **Ato 2 (Explosão/Dinâmica):** O produto se desconstroi ou derrete (30-68% de scroll).
*   **Ato 3 (Reconstrução):** O produto volta ao normal (72-100% de scroll).

### "Cicatrizes" e Troubleshooting (Dificuldades Encontradas)
*   **Poluição de Contexto:** Descobriu-se que o Claude Code carrega informações de forma **recursiva**. Se houver arquivos pesados na pasta "mãe", eles consomem tokens em todos os subprojetos. **Solução:** Usar `/clear` agressivamente entre tarefas e manter uma estrutura de pastas limpa.
*   **Erros de Importação em 3D:** Ao usar bibliotecas como Three.js com WebGPU, o Claude frequentemente tenta usar APIs legadas. **Solução:** Instalar **Skills** específicas de Three.js ou fornecer documentação atualizada via prompt ou arquivo Markdown.
*   **Overthinking:** O modo `Extended Thinking` pode gastar até **5x mais tokens** em tarefas simples. **Solução:** Desabilitar por padrão e usar apenas para decisões de arquitetura complexa.

## Miniguia de Estudo (Entrega Final)

### Resumos Estruturados
1.  **Fundamentos do SaaS PLG (2026):** O foco mudou de "aquisição a qualquer custo" para **eficiência**. O produto deve entregar o "momento Aha" em menos de 5-10 minutos. O onboarding deve ser interativo e baseado em ações reais, não apenas tours estáticos.
2.  **Economia de Tokens no Claude Code:** O maior "vilão" é a releitura do histórico. Comandos como `/btw` permitem tirar dúvidas sem poluir o histórico da sessão e sem gastar tokens de ferramentas. Converta PDFs longos para Markdown, que é até 10x mais leve para a IA processar.
3.  **Sites 3D de Conversão:** A animação não é apenas estética; ela mantém o usuário no site por mais tempo, aumentando a conexão com a marca. Use ferramentas como **Spline** para assets gratuitos e **React Three Fiber** para uma sintaxe declarativa e otimizada.

### Glossário de Conceitos Chave
*   **AEO (Answer Engine Optimization):** Otimizar conteúdo para ser a resposta direta em IAs como ChatGPT e Perplexity, focando em clareza sobre volume.
*   **TTV (Time-to-Value):** O tempo que um usuário leva para perceber o valor real. Em SaaS low-ticket, o alvo é abaixo de 15 minutos.
*   **MCP (Model Context Protocol):** Linguagem universal que permite ao Claude conectar-se a ferramentas externas como GitHub, Figma ou bancos de dados.
*   **PQL (Product Qualified Lead):** Um usuário que já demonstrou valor no produto e está pronto para converter ou expandir.
*   **Zeigarnik Effect:** A tendência humana de querer completar tarefas inacabadas, usada em onboarding através de barras de progresso.

### Conjunto de Prompts Reutilizáveis
*   **Para Higiene de Contexto:** `/compact Focus on the core business logic and current tasks, summarizing past architectural decisions.`
*   **Para Criação de Hero 3D:** `Utilize a fórmula de 3 atos: Ato 1 produto estático com spotlight; Ato 2 desconstrução estilo sanduíche no scroll 30-60%; Ato 3 reconstrução. Sem textos na imagem, 8K fotorealista.`
*   **Para Otimização de Conversão:** `Analise este arquivo guia_design.md e melhore esta landing page usando a skill de frontend-design. Simplifique a copy para o nível de leitura de 6ª série para aumentar a conversão.`
