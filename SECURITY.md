# Política de segurança

## Reportar vulnerabilidades
Não publique detalhes de vulnerabilidades não corrigidas em Issues ou Pull Requests públicos.

Utilize o recurso Private vulnerability reporting do GitHub, se habilitado para este repositório, ou contate os mantenedores por um canal privado oficial da organização.

Inclua passos para reprodução, impacto, versão/commit afetado e evidências mínimas. Não envie credenciais, dados pessoais ou dados reais de clientes.

## Escopo
Esta política cobre código, workflows, dependências, configurações, documentação operacional e infraestrutura mantida neste repositório.

## Práticas obrigatórias
- Nunca versionar tokens, chaves privadas, senhas ou arquivos de ambiente reais.
- Usar permissões mínimas em GitHub Actions.
- Fixar Actions de terceiros em SHA completo quando adotadas em workflows sensíveis.
- Revisar dependências e alertas de segurança.
- Validar autorização no servidor e isolamento entre aplicações/tenants.
- Registrar mudanças de segurança e evidências nos Pull Requests.
- Rotacionar imediatamente qualquer credencial exposta.

## Resposta a incidentes
Registrar o incidente, preservar evidências, avaliar impacto, revogar/rotacionar credenciais, corrigir a causa, validar a correção e documentar ações sem expor dados sensíveis.