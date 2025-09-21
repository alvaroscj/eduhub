# Arquitetura — EduHub (G4)

## Visão Geral
Arquitetura **híbrida**:
- **Núcleo monolítico modular** para processos acadêmicos críticos (matrículas, notas, histórico).
- **Microsserviços especializados** para componentes com escalabilidade independente (videochamadas, notificações, buscas, gamificação, IA, reservas).
- **API Gateway** centralizando autenticação, segurança e integração.

## Justificativas
- **Consistência e confiabilidade**: o núcleo modular mantém transações críticas sob controle.
- **Escalabilidade**: microsserviços isolam picos de carga sem afetar todo o sistema.
- **Segurança e conformidade**: política transversal no gateway (LGPD, criptografia, auditoria).
- **Evolução contínua**: modularidade facilita introdução de novas funções sem interrupção.

## Diretrizes de Implementação
- Versionamento semântico (SemVer) para serviços.
- Contratos de API versionados; documentação com OpenAPI.
- Observabilidade (logs estruturados, métricas e tracing).
- CI/CD com integração contínua e políticas de aprovação.
- Padrões de confiabilidade (timeouts, retries, circuit breaker).
