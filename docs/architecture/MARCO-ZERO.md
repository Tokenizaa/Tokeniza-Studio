# Tokenizaa Studio — Marco Zero

**Versão:** 0.1 | **Status:** Proposta arquitetural para validação

## Visão
Ambiente interno para criar, configurar, administrar e evoluir aplicações da Tokenizaa. Combina infraestrutura compartilhada, componentes reutilizáveis, construtores visuais, módulos de negócio e integrações. Não substitui WordPress, frameworks ou desenvolvimento tradicional: reduz repetição preservando a independência dos produtos.

## Princípios
- Reutilizar capacidades comprovadas antes de reconstruir.
- Preservar domínio, dados e implantação independentes por produto.
- Compartilhar contratos e bibliotecas versionadas.
- Exigir fronteiras claras, testes e documentação para extrações.
- Aplicar autorização no servidor e isolamento de dados.
- Não executar código arbitrário armazenado em JSON ou no banco.
- Não criar abstrações cujo custo supere o benefício.
- Permitir código específico quando soluções declarativas forem inadequadas.

## Modelo conceitual
- **Core:** identidade, organizações, aplicações, autorização, contratos de API, eventos, configurações, auditoria, registro de extensões, jobs e storage básico.
- **Plugins:** capacidades opcionais por aplicação, como SEO, analytics, mídia, formulários, backup e notificações.
- **Providers:** adaptadores para pagamento, e-mail, IA, storage e APIs externas.
- **Modules:** capacidades de domínio reutilizáveis, como CRM, agenda, catálogo, pedidos e documentos.
- **Components/Widgets:** elementos visuais com propriedades, estados, contratos e documentação.
- **Themes/Templates:** identidade visual e estruturas iniciais de páginas, telas e aplicações.
- **Workflows:** automações com eventos, condições e ações registradas, validadas e autorizadas.

## Construtores
- **Page Builder:** páginas, layouts, widgets, templates, responsividade e conteúdo dinâmico.
- **Application Builder:** dashboards, CRUDs, tabelas, formulários, filtros, gráficos e áreas autenticadas.
- **Data Builder:** entidades, campos, relacionamentos, validações e coleções.
- **Workflow Builder:** gatilhos, eventos, condições, ações, integrações e histórico.

## Experiência visual
Biblioteca de elementos à esquerda, canvas central, propriedades à direita e barra superior para salvar, preview, responsividade e publicação. Cada elemento separa Visual (aparência), Dados (origem e vínculos) e Comportamento (ações, eventos e APIs).

## Extensibilidade e segurança
Cada extensão declara identificador, versão, tipo, compatibilidade, dependências, permissões, configurações e recursos. Conteúdo declarativo passa por schemas validados. Extensões com código devem ser registradas, revisadas, compiladas e implantadas de forma controlada.

## Direção tecnológica em avaliação
TypeScript, React, Tailwind, Cloudflare Workers, PostgreSQL/Supabase, R2 ou Supabase Storage, Cloudflare Queues, REST tipada, pnpm/Turborepo, Vitest e Playwright são possibilidades iniciais, não decisões aprovadas. A escolha depende do inventário dos repositórios e de ADRs. Não exigir migração imediata dos produtos.

## Extração dos produtos
- **Beleza Digital:** investigar componentes, design system, templates, renderer, mídia, SEO, contratos de pagamento, autenticação e onboarding. Regras específicas de salões permanecem no produto.
- **MapScrape v2:** investigar contratos de API, autenticação de consumidores, jobs, filas, estados, logs, auditoria, CSV e OpenAPI. Scraping permanece fora do Core.
- **DefesaAI:** investigar storage documental, histórico, PDF, notificações, validação de pagamentos, processamento e auditoria. Conteúdo jurídico permanece no produto.

Nenhuma extração ocorre por semelhança superficial. Cada proposta mapeia responsabilidade, dependências, dados, contrato, segurança, testes, consumidores e atualização.

## Priorização
- **P0 — Fundação:** identidade, organizações, aplicações, permissões, registro de extensões, contratos, eventos, configurações, auditoria, segurança, jobs essenciais, storage básico e biblioteca inicial.
- **P1 — Produtividade:** Media Library, Data Builder, Form Builder, Page Builder, Application Builder, themes, templates, providers de pagamento, notificações, documentos e importação/exportação.
- **P2 — Evolução:** Workflow Builder, SEO, analytics, cache, backup/restauração, IA avançada e monitoramento.

## Fases
0. Validar arquitetura, inventariar produtos, mapear dependências e registrar ADRs.
1. Construir Core mínimo.
2. Consolidar biblioteca compartilhada.
3. Implementar construtores iniciais.
4. Adicionar extensões, providers e workflows.
5. Migrar capacidades comprovadas progressivamente.

## Critérios de aceitação
- Aplicações utilizam o Core sem depender umas das outras.
- Extensões respeitam contratos e permissões.
- Dados permanecem isolados.
- Componentes compartilhados têm testes e documentação.
- APIs possuem contratos e versionamento.
- Jobs têm rastreabilidade e tratamento de falhas.
- Deploys são independentes.
- Atualizações do Core não quebram consumidores silenciosamente.
- Reutilização reduz duplicação de fato.

## Fora do escopo inicial
Marketplace público, compatibilidade WordPress, migração obrigatória dos produtos, construtor universal, execução arbitrária em runtime e implementação antecipada de todos os módulos.

## Decisões pendentes
1. Studio central com aplicações independentes ou pacotes incorporados por aplicação?
2. Bancos independentes ou infraestrutura compartilhada com isolamento rigoroso?
3. Identidade central ou autenticação independente por aplicação?
4. Application Builder ou Page Builder como primeiro construtor?
5. Pacotes versionados ou dependência direta de repositório central?

Recomendação inicial: preservar independência dos produtos, compartilhar contratos e bibliotecas versionadas e evitar dependência obrigatória de backend central em runtime.

## Conclusão do Marco Zero
Inventário técnico atualizado, matriz de capacidades, fronteiras de módulos, ADRs, plano priorizado e critérios de aceitação aprovados.