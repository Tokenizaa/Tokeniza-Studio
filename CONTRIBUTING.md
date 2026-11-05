# Contribuição

## Fluxo de trabalho
1. Abra uma Issue para registrar contexto, objetivo e critérios de aceitação quando a mudança não for trivial.
2. Crie uma branch curta a partir de main: feat/, fix/, docs/, refactor/, test/ ou chore/.
3. Faça mudanças focadas e mantenha commits claros.
4. Abra um Pull Request para main.
5. Descreva problema, solução, riscos, testes e evidências.
6. Aguarde checks e revisão antes do merge.

Não desenvolver diretamente em main, exceto manutenção administrativa inicial ou resposta documentada a incidente.

## Pull Requests
- Relacione Issues com Closes #N quando aplicável.
- Explique impacto em arquitetura, dados, segurança e compatibilidade.
- Inclua testes automatizados ou justifique sua ausência.
- Atualize documentação e ADRs quando decisões ou contratos mudarem.
- Não inclua segredos, tokens, dados pessoais ou dumps de produção.
- Não marque checks como aprovados sem execução real.

## Commits
Preferir mensagens claras e consistentes:
- feat: add extension registry contract
- fix: enforce tenant boundary
- docs: record deployment decision
- test: cover permission boundary

## Revisão
Revisores avaliam correção, segurança, escopo, compatibilidade, testes e manutenção. Mudanças de arquitetura ou segurança precisam de justificativa explícita e evidências.

## Auditoria
Decisões relevantes devem ser registradas em ADR. Alterações sensíveis devem deixar rastros verificáveis no PR, nos checks e no histórico de commits.