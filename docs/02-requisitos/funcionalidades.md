# Funcionalidades - Blue-Copilot

## Visão Geral

Este documento lista todas as funcionalidades do Blue-Copilot organizadas por área e fase de desenvolvimento.

**Legenda de Prioridade:**
- **P0** = MVP (Fase 1) - Obrigatório para lançamento
- **P1** = Fase 2 - Agente Jurídico
- **P2** = Fase 3 - Robô de Lances

**Legenda de Complexidade:**
- **B** = Baixa (1-2 dias)
- **M** = Média (3-5 dias)
- **A** = Alta (7-10 dias)
- **MA** = Muito Alta (10+ dias)

---

## 1. CORE (MVP - Fase 1)

### 1.1 Captação de Editais

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| CAP-001 | Integração API PNCP | Conexão com Portal Nacional de Contratações Públicas | P0 | A |
| CAP-002 | Integração Compras.gov | Conexão com portal federal | P0 | A |
| CAP-003 | Filtros por segmento | Configurar palavras-chave e categorias do cliente | P0 | M |
| CAP-004 | Filtros por região | UF, município, abrangência | P0 | B |
| CAP-005 | Filtros por modalidade | Pregão, dispensa, concorrência, etc. | P0 | B |
| CAP-006 | Filtros por valor | Faixa de valores estimados | P0 | B |
| CAP-007 | Fila de editais | Editais captados aguardando validação | P0 | M |
| CAP-008 | Download automático | Baixar PDF do edital e anexos | P0 | M |
| CAP-009 | Validação rápida | Tela para aprovar/rejeitar edital captado | P0 | M |
| CAP-010 | Motivo de rejeição | Registrar por que edital foi descartado | P0 | B |
| CAP-011 | Agendamento de captação | Frequência de busca (diária, horária) | P0 | B |
| CAP-012 | Notificação de novos editais | Alerta quando chegam editais novos | P0 | B |

### 1.2 Agente de Leitura (IA)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| LER-001 | Upload de PDF | Receber edital em PDF | P0 | B |
| LER-002 | OCR quando necessário | Extrair texto de PDFs escaneados | P0 | M |
| LER-003 | Extração de dados básicos | Órgão, modalidade, número, data abertura | P0 | A |
| LER-004 | Extração de objeto | Descrição do objeto licitado | P0 | M |
| LER-005 | Extração de itens | Lista de itens com quantidades | P0 | A |
| LER-006 | Extração de prazos | Entrega, vigência, validade proposta | P0 | M |
| LER-007 | Extração de exigências | Documentação, atestados, certificações | P0 | A |
| LER-008 | Extração de valores | Valor estimado, valor máximo | P0 | M |
| LER-009 | Identificação de restrições | Cláusulas potencialmente restritivas | P0 | A |
| LER-010 | Preenchimento automático FEVG | Preencher formulário com dados extraídos | P0 | A |
| LER-011 | Confiança da extração | Indicar campos com baixa certeza | P0 | M |
| LER-012 | Revisão humana | Interface para confirmar/corrigir dados | P0 | M |

### 1.3 FEVG (Ficha Eletrônica de Vendas ao Governo)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| FEV-001 | Formulário completo | Todos os campos da FEVG | P0 | M |
| FEV-002 | Dados do órgão | Nome, CNPJ, contato, endereço | P0 | B |
| FEV-003 | Dados do edital | Número, modalidade, identificador portal | P0 | B |
| FEV-004 | Registro de preços | Flag se é ARP | P0 | B |
| FEV-005 | Itens da licitação | Tabela de itens com produto vinculado | P0 | M |
| FEV-006 | Valores por item | Referência, mínimo, negociado | P0 | B |
| FEV-007 | Prazos | Entrega, vigência ARP, validade proposta | P0 | B |
| FEV-008 | Tributação | Impostos aplicáveis | P0 | B |
| FEV-009 | Aprovação comercial | Workflow de aprovação | P0 | M |
| FEV-010 | Aprovação técnica | Workflow de aprovação | P0 | M |
| FEV-011 | Aprovação financeira | Workflow de aprovação + análise de viabilidade | P0 | M |
| FEV-012 | Observações | Campo livre para anotações | P0 | B |
| FEV-013 | Vinculação de CNPJ | Qual CNPJ vai participar | P0 | B |
| FEV-014 | Efeito jurídico pendente | Flag para movimentação jurídica em andamento | P0 | B |
| FEV-015 | Edital suspenso | Flag quando edital está suspenso | P0 | B |
| FEV-016 | Resumo da licitação | Resultado: participantes, valores, vencedor | P0 | M |
| FEV-017 | Razão de arquivo | Motivo predefinido + texto livre | P0 | B |

### 1.4 Kanban e Visualização

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| KAN-001 | Colunas por status | Visualização em colunas | P0 | M |
| KAN-002 | Colunas pré-licitação | Qualificação, FEVG, Impugnação, Suspensa, Proposta | P0 | B |
| KAN-003 | Colunas licitação | Pregão, Ganhamos, Perdemos, ARP | P0 | B |
| KAN-004 | Colunas pós-licitação | Contrato, Execução, Concluído | P0 | B |
| KAN-005 | Coluna arquivo | Licitações arquivadas | P0 | B |
| KAN-006 | Drag and drop | Mover cards entre colunas | P0 | M |
| KAN-007 | Contadores | Quantidade de cards por coluna | P0 | B |
| KAN-008 | Filtros rápidos | Por CNPJ, responsável, prazo | P0 | M |
| KAN-009 | Busca | Pesquisar por texto | P0 | B |
| KAN-010 | Ordenação | Por data, valor, prazo | P0 | B |
| KAN-011 | Cores por urgência | Destaque visual para prazos próximos | P0 | B |
| KAN-012 | Visão por lista | Alternativa ao kanban | P0 | M |

### 1.5 Fluxo Pré-Licitação

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| PRE-001 | Qualificação inicial | Decidir se participa ou arquiva | P0 | B |
| PRE-002 | Análise de conformidade | Verificar se produto atende 100% | P0 | M |
| PRE-003 | Planilha comparativa | Comparar edital x produto x concorrentes | P0 | A |
| PRE-004 | Decisão de impugnação | Registrar decisão de impugnar | P0 | B |
| PRE-005 | Decisão de esclarecimento | Registrar decisão de pedir esclarecimento | P0 | B |
| PRE-006 | Acompanhar resposta | Monitorar resposta do órgão | P0 | M |
| PRE-007 | Elaboração de proposta | Checklist de preparação | P0 | M |
| PRE-008 | Declarações | Gerar declarações obrigatórias | P0 | M |
| PRE-009 | Suspensão de edital | Registrar quando edital é suspenso | P0 | B |
| PRE-010 | Nova data | Atualizar quando edital é reagendado | P0 | B |

### 1.6 Fluxo Licitação (Durante o Pregão)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| LIC-001 | Registrar participação | Marcar que está participando | P0 | B |
| LIC-002 | Registrar resultado | Venceu, perdeu, desclassificado | P0 | B |
| LIC-003 | Valor final | Registrar valor do lance vencedor | P0 | B |
| LIC-004 | Upload da ata | Anexar ata do pregão | P0 | B |
| LIC-005 | Intenção de recurso | Registrar se houve recurso | P0 | B |
| LIC-006 | Acompanhar recurso | Monitorar andamento | P0 | M |
| LIC-007 | Resultado tipo | Contrato direto ou ARP | P0 | B |

### 1.7 Fluxo Pós-Licitação

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| POS-001 | Receber contrato/ARP | Registrar recebimento | P0 | B |
| POS-002 | Assinar e devolver | Checklist de assinatura | P0 | B |
| POS-003 | Cadastrar contrato | Dados do contrato no sistema | P0 | M |
| POS-004 | Cadastrar ARP | Dados da ata no sistema | P0 | M |
| POS-005 | Vigência | Controlar prazo de vigência | P0 | B |
| POS-006 | Saldo | Controlar saldo disponível | P0 | M |
| POS-007 | Receber empenho | Registrar nota de empenho | P0 | M |
| POS-008 | Vincular empenho | Ligar empenho ao contrato/ARP | P0 | B |
| POS-009 | Faturamento | Registrar nota fiscal emitida | P0 | M |
| POS-010 | Despacho | Registrar envio/entrega | P0 | B |
| POS-011 | Aceite | Registrar aceite do órgão | P0 | B |
| POS-012 | Pagamento | Registrar recebimento | P0 | B |
| POS-013 | Aditivos | Registrar aditivos contratuais | P0 | M |

### 1.8 Gestão de ARP (Ata de Registro de Preços)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| ARP-001 | Órgão gerenciador | Identificar quem administra a ata | P0 | B |
| ARP-002 | Órgãos participantes | Listar participantes originais | P0 | M |
| ARP-003 | Saldo por órgão | Controlar quantidade por participante | P0 | M |
| ARP-004 | Pedido de adesão | Registrar solicitação de carona | P0 | M |
| ARP-005 | Autorizar adesão | Workflow de autorização | P0 | M |
| ARP-006 | Limites de adesão | Controlar 50% por carona, 2x total | P0 | M |
| ARP-007 | Hierarquia de adesão | Validar regras (município→estado→federal) | P0 | M |
| ARP-008 | Empenhos por órgão | Controlar empenhos de cada aderente | P0 | M |

### 1.9 Gestão de Documentos

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| DOC-001 | Upload de documentos | Anexar arquivos à licitação | P0 | B |
| DOC-002 | Pastas por fase | Organização automática por fase | P0 | M |
| DOC-003 | Tipos de documento | Categorização (edital, proposta, contrato...) | P0 | B |
| DOC-004 | Visualização inline | Ver PDF sem baixar | P0 | M |
| DOC-005 | Download individual | Baixar documento específico | P0 | B |
| DOC-006 | Download em lote | Baixar todos de uma fase/licitação | P0 | M |
| DOC-007 | Versionamento | Manter versões anteriores | P0 | M |
| DOC-008 | Busca em documentos | Pesquisar texto dentro dos PDFs | P0 | A |
| DOC-009 | Metadados | Data upload, usuário, tamanho | P0 | B |
| DOC-010 | Limite de armazenamento | Controle por tier/plano | P0 | B |

### 1.10 Timeline de Auditoria

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| AUD-001 | Log de criação | Registrar quem criou, quando | P0 | B |
| AUD-002 | Log de edição | Registrar alterações de campos | P0 | M |
| AUD-003 | Log de movimentação | Registrar mudanças de status | P0 | B |
| AUD-004 | Log de documentos | Registrar uploads/exclusões | P0 | B |
| AUD-005 | Log de comentários | Registrar mensagens do chat | P0 | B |
| AUD-006 | Dados anterior/novo | Guardar valor antes e depois | P0 | M |
| AUD-007 | Visualização timeline | Interface cronológica | P0 | M |
| AUD-008 | Filtro por tipo | Filtrar por tipo de ação | P0 | B |
| AUD-009 | Filtro por usuário | Filtrar por quem fez | P0 | B |
| AUD-010 | Exportar log | Gerar relatório de auditoria | P0 | M |

### 1.11 Chat Interno

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| CHT-001 | Chat por licitação | Conversa vinculada ao processo | P0 | M |
| CHT-002 | Mensagens de texto | Enviar/receber mensagens | P0 | B |
| CHT-003 | Menções | Marcar usuários com @ | P0 | M |
| CHT-004 | Notificação de menção | Alertar usuário mencionado | P0 | B |
| CHT-005 | Histórico completo | Manter todas as mensagens | P0 | B |
| CHT-006 | Anexar no chat | Enviar arquivo na conversa | P0 | M |
| CHT-007 | Indicador de não lido | Mostrar mensagens novas | P0 | B |
| CHT-008 | Busca no chat | Pesquisar mensagens | P0 | M |

### 1.12 Alertas e Notificações

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| ALE-001 | Alerta de prazo | Notificar vencimento próximo | P0 | M |
| ALE-002 | Configurar antecedência | Quantos dias antes alertar | P0 | B |
| ALE-003 | Alerta de novo edital | Notificar editais captados | P0 | B |
| ALE-004 | Alerta de menção | Notificar quando mencionado | P0 | B |
| ALE-005 | Central de notificações | Tela com todas as notificações | P0 | M |
| ALE-006 | Marcar como lido | Dispensar notificação | P0 | B |
| ALE-007 | E-mail de alertas | Enviar por e-mail (configurável) | P0 | M |
| ALE-008 | Resumo diário | E-mail com pendências do dia | P0 | M |

### 1.13 Dashboard

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| DAS-001 | Visão geral | Números principais | P0 | M |
| DAS-002 | Licitações por status | Gráfico de distribuição | P0 | M |
| DAS-003 | Próximos vencimentos | Lista de prazos urgentes | P0 | M |
| DAS-004 | Taxa de sucesso | % de licitações ganhas | P0 | M |
| DAS-005 | Valor em disputa | Soma de valores em andamento | P0 | B |
| DAS-006 | Valor ganho | Soma de contratos/ARPs | P0 | B |
| DAS-007 | Filtro por período | Selecionar range de datas | P0 | B |
| DAS-008 | Filtro por CNPJ | Ver dados de CNPJ específico | P0 | B |

### 1.14 Multi-CNPJ

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| CNP-001 | Cadastrar CNPJ | Adicionar empresa/filial/cliente | P0 | B |
| CNP-002 | Dados do CNPJ | Razão social, endereço, contato | P0 | B |
| CNP-003 | Tipo de CNPJ | Próprio, filial, cliente | P0 | B |
| CNP-004 | Documentos do CNPJ | Certidões, contratos sociais | P0 | M |
| CNP-005 | Validade de documentos | Alertar vencimento de certidões | P0 | M |
| CNP-006 | Vincular licitação | Associar licitação a CNPJ | P0 | B |
| CNP-007 | Filtrar por CNPJ | Ver apenas licitações de um CNPJ | P0 | B |
| CNP-008 | Segregação de dados | Usuário vê apenas CNPJs autorizados | P0 | M |

### 1.15 Gestão de Usuários e Assentos

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| USR-001 | Convidar usuário | Enviar convite por e-mail | P0 | M |
| USR-002 | Roles | Owner, Admin, Operator, Viewer | P0 | M |
| USR-003 | Permissões por role | Controle de acesso | P0 | M |
| USR-004 | Acesso a CNPJs | Definir quais CNPJs usuário vê | P0 | M |
| USR-005 | Desativar usuário | Remover acesso sem deletar | P0 | B |
| USR-006 | Limite de assentos | Controlar por plano | P0 | M |
| USR-007 | Transferir ownership | Passar propriedade da conta | P0 | M |

---

## 2. MÓDULO: Agente Jurídico (Fase 2)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| JUR-001 | Gerar impugnação | IA redige com base no edital | P1 | A |
| JUR-002 | Base de jurisprudência | TCU, tribunais estaduais | P1 | A |
| JUR-003 | Citar precedentes | Incluir decisões relevantes | P1 | A |
| JUR-004 | Templates de impugnação | Modelos por tipo de problema | P1 | M |
| JUR-005 | Gerar esclarecimento | IA redige pedido | P1 | M |
| JUR-006 | Gerar recurso | IA redige recurso administrativo | P1 | A |
| JUR-007 | Gerar contrarrazões | IA redige resposta a recurso | P1 | A |
| JUR-008 | Histórico de peças | Banco de peças já criadas | P1 | M |
| JUR-009 | Análise de risco | IA avalia chance de sucesso | P1 | A |
| JUR-010 | Revisão humana | Interface para ajustar texto | P1 | M |
| JUR-011 | Formatação DOCX | Exportar documento formatado | P1 | M |

---

## 3. MÓDULO: Robô de Lances (Fase 3)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| ROB-001 | Conectar portal | Login automatizado (Comprasnet, BB, etc.) | P2 | MA |
| ROB-002 | Monitorar pregão | Acompanhar fase de lances | P2 | A |
| ROB-003 | Estratégia agressiva | Sempre cobrir menor lance | P2 | A |
| ROB-004 | Estratégia moderada | Cobrir com margem de segurança | P2 | A |
| ROB-005 | Estratégia defensiva | Só cobrir se viável | P2 | A |
| ROB-006 | Valor limite | Definir lance mínimo | P2 | M |
| ROB-007 | Multi-pregão | Participar de vários simultâneos | P2 | MA |
| ROB-008 | Monitorar chat | Alertar convocação do pregoeiro | P2 | A |
| ROB-009 | Log de lances | Registrar todos os lances dados | P2 | M |
| ROB-010 | Pausa manual | Permitir intervenção humana | P2 | M |
| ROB-011 | Relatório pós-pregão | Resumo da participação | P2 | M |

---

## 4. BILLING E SELF-SERVICE (Fase 1)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| BIL-001 | Integração Stripe | Processamento de pagamentos | P0 | A |
| BIL-002 | Planos/Tiers | ME, Média/Grande, Prestadora | P0 | M |
| BIL-003 | Subscription items | Itens dinâmicos na assinatura | P0 | A |
| BIL-004 | Comprar assento | Self-service | P0 | M |
| BIL-005 | Comprar CNPJ | Self-service | P0 | M |
| BIL-006 | Contratar módulo | Self-service | P0 | M |
| BIL-007 | Cancelar módulo | Self-service | P0 | M |
| BIL-008 | Upgrade de tier | Self-service com pro-rata | P0 | A |
| BIL-009 | Downgrade de tier | Validar limites, agendar | P0 | A |
| BIL-010 | Painel de fatura | Ver cobrança atual | P0 | M |
| BIL-011 | Histórico de faturas | Faturas anteriores | P0 | M |
| BIL-012 | Atualizar cartão | Trocar forma de pagamento | P0 | M |
| BIL-013 | Cancelar assinatura | Self-service com confirmação | P0 | M |
| BIL-014 | Webhooks Stripe | Processar eventos de pagamento | P0 | A |
| BIL-015 | Período de graça | Manter acesso em falha de pagamento | P0 | M |
| BIL-016 | Bloqueio por inadimplência | Restringir acesso após período | P0 | M |

---

## 5. INFRAESTRUTURA E SEGURANÇA (Fase 1)

| ID | Funcionalidade | Descrição | Prioridade | Complexidade |
|----|----------------|-----------|------------|--------------|
| INF-001 | Autenticação | Login com e-mail/senha | P0 | M |
| INF-002 | OAuth Google | Login com Google | P0 | M |
| INF-003 | 2FA | Autenticação em dois fatores | P0 | M |
| INF-004 | Recuperação de senha | Fluxo de reset | P0 | B |
| INF-005 | Multi-tenant | Isolamento de dados por organização | P0 | A |
| INF-006 | Row Level Security | Segurança no Supabase | P0 | A |
| INF-007 | Backup automático | Backup diário dos dados | P0 | M |
| INF-008 | SSL/HTTPS | Conexão segura | P0 | B |
| INF-009 | Rate limiting | Proteção contra abuso | P0 | M |
| INF-010 | Logs de acesso | Registrar logins | P0 | B |

---

## 6. RESUMO POR FASE

### Fase 1 - MVP (Core + Billing)

| Área | Qtd Funcionalidades |
|------|---------------------|
| Captação | 12 |
| Agente de Leitura | 12 |
| FEVG | 17 |
| Kanban | 12 |
| Pré-Licitação | 10 |
| Licitação | 7 |
| Pós-Licitação | 13 |
| ARP | 8 |
| Documentos | 10 |
| Auditoria | 10 |
| Chat | 8 |
| Alertas | 8 |
| Dashboard | 8 |
| Multi-CNPJ | 8 |
| Usuários | 7 |
| Billing | 16 |
| Infraestrutura | 10 |
| **TOTAL MVP** | **166** |

### Fase 2 - Agente Jurídico

| Área | Qtd Funcionalidades |
|------|---------------------|
| Agente Jurídico | 11 |
| **TOTAL FASE 2** | **11** |

### Fase 3 - Robô de Lances

| Área | Qtd Funcionalidades |
|------|---------------------|
| Robô de Lances | 11 |
| **TOTAL FASE 3** | **11** |

---

## 7. ESTIMATIVA DE ESFORÇO

### MVP (Fase 1)

| Complexidade | Quantidade | Dias médios | Total dias |
|--------------|------------|-------------|------------|
| Baixa (B) | ~50 | 1,5 | 75 |
| Média (M) | ~80 | 4 | 320 |
| Alta (A) | ~30 | 8 | 240 |
| Muito Alta (MA) | ~6 | 12 | 72 |
| **TOTAL** | **166** | - | **~707 dias** |

**Considerando 1 desenvolvedor full-time:**
- Estimativa bruta: ~707 dias úteis
- Com paralelização e reuso: ~4-5 meses para MVP funcional
- Com escopo reduzido (vertical slice): ~3-4 meses

**Recomendação:** Começar com vertical slice (uma licitação do início ao fim) e expandir.

---

*Documento gerado em Dezembro/2024 para o Blue-Copilot.*
