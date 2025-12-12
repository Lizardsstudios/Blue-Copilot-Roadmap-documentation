# Processo de Licitações - Blue-Copilot

## Visão Geral

O ciclo de uma licitação é dividido em 3 fases principais + arquivo:

| Fase | Descrição |
|------|-----------|
| **Pré-Licitação** | Todos os atos necessários até a data do pregão |
| **Licitação** | O pregão em si, até o encerramento |
| **Pós-Licitação** | Todos os processos após o término do pregão |
| **Arquivo** | Processos encerrados (ganhos, perdidos, desistências) |

---

## Fluxo Visual Completo

```
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│                                    PRÉ-LICITAÇÃO                                        │
└─────────────────────────────────────────────────────────────────────────────────────────┘

    CAPTAÇÃO                 QUALIFICAÇÃO                      FEVG
   (externa)                   INICIAL                          │
       │                          │                              │
       ▼                          ▼                              ▼
  ┌─────────┐              ┌─────────────┐              ┌───────────────┐
  │ Emails  │              │   Cliente   │              │   Análise     │
  │ com     │─────────────▶│   decide    │─────────────▶│   Técnica +   │
  │ editais │              │  participar │              │   Financeira  │
  └─────────┘              └─────────────┘              └───────────────┘
       │                          │                              │
       │                          │ NÃO                          │
       │                          ▼                              ▼
       │                    ┌──────────┐                ┌───────────────────┐
       │                    │ ARQUIVO  │                │ Produto atende?   │
       │                    │(motivado)│                └───────────────────┘
       │                    └──────────┘                    │    │    │
       │                                                    │    │    │
       │                          ┌─────────────────────────┘    │    └──────────────────┐
       │                          │                              │                       │
       │                          ▼                              ▼                       ▼
       │                    ┌───────────┐              ┌──────────────┐          ┌──────────────┐
       │                    │ Caminho A │              │  Caminho B   │          │  Caminho C   │
       │                    │  Atende   │              │  Não atende  │          │  Ilegalidade │
       │                    │   100%    │              │  técnico     │          │  do edital   │
       │                    └───────────┘              └──────────────┘          └──────────────┘
       │                          │                         │                          │
       │                          │                         ▼                          ▼
       │                          │                   ┌─────────────────────────────────────┐
       │                          │                   │      IMPUGNAÇÃO / ESCLARECIMENTO    │
       │                          │                   └─────────────────────────────────────┘
       │                          │                              │
       │                          │         ┌────────────────────┼────────────────────┐
       │                          │         │                    │                    │
       │                          │         ▼                    ▼                    ▼
       │                          │   ┌──────────┐        ┌───────────┐        ┌───────────┐
       │                          │   │ Deferido │        │Indeferido │        │  Aguarda  │
       │                          │   └──────────┘        └───────────┘        │ resposta  │
       │                          │         │                    │             └───────────┘
       │                          │         │                    ▼
       │                          │         │             ┌──────────┐
       │                          │         │             │ ARQUIVO  │
       │                          │         │             │(motivado)│
       │                          │         │             └──────────┘
       │                          │         │
       │                          ▼         ▼
       │                    ┌─────────────────────┐
       │                    │ ELABORAÇÃO PROPOSTA │
       │                    │                     │
       │                    │ • Documentação      │
       │                    │ • Declarações       │
       │                    │ • Proposta inicial  │
       │                    └─────────────────────┘
       │                              │
       │                              ▼
       │                    ┌─────────────────────┐
       │                    │  SUSPENSA/ADIADA    │◀──── (monitoramento contínuo)
       │                    └─────────────────────┘
       │                              │
       ▼                              ▼
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│                                      LICITAÇÃO                                          │
└─────────────────────────────────────────────────────────────────────────────────────────┘

                         ┌─────────────────────────┐
                         │   PREGÃO/NEGOCIAÇÃO     │
                         └─────────────────────────┘
                                     │
            ┌────────────────────────┼────────────────────────┐
            │                        │                        │
            ▼                        ▼                        ▼
    ┌───────────────┐      ┌───────────────┐        ┌───────────────┐
    │ 1. Abertura   │      │ 2. Fase de    │        │ 3. Julgamento │
    │    propostas  │─────▶│    Lances     │───────▶│ Classificação │
    └───────────────┘      └───────────────┘        └───────────────┘
                                                            │
                                                            ▼
                                                   ┌───────────────┐
                                                   │ 4. Aceitação  │
                                                   │    proposta   │
                                                   └───────────────┘
                                                            │
                                      ┌─────────────────────┼─────────────────────┐
                                      │                     │                     │
                                      ▼                     ▼                     ▼
                               ┌────────────┐       ┌──────────────┐      ┌──────────────┐
                               │ Desclassif.│       │   Aceita     │      │  Negociação  │
                               │            │       │              │      │  de preço    │
                               └────────────┘       └──────────────┘      └──────────────┘
                                      │                     │                     │
                                      ▼                     └──────────┬──────────┘
                               ┌────────────┐                          │
                               │  PERDEMOS  │                          ▼
                               └────────────┘               ┌───────────────────┐
                                                            │ 5. Habilitação    │
                                                            │    do vencedor    │
                                                            └───────────────────┘
                                                                      │
                                                                      ▼
                                                            ┌───────────────────┐
                                                            │ 6. Fase Recursal  │
                                                            │                   │
                                                            │ • 5 min intenção  │
                                                            │ • 3 dias recurso  │
                                                            │ • 3 dias contrarr.│
                                                            └───────────────────┘
                                                                      │
                                                     ┌────────────────┼────────────────┐
                                                     │                │                │
                                                     ▼                ▼                ▼
                                              ┌───────────┐    ┌───────────┐    ┌───────────┐
                                              │ Sem       │    │ Recurso   │    │ Recurso   │
                                              │ recurso   │    │ procedente│    │improcedent│
                                              └───────────┘    └───────────┘    └───────────┘
                                                     │                │                │
                                                     │                ▼                │
                                                     │         ┌───────────┐           │
                                                     │         │ Chama 2º  │           │
                                                     │         │ colocado  │           │
                                                     │         └───────────┘           │
                                                     │                                 │
                                                     └────────────────┬────────────────┘
                                                                      │
                                                                      ▼
                                                            ┌───────────────────┐
                                                            │ 7. Adjudicação    │
                                                            │   (pregoeiro)     │
                                                            └───────────────────┘
                                                                      │
                                                                      ▼
                                                            ┌───────────────────┐
                                                            │ 8. Homologação    │
                                                            │ (superior hierárq)│
                                                            └───────────────────┘
                                                                      │
                              ┌────────────────────────────────────────┼─────────────────┐
                              │                                        │                 │
                              ▼                                        ▼                 ▼
                       ┌────────────┐                           ┌────────────┐    ┌────────────┐
                       │  GANHAMOS  │                           │    ARP     │    │  PERDEMOS  │
                       │ (contrato) │                           │   (ata)    │    │            │
                       └────────────┘                           └────────────┘    └────────────┘
                              │                                        │
                              ▼                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│                                    PÓS-LICITAÇÃO                                        │
└─────────────────────────────────────────────────────────────────────────────────────────┘

        CONTRATO DIRETO                                        ARP
              │                                                  │
              ▼                                                  ▼
    ┌───────────────────┐                           ┌───────────────────────┐
    │ Recebe/Assina     │                           │ Recebe/Assina ARP     │
    │ Contrato          │                           │                       │
    └───────────────────┘                           └───────────────────────┘
              │                                                  │
              ▼                                     ┌────────────┼────────────┐
    ┌───────────────────┐                           │            │            │
    │ Cadastra Contrato │                           ▼            ▼            ▼
    │ no Sistema        │                     ┌──────────┐ ┌──────────┐ ┌──────────┐
    └───────────────────┘                     │Gerenciad.│ │Participan│ │ Caronas  │
              │                               └──────────┘ └──────────┘ └──────────┘
              │                                     │            │            │
              │                                     │            │            ▼
              │                                     │            │     ┌─────────────┐
              │                                     │            │     │ Anuência?   │
              │                                     │            │     │ (consulta   │
              │                                     │            │     │  cliente)   │
              │                                     │            │     └─────────────┘
              │                                     │            │            │
              │                                     └────────────┴────────────┘
              │                                                  │
              ▼                                                  ▼
    ┌───────────────────┐                           ┌───────────────────────┐
    │ EMPENHO(S)        │                           │ EMPENHO(S)            │
    │ (órgão licitante) │                           │ (múltiplos órgãos)    │
    └───────────────────┘                           └───────────────────────┘
              │                                                  │
              └──────────────────────┬───────────────────────────┘
                                     │
                                     ▼
                        ┌───────────────────────────┐
                        │      PARA CADA EMPENHO    │
                        └───────────────────────────┘
                                     │
         ┌───────────────────────────┼───────────────────────────┐
         │                           │                           │
         ▼                           ▼                           ▼
   ┌───────────┐            ┌───────────────┐           ┌───────────────┐
   │ Protótipo │            │  Faturamento  │           │  Ocorrências  │
   │(se exigido)│            └───────────────┘           │               │
   └───────────┘                     │                   │ • Dilação     │
         │                           ▼                   │ • Reequilíbrio│
         │                  ┌───────────────┐           │ • Pendências  │
         ▼                  │   Despacho    │           └───────────────┘
   ┌───────────┐            └───────────────┘
   │ Avaliação │                     │
   │ do órgão  │                     ▼
   └───────────┘            ┌───────────────┐
         │                  │   Entrega     │
         │                  └───────────────┘
         │                           │
         │                           ▼
         │                  ┌───────────────┐
         └─────────────────▶│    Aceite     │
                            └───────────────┘
                                     │
                                     ▼
                            ┌───────────────┐
                            │  Pagamento    │
                            │ (após entrega │
                            │  ou aceite)   │
                            └───────────────┘
                                     │
                                     ▼
                            ┌───────────────┐
                            │   CONCLUÍDO   │
                            └───────────────┘
```

---

## Fase 1: Pré-Licitação

### 1.1 Captação de Editais

| Aspecto | Situação Atual |
|---------|----------------|
| Como | Serviço terceirizado envia emails com editais filtrados por segmento |
| Validação | Pessoa confere se edital realmente é do segmento do cliente |
| Destino | Se válido, cadastra no sistema na coluna "Qualificação Inicial" |

### 1.2 Qualificação Inicial

| Aspecto | Descrição |
|---------|-----------|
| O que é | Oportunidade aguardando decisão do cliente |
| Decisão | Cliente determina se segue em frente ou arquiva |
| Se SIM | Vira uma FEVG (Ficha Eletrônica de Vendas a Governo) |
| Se NÃO | Vai para Arquivo (motivado) |

### 1.3 FEVG - Caminhos Possíveis

#### Caminho A: Produtos atendem 100% das exigências

| Etapa | Responsável | Ação |
|-------|-------------|------|
| 1 | Comercial | Dá OK para seguir |
| 2 | Técnico | Analisa descritivo, confirma que produto atende |
| 3 | Financeiro | Analisa prazo, validade, ARP, custos, define menor preço possível |
| 4 | Operacional | Verifica/prepara documentação |
| 5 | Operacional | Preenche declarações exigidas |
| 6 | Operacional | Prepara proposta com valor inicial |
| 7 | - | Aguarda abertura do pregão |

#### Caminho B: Produtos NÃO atendem todas as especificações

| Etapa | Ação |
|-------|------|
| 1 | Analisar descritivo técnico do edital |
| 2 | Verificar se está direcionado para algum concorrente |
| 3 | Identificar quais exigências não atendemos |
| 4 | Criar planilha comparativa (edital x nosso produto x concorrentes) |
| 5 | Decidir: impugnar ou pedir esclarecimento |
| 6 | Mover FEVG para coluna "Impugnação/Esclarecimento" |

#### Caminho C: Exigências que afrontam as leis

| Aspecto | Descrição |
|---------|-----------|
| Natureza | Ilegalidade do edital, não técnico do produto |
| Exemplos | Prazo inexequível, exigências além do previsto em lei |
| Fluxo | Mesmo do Caminho B |

### 1.4 Resultados de Impugnação/Esclarecimento

| Situação | Resultado | O que acontece |
|----------|-----------|----------------|
| Impugnação deferida | Aceita | Nova licitação ou remarcam data |
| Impugnação indeferida | Negada | Decide se participa ou arquiva |
| Esclarecimento permissivo | Abre possibilidade | Volta pro fluxo normal |
| Esclarecimento indeferido | Negado | Decide se participa ou arquiva |

### 1.5 Colunas do Kanban - Pré-Licitação

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| Qualificação Inicial | Sequencial | Aguardando decisão do cliente |
| FEVG | Sequencial | Em análise/preparação |
| Impugnação/Esclarecimento | Monitoramento | Aguardando resposta do órgão |
| Suspensa/Adiada | Monitoramento | Acompanhar mudanças de data |
| Elaboração Proposta | Sequencial | Preparando documentação |
| Arquivo | Final | Processo encerrado (motivado) |

---

## Fase 2: Licitação

### 2.1 Etapas do Pregão

| Etapa | O que acontece |
|-------|----------------|
| 1. Abertura das propostas | Análise de conformidade. Pregoeiro pode desclassificar antes dos lances |
| 2. Fase de lances | Disputa de preços |
| 3. Julgamento/Classificação | Define a melhor oferta |
| 4. Aceitação da proposta | Pregoeiro pode: desclassificar, aceitar, ou negociar redução |
| 5. Habilitação do vencedor | Verificação de documentação |
| 6. Fase recursal | 5 min intenção → 3 dias recurso → 3 dias contrarrazões |
| 7. Adjudicação | Pregoeiro adjudica o vencedor |
| 8. Homologação | Superior hierárquico confirma |

### 2.2 Colunas do Kanban - Licitação

| Coluna | Descrição |
|--------|-----------|
| Pregão/Negociação | Card permanece aqui durante toda a disputa |
| Ganhamos | Vitória em licitação comum → segue para contrato |
| Perdemos | Não vencemos |
| ARP | Vitória em registro de preços → segue para ata |

---

## Fase 3: Pós-Licitação

### 3.1 Tipos de Resultado

#### Licitação Comum (Contrato Direto)

| Aspecto | Regra |
|---------|-------|
| Resultado | Contrato assinado |
| Quem empenha | Apenas o órgão licitante |
| Aditivos | 25% regra geral, 50% para reforma de engenharia |
| Supressão | Até 25% |

#### ARP (Ata de Registro de Preços)

| Aspecto | Descrição |
|---------|-----------|
| Resultado | Ata de Registro de Preços (não é contrato) |
| A ata não é contrato | Cria mera expectativa de direito |
| Obrigação nasce ato a ato | Cada vez que o órgão "puxa" a ata |

**Fontes de Empenho na ARP:**

| Persona | Descrição | Limites |
|---------|-----------|---------|
| Órgão Gerenciador | Administra a ARP, pode contratar direto | Saldo da ata |
| Órgãos Participantes | Entraram desde o início | Saldo próprio na ata |
| Órgãos Caronas | Aderem depois, precisam de anuência | 50% por carona, 2x total |

**Regra de Adesão (Carona) - Hierarquia:**

| Órgão | Pode aderir a atas de |
|-------|----------------------|
| Município | Município, Estado, União |
| Estado | Estado, União |
| União | Apenas União |

### 3.2 Fluxo Pós-Vitória

| Etapa | Descrição |
|-------|-----------|
| 1. Recebe Contrato/ARP | Órgão emite documento |
| 2. Assina | Empresa assina e devolve |
| 3. Cadastra no Sistema | Cria registro para controle |
| 4. Empenho(s) | Recebe ordem de fornecimento |
| 5. Faturamento | Emite nota fiscal |
| 6. Despacho | Envia produto |
| 7. Entrega | Recebimento físico |
| 8. Aceite | Confirmação do órgão |
| 9. Pagamento | Recebe (após entrega ou aceite, conforme edital) |

### 3.3 Ocorrências Durante Execução

| Ocorrência | Ação |
|------------|------|
| Protótipo exigido | Acompanhar, avisar órgão quando pronto |
| Atraso na entrega | Solicitar dilação de prazo |
| Pedido de carona | Consultar cliente (não é obrigatório aceitar) |
| Reequilíbrio | Solicitar revisão de preço |
| Pendência documental | Regularizar |
| Recusa do aceite | Resolver divergência |
| Atraso no pagamento | Cobrar órgão |

---

## Arquivamento

| Aspecto | Descrição |
|---------|-----------|
| Quando | Pode acontecer em qualquer momento |
| Requisito | Deve ser motivado |
| Motivação | Opções pré-definidas + campo "Outros" (texto livre) |
| Exemplos | Sem estoque, indeferimento, cliente desistiu, preço inviável |

---

## Campos da FEVG (Sistema Atual)

### Cabeçalho
- Assunto
- Cliente
- Vendedor
- Empresa
- Equipe de Vendas
- Aprovação Financeira
- Aprovação Técnica
- Cadastro de Proposta (data)
- Data da Licitação
- Edital Suspenso (checkbox)
- Efeito Jurídico (checkbox) - movimento jurídico pendente
- Participação
- Observação

### Aba Dados da Licitação
- Dados do órgão (Nome, Endereço, CNPJ, Cidade, Estado, CEP)
- Contato (Nome, Função, Telefone, E-mail)
- Edital (Nº, Modalidade, Registro de Preços, Validade, Identif., Local)
- Impostos (Isento IPI, Isento ICMS, NCM, Validado)
- Diversos (Validade Proposta, Prazo Pag., Amostra, Aceite)
- Referências (Origem)
- Dotação Orçamentária

### Aba Itens da Licitação
Itens do edital que o cliente pode participar + produto correspondente:
- Item, Objeto, Descrição, Produto, Quantidade, Status
- Valor Referência, Valor Mínimo, Valor Negociado, Prazo entrega

### Aba Resumo da Licitação
Resultado do pregão (baseado na ata):
- Item, Qtde, Empresa, Produto, Preço Inicial, Preço Final, Status

### Aba Razão de Arquivo
- Motivo do arquivamento

---

## Oportunidades de Automação Identificadas

| Processo | Situação Atual | Automação Possível |
|----------|----------------|-------------------|
| Captação de editais | Serviço terceirizado + validação manual | Agente de captação (PNCP, Compras.gov) |
| Análise de edital | Leitura manual | Agente de leitura + auto-preenchimento |
| Planilha comparativa | Criação manual | Agente compara descritivo x produto |
| Impugnação/Esclarecimento | Redação manual | Agente jurídico com jurisprudência |
| Participação no pregão | Manual ou robô terceirizado | Agente lançador |
| Análise de concorrentes | Manual | Agente de conferência documental |
| Contrarrazões | Redação manual | Agente jurídico |
| Acompanhamento de prazos | Manual | Alertas automáticos |
| Monitoramento de status | Manual | Agente de acompanhamento |
