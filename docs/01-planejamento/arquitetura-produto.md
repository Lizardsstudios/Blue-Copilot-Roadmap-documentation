# Arquitetura de Produto - Blue-Copilot

## Visão Geral

O Blue-Copilot é estruturado em camadas que permitem escalabilidade de receita e flexibilidade para o cliente:

```
┌─────────────────────────────────────────────────────────────┐
│                         MÓDULOS                             │
│              (Add-ons independentes opcionais)              │
├─────────────────────────────────────────────────────────────┤
│                          TIERS                              │
│        (ME/EPP → Média/Grande → Prestadora)                 │
├─────────────────────────────────────────────────────────────┤
│                          CORE                               │
│            (Sempre incluído em todos os planos)             │
└─────────────────────────────────────────────────────────────┘
```

---

## 1. Core (Base do Produto)

O Core está incluído em **todos os tiers**. É o produto principal.

### 1.1 Funcionalidades do Core

| Funcionalidade | Descrição |
|----------------|-----------|
| **Captação automática** | Editais chegam filtrados por segmento do cliente |
| **Agente de leitura** | IA lê edital (PDF) e extrai dados estruturados |
| **Preenchimento FEVG** | Sistema preenche automaticamente, usuário revisa e aprova |
| **Fluxo completo** | Pré-licitação → Licitação → Pós-licitação → Arquivo |
| **Gestão de contratos** | Controle de contratos diretos (manual) |
| **Gestão de ARP** | Controle de atas, empenhos, adesões/caronas (manual) |
| **Kanban** | Visualização por colunas de status |
| **Alertas de prazo** | Notificações automáticas de vencimentos |
| **Dashboard** | Visão geral das licitações em andamento |

### 1.2 Por que o Core inclui automação

Sem captação automática e preenchimento por IA, o sistema seria apenas "mais trabalho" para o operador. A automação **é** o produto — é o que justifica a adoção.

| Sem Blue-Copilot | Com Blue-Copilot |
|------------------|------------------|
| Busca editais em múltiplos portais | Editais chegam filtrados |
| Lê cada PDF manualmente | IA lê e extrai dados |
| Digita tudo no sistema | Revisa e aprova |
| 2-3 horas por edital | 10-15 minutos por edital |

---

## 2. Módulos (Add-ons)

Módulos são funcionalidades adicionais que o cliente contrata separadamente. **Qualquer tier pode contratar qualquer módulo.**

### 2.1 Módulos Disponíveis

```
┌──────────────────────┐  ┌──────────────────────┐
│   AGENTE JURÍDICO    │  │   ROBÔ DE LANCES     │
├──────────────────────┤  ├──────────────────────┤
│ • Impugnações        │  │ • Lances automáticos │
│ • Recursos admin.    │  │ • Multi-pregão       │
│ • Contrarrazões      │  │ • Estratégias:       │
│ • Esclarecimentos    │  │   - Agressivo        │
│ • Jurisprudência TCU │  │   - Moderado         │
│                      │  │   - Defensivo        │
├──────────────────────┤  ├──────────────────────┤
│     R$ 247/mês       │  │     R$ 397/mês       │
└──────────────────────┘  └──────────────────────┘
```

### 2.2 Roadmap de Módulos

| Fase | Módulo | Prioridade | Justificativa |
|------|--------|------------|---------------|
| 1 | Core (captação + leitura + fluxo) | MVP | Razão de existir do produto |
| 2 | Agente Jurídico | Alta | Diferencial competitivo único |
| 3 | Robô de Lances | Média | Paridade com mercado (commodity) |
| Futuro | Outros agentes | Baixa | Conforme demanda |

### 2.3 Características dos Módulos

- **Independentes**: Cada módulo funciona sozinho
- **Combináveis**: Cliente pode ter vários módulos ativos
- **Self-service**: Contratação e cancelamento pelo painel
- **Billing separado**: Cada módulo é um item na fatura

---

## 3. Tiers (Planos)

### 3.1 Estrutura dos Tiers

| Recurso | ME/EPP | Média/Grande | Prestadora |
|---------|--------|--------------|------------|
| **Core completo** | ✅ | ✅ | ✅ |
| **CNPJs inclusos** | 1 (fixo) | 1 (inicial) | 5 (inicial) |
| **Comprar + CNPJs** | ❌ Migrar tier | ✅ Self-service | ✅ Self-service |
| **Assentos inclusos** | 1 (fixo) | 3 (inicial) | 6 próprios + 2/CNPJ |
| **Comprar + assentos** | ❌ Migrar tier | ✅ Self-service | ✅ Self-service |
| **Contratar módulos** | ✅ | ✅ | ✅ |

### 3.2 Detalhamento por Tier

#### ME/EPP (Microempresa / Empresa de Pequeno Porte)

```
ME/EPP
├── 1 CNPJ (fixo, não pode adicionar)
├── 1 Assento (fixo, não pode adicionar)
├── Core completo ✅
└── Módulos: pode contratar qualquer um

Caso de uso: Dono opera sozinho
Preço base: R$ 247/mês
```

**Regras de upgrade:**
- Precisa de mais assentos? → Sistema oferece upgrade para Média/Grande
- Precisa de mais CNPJs? → Sistema oferece upgrade para Média/Grande

#### Média/Grande Empresa

```
Média/Grande
├── 1 CNPJ inicial
│   └── [+ Adicionar CNPJ] → R$ 197/mês (para filiais)
├── 3 Assentos iniciais
│   └── [+ Adicionar assento] → R$ 97/mês
├── Core completo ✅
└── Módulos: pode contratar qualquer um

Caso de uso: Empresa com equipe e/ou filiais
Preço base: R$ 597/mês
```

**CNPJs adicionais:** Para filiais da própria empresa que faturam separadamente.

#### Prestadora de Serviços

```
Prestadora
├── 5 CNPJs iniciais (clientes)
│   └── [+ Adicionar CNPJ cliente] → R$ 197/mês
├── 6 Assentos próprios (sua equipe)
│   └── [+ Adicionar assento próprio] → R$ 97/mês
├── 2 Assentos por CNPJ cliente (inclusos)
├── Core completo ✅
└── Módulos: pode contratar qualquer um

Caso de uso: Opera licitações para terceiros
Preço base: R$ 1.197/mês
```

**Diferenças da Prestadora:**
- CNPJs são de clientes (terceiros), não filiais
- Cada CNPJ cliente tem 2 assentos dedicados inclusos
- Pode segregar visão por cliente
- Assentos próprios são para a equipe interna da prestadora

### 3.3 Comparativo: Média/Grande vs Prestadora

| Aspecto | Média/Grande | Prestadora |
|---------|--------------|------------|
| CNPJs são | Dela mesma (filiais) | De terceiros (clientes) |
| Assentos por CNPJ | Compartilhados | 2 dedicados por CNPJ |
| Segregação de dados | Não | Sim (por cliente) |
| Preço base | R$ 597/mês | R$ 1.197/mês |

---

## 4. Precificação Consolidada

### 4.1 Preços Base (Tiers)

| Tier | Mensal | Anual (15% desc.) |
|------|--------|-------------------|
| ME/EPP | R$ 247 | R$ 2.519 |
| Média/Grande | R$ 597 | R$ 6.089 |
| Prestadora | R$ 1.197 | R$ 12.209 |

### 4.2 Preços Adicionais

| Item | Preço | Disponível para |
|------|-------|-----------------|
| Assento adicional | R$ 97/mês | Média/Grande, Prestadora |
| CNPJ adicional | R$ 197/mês | Média/Grande, Prestadora |

### 4.3 Preços Módulos

| Módulo | Preço |
|--------|-------|
| Agente Jurídico | R$ 247/mês |
| Robô de Lances | R$ 397/mês |

### 4.4 Exemplos de Fatura

**Exemplo 1: ME/EPP com módulo jurídico**
```
Plano ME/EPP ..................... R$ 247
Agente Jurídico .................. R$ 247
────────────────────────────────────────
TOTAL ............................ R$ 494/mês
```

**Exemplo 2: Média/Grande com 2 filiais e equipe de 5**
```
Plano Média/Grande ............... R$ 597
CNPJs adicionais (2) ............. R$ 394
Assentos adicionais (2) .......... R$ 194
Agente Jurídico .................. R$ 247
Robô de Lances ................... R$ 397
────────────────────────────────────────
TOTAL ............................ R$ 1.829/mês
```

**Exemplo 3: Prestadora com 8 clientes**
```
Plano Prestadora ................. R$ 1.197
CNPJs adicionais (3) ............. R$ 591
Assentos próprios adic. (2) ...... R$ 194
Agente Jurídico .................. R$ 247
Robô de Lances ................... R$ 397
────────────────────────────────────────
TOTAL ............................ R$ 2.626/mês
```

---

## 5. Self-Service (100% Automatizado)

### 5.1 Princípio

**Zero intervenção manual.** O cliente compra, faz upgrade, adiciona recursos e cancela tudo pelo painel, sem precisar falar com ninguém.

### 5.2 Ações Self-Service

| Ação | Fluxo |
|------|-------|
| Contratar módulo | Clica → Stripe Checkout → Webhook → Sistema ativa |
| Cancelar módulo | Clica → Confirma → Desativa no próximo ciclo |
| Adicionar assento | Clica → Verifica tier → Checkout → Provisiona |
| Adicionar CNPJ | Clica → Verifica tier → Checkout → Provisiona |
| Upgrade de tier | Clica → Checkout (diferença pro-rata) → Migra |
| Downgrade de tier | Clica → Verifica se cabe → Agenda para próximo ciclo |

### 5.3 Fluxo de Compra

```
Cliente clica em ação (ex: "+ Adicionar assento")
                    │
                    ▼
        ┌───────────────────────┐
        │ Sistema verifica:     │
        │ - Tier permite?       │
        │ - Tem limite?         │
        └───────────────────────┘
                    │
          ┌────────┴────────┐
          │                 │
          ▼                 ▼
      Permitido         Bloqueado
          │                 │
          │                 ▼
          │         ┌─────────────────┐
          │         │ Modal:          │
          │         │ "Faça upgrade   │
          │         │ para Tier X"    │
          │         │ [Ver planos]    │
          │         └─────────────────┘
          │
          ▼
┌─────────────────────┐
│ Stripe Checkout     │
│ (add subscription   │
│  item)              │
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│ Webhook recebido    │
│ (payment_success)   │
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│ Sistema provisiona  │
│ automaticamente     │
└─────────────────────┘
          │
          ▼
   Cliente usa imediatamente
```

### 5.4 Painel do Cliente

```
┌─────────────────────────────────────────────────────────────────┐
│                    PAINEL DO CLIENTE                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  MEU PLANO: Média/Grande                    [Fazer upgrade ↑]  │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │ CNPJs                                                   │   │
│  │                                                         │   │
│  │ • Empresa Principal Ltda (matriz)                       │   │
│  │ • Filial São Paulo                                      │   │
│  │ • Filial Rio de Janeiro                                 │   │
│  │                                                         │   │
│  │ Usando: 3 CNPJs              [+ Adicionar CNPJ filial]  │   │
│  │ Custo por CNPJ adicional: R$ 197/mês                    │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │ ASSENTOS                                                │   │
│  │                                                         │   │
│  │ • joao@empresa.com (Admin)                              │   │
│  │ • maria@empresa.com (Operador)                          │   │
│  │ • pedro@empresa.com (Operador)                          │   │
│  │ • ana@empresa.com (Viewer)                              │   │
│  │                                                         │   │
│  │ Usando: 4 de 3 inclusos (1 adicional)    [+ Adicionar]  │   │
│  │ Custo por assento adicional: R$ 97/mês                  │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │ MÓDULOS                                                 │   │
│  │                                                         │   │
│  │ ☑ Agente Jurídico     R$ 247/mês         [Gerenciar]   │   │
│  │ ☐ Robô de Lances      R$ 397/mês         [Contratar]   │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │ FATURA ATUAL                                            │   │
│  │                                                         │   │
│  │ Plano Média/Grande .................. R$ 597            │   │
│  │ CNPJs adicionais (2) ................ R$ 394            │   │
│  │ Assentos adicionais (1) ............. R$ 97             │   │
│  │ Agente Jurídico ..................... R$ 247            │   │
│  │ ─────────────────────────────────────────────           │   │
│  │ TOTAL ............................... R$ 1.335/mês      │   │
│  │                                                         │   │
│  │ Próxima cobrança: 15/01/2025        [Ver histórico]     │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 6. Arquitetura Técnica (Multi-Tenant)

### 6.1 Modelo de Dados

```
Organization (tenant)
├── id
├── name
├── tier: 'me' | 'media' | 'prestadora'
├── billing
│   ├── stripe_customer_id
│   ├── stripe_subscription_id
│   └── subscription_items: [...]
├── created_at
└── updated_at

CNPJ
├── id
├── organization_id (FK)
├── cnpj (número)
├── razao_social
├── tipo: 'proprio' | 'filial' | 'cliente'
├── is_included (veio com o plano?)
└── created_at

User
├── id
├── organization_id (FK)
├── email
├── name
├── role: 'owner' | 'admin' | 'operator' | 'viewer'
├── cnpj_access: [...] (quais CNPJs pode acessar)
├── is_included (veio com o plano?)
└── created_at

Module
├── id
├── organization_id (FK)
├── type: 'juridico' | 'robo_lances' | ...
├── status: 'active' | 'cancelled'
├── stripe_subscription_item_id
└── created_at
```

### 6.2 Permissões por Role

| Role | Criar licitação | Editar | Deletar | Ver relatórios | Gerenciar usuários | Billing |
|------|-----------------|--------|---------|----------------|-------------------|---------|
| Owner | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Admin | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| Operator | ✅ | ✅ | ❌ | ✅ | ❌ | ❌ |
| Viewer | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ |

### 6.3 Segregação de Dados (Prestadora)

Na Prestadora, usuários podem ter acesso restrito a CNPJs específicos:

```
Prestadora: BlueBox
├── CNPJ: BlueBox (próprio)
│   └── Usuários com acesso: Todos da equipe
├── CNPJ: Cliente ABC
│   └── Usuários com acesso: João, Maria
├── CNPJ: Cliente XYZ
│   └── Usuários com acesso: João, Pedro
```

---

## 7. Integrações de Billing

### 7.1 Stripe Subscription Items

Cada componente da fatura é um `subscription_item` separado:

```javascript
{
  subscription: "sub_xxx",
  items: [
    { price: "price_tier_media", quantity: 1 },      // Plano base
    { price: "price_cnpj_extra", quantity: 2 },      // CNPJs adicionais
    { price: "price_seat_extra", quantity: 1 },      // Assentos adicionais
    { price: "price_mod_juridico", quantity: 1 },    // Módulo jurídico
  ]
}
```

### 7.2 Webhooks Necessários

| Evento | Ação |
|--------|------|
| `invoice.paid` | Mantém acesso, atualiza próximo vencimento |
| `invoice.payment_failed` | Notifica cliente, período de graça |
| `customer.subscription.updated` | Atualiza recursos provisionados |
| `customer.subscription.deleted` | Revoga acesso |

---

## 8. Resumo

| Camada | O que é | Quem pode |
|--------|---------|-----------|
| **Core** | Captação + Leitura + Fluxo completo | Todos (incluído) |
| **Módulos** | Agente Jurídico, Robô de Lances | Todos (opcional) |
| **Assentos** | Usuários adicionais | Média/Grande, Prestadora |
| **CNPJs** | Filiais ou clientes | Média/Grande, Prestadora |
| **Self-service** | Comprar tudo pelo painel | Todos |

---

*Documento gerado em Dezembro/2024 para o Blue-Copilot.*
