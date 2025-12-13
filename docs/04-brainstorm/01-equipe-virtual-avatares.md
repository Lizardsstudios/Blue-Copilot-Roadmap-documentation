# Visão de Produto: Equipe Virtual Helion

> **Classificação:** Confidencial - Visão Estratégica  
> **Versão:** 1.0  
> **Data:** Dezembro 2025  
> **Status:** Conceito / Roadmap Futuro

---

## 📋 Sumário Executivo

### O Conceito

Transformar a interação com IA no Helion de um **chatbot tradicional** para uma **experiência de equipe de trabalho virtual**, simulando video calls com avatares especializados que colaboram entre si para resolver as demandas do usuário.

### Por Que Isso Importa

- **Ninguém faz isso** - Não existe SaaS B2B no mundo com esta experiência
- **Novo paradigma de UX** - De "usar software" para "trabalhar com equipe"
- **Humanização da IA** - Reduz a frieza da interação com robôs
- **Diferencial competitivo absoluto** - Impossível de copiar rapidamente
- **Potencial de viralização** - Feature que se vende sozinha

### Status

Esta é uma **visão de longo prazo**, não uma feature de MVP. A implementação está planejada para Fase 2/3 do produto, após validação do core business.

---

## 🎯 O Problema

### Como Funciona Hoje (Mercado)

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│   Usuário digita pergunta                           │
│              ↓                                      │
│   IA processa                                       │
│              ↓                                      │
│   IA responde em texto                              │
│              ↓                                      │
│   Usuário lê e digita próxima pergunta              │
│                                                     │
│   Experiência: FRIA, IMPESSOAL, ROBÓTICA            │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### O Insight

Após a pandemia de COVID-19, o mundo corporativo migrou de reuniões presenciais para **video calls**. As pessoas se acostumaram a resolver problemas complexos "numa call". 

**E se pudéssemos replicar essa experiência com IA?**

Não como um chatbot com avatar, mas como uma **simulação realista de reunião de trabalho** com especialistas virtuais.

---

## 💡 A Solução Proposta

### Experiência do Usuário

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  1. Usuário clica em "Falar com Jurídico"                       │
│              ↓                                                  │
│  2. Tela escurece: "Calling..."                                 │
│              ↓                                                  │
│  3. Notificação: "Dra. Helena quer entrar na reunião"           │
│     [Permitir Entrada]                                          │
│              ↓                                                  │
│  4. Avatar aparece na tela, cumprimenta o usuário pelo nome     │
│              ↓                                                  │
│  5. Conversa por voz (bidirecional) com transcrição ao lado     │
│              ↓                                                  │
│  6. Quando "pensando", avatar olha pra tela e "digita"          │
│              ↓                                                  │
│  7. Se precisar de outro especialista:                          │
│     "Vou chamar o Carlos do setor de Propostas"                 │
│              ↓                                                  │
│  8. Novo avatar entra na call, recebe briefing, executa         │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Layout da Interface

```
┌─────────────────────────────────────────────────────────────────┐
│  🎥 Reunião com Equipe Jurídica                    [Encerrar]   │
├────────────────────────────────┬────────────────────────────────┤
│                                │                                │
│   ┌────────────────────────┐   │   📝 TRANSCRIÇÃO               │
│   │                        │   │                                │
│   │     👩‍⚖️ Dra. Helena     │   │   [14:32] Helena:              │
│   │                        │   │   Olá Paulo, vi que você       │
│   │     (Avatar falando    │   │   está analisando o edital     │
│   │      com lip-sync)     │   │   PE 234/2025. Encontrei       │
│   │                        │   │   3 cláusulas restritivas.     │
│   │                        │   │                                │
│   └────────────────────────┘   │   [14:33] Você:                 │
│                                │   Quais são? Podemos            │
│   🎤 Microfone [Ativo]         │   impugnar?                     │
│                                │                                │
│   Participantes:               │   [14:33] Helena:               │
│   • Dra. Helena (Jurídico)     │   Sim, vou detalhar cada uma   │
│   • Você                       │   com base em jurisprudência   │
│                                │   do TCU...                    │
│                                │                                │
├────────────────────────────────┴────────────────────────────────┤
│  [📎 Compartilhar Edital]  [📋 Gerar Documento]  [➕ Add Pessoa] │
└─────────────────────────────────────────────────────────────────┘
```

### Comportamentos do Avatar

| Situação | Comportamento do Avatar |
|----------|-------------------------|
| Ouvindo usuário | Olha para a câmera, acena com a cabeça |
| Processando (IA pensando) | Olha para baixo/lado, "digita" no teclado |
| Respondendo | Olha para câmera, fala com lip-sync |
| Consultando documentos | Olha para o lado, simula leitura |
| Chamando outro agente | "Deixa eu chamar o especialista..." |
| Aguardando | Postura relaxada, pequenos movimentos |

---

## 👥 Os Agentes Virtuais

### Equipe Proposta

| Avatar | Nome Sugerido | Especialidade | Personalidade |
|--------|---------------|---------------|---------------|
| 👩‍⚖️ | Dra. Helena | Jurídico | Técnica, precisa, cita jurisprudência |
| 👨‍💼 | Carlos | Propostas Comerciais | Prático, focado em ganhar |
| 👩‍💻 | Marina | Análise de Editais | Detalhista, encontra oportunidades |
| 👨‍🔧 | Roberto | Operações/Entregas | Logístico, prazos, execução |
| 👩‍📊 | Fernanda | Financeiro | Números, margens, viabilidade |
| 🤖 | ARIA | Assistente Geral | Versátil, primeiro contato |

### Personalização

O usuário poderá:
- Escolher gênero dos avatares (masculino/feminino)
- Escolher aparência (diferentes opções pré-definidas)
- Definir nomes personalizados
- Ajustar "personalidade" (mais formal/informal)

---

## 🔧 Arquitetura Técnica

### Stack Proposta

```
┌─────────────────────────────────────────────────────────────────┐
│                        FRONTEND                                 │
│  Next.js + React + WebRTC (para áudio) + Video Stream          │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      API GATEWAY                                │
│                    (Supabase Edge Functions)                    │
└─────────────────────────────────────────────────────────────────┘
                              │
          ┌───────────────────┼───────────────────┐
          ▼                   ▼                   ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│   SPEECH-TO-    │ │    CLAUDE       │ │   TEXT-TO-      │
│     TEXT        │ │   (Raciocínio)  │ │    SPEECH       │
│                 │ │                 │ │                 │
│  • Whisper API  │ │  • Opus 4       │ │  • ElevenLabs   │
│  • Deepgram     │ │  • Sonnet 4     │ │  • PlayHT       │
│  • AssemblyAI   │ │                 │ │  • Azure TTS    │
└─────────────────┘ └─────────────────┘ └─────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    AVATAR RENDERING                             │
│                                                                 │
│  Opções:                                                        │
│  • D-ID (Streaming API) - Mais maduro                          │
│  • HeyGen (Streaming Avatar) - Boa qualidade                   │
│  • Simli.ai - Mais barato, low-latency                         │
│  • Tavus - Real-time, novo player                              │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                     VIDEO STREAM                                │
│              WebSocket → Browser (< 500ms latency)              │
└─────────────────────────────────────────────────────────────────┘
```

### Fluxo de Dados

```
1. Usuário fala
       ↓ (WebRTC audio stream)
2. Whisper transcreve
       ↓ (texto, ~1-2s)
3. Claude processa
       ↓ (texto resposta, ~2-4s)
4. ElevenLabs gera áudio
       ↓ (audio stream, ~1-2s)
5. D-ID renderiza avatar
       ↓ (video stream, ~1-2s)
6. Browser exibe
       
Latência total: 5-10 segundos
```

### Otimizações de Latência

| Técnica | Ganho |
|---------|-------|
| Streaming de resposta Claude | Avatar começa a falar antes de terminar de processar |
| Pré-cache de expressões | Animações de "pensando" já prontas |
| Edge computing | Processamento mais perto do usuário |
| Chunked audio | ElevenLabs em pedaços, não espera completar |
| Warm connections | WebSockets sempre abertos |

---

## 💰 Análise de Custos

### Custo por Minuto de Conversa

| Serviço | Custo/minuto | Notas |
|---------|--------------|-------|
| Whisper (STT) | $0.006 | ~150 palavras/min |
| Claude Sonnet | $0.05-0.15 | Depende do contexto |
| ElevenLabs | $0.18 | ~150 palavras/min |
| D-ID Streaming | $0.30-0.60 | Varia por resolução |
| **TOTAL** | **$0.54-0.94** | Por minuto |

### Cenários de Uso

| Cenário | Duração | Custo |
|---------|---------|-------|
| Consulta rápida | 2 min | ~$1.20 |
| Análise de edital | 5 min | ~$3.50 |
| Elaboração de impugnação | 10 min | ~$7.00 |
| Sessão completa | 20 min | ~$14.00 |

### Modelo de Monetização Sugerido

| Plano | Minutos Inclusos | Custo Adicional |
|-------|------------------|-----------------|
| ME/EPP (R$ 247) | 30 min/mês | R$ 2/min extra |
| Média/Grande (R$ 597) | 120 min/mês | R$ 1.50/min extra |
| Prestadora (R$ 497) | 90 min/mês | R$ 1.50/min extra |
| Enterprise | Ilimitado* | Incluso |

*Enterprise: Limite razoável de 500 min/mês, depois cobrança adicional

---

## 📈 Impacto de Mercado

### Por Que Ninguém Fez Isso Ainda

1. **Tecnologia recente** - Avatares real-time viáveis só em 2024/2025
2. **Custo estava alto** - Era $1+/segundo, agora ~$0.50/minuto
3. **Mindset de chatbot** - Empresas pensam em "assistente", não "colega"
4. **Complexidade** - Integrar voz + IA + avatar + streaming é difícil

### O Que Existe Hoje (Competidores Indiretos)

| Produto | O Que Faz | Limitação |
|---------|-----------|-----------|
| Intercom Fin | Chatbot de atendimento | Só texto, sem avatar |
| Synthesia | Avatares para vídeos | Pré-gravado, não real-time |
| Soul Machines | Avatares enterprise | Caríssimo, foco em atendimento |
| HeyGen | Avatares para marketing | Focado em vídeos, não conversação |
| Character.ai | Chatbots com personalidade | Só texto, sem voz real |

**Nenhum oferece:** Avatar real-time + contexto de trabalho B2B + múltiplos agentes colaborando

### Potencial de Disrupção

```
Escala de Impacto:

[Incremental] -------- [Significativo] -------- [Disruptivo]
                                                     ↑
                                              VOCÊ ESTÁ AQUI

Razão: Não é uma feature melhor.
       É um NOVO PARADIGMA de interface.
```

### Aplicações Além de Licitações

Se o conceito funcionar, pode ser aplicado em:

| Vertical | Exemplo de Uso |
|----------|----------------|
| SaaS Contábil | "Fale com seu contador virtual" |
| SaaS Jurídico | "Consulta com advogado virtual" |
| SaaS RH | "Entrevista com recrutador virtual" |
| SaaS Vendas | "Call com SDR virtual" |
| SaaS Saúde | "Triagem com enfermeiro virtual" |
| SaaS Educação | "Aula com professor virtual" |

**Oportunidade:** Licenciar a tecnologia/framework para outros SaaS.

---

## 🗓️ Roadmap de Implementação

### Fase 0: MVP do Core (Atual)
**Foco:** Validar o produto base

- [ ] Captação automática de editais
- [ ] Preenchimento de propostas com IA
- [ ] Kanban visual
- [ ] Agente Jurídico em **texto** (chat tradicional)
- [ ] Dashboard básico

**Entregável:** CRM funcional sem avatares

### Fase 1: Voz Simples (Q2 2026)
**Foco:** Adicionar voz sem avatar

```
┌─────────────────────────────────────────┐
│  🎙️ Agente Jurídico                     │
├─────────────────────────────────────────┤
│  ┌───────┐                              │
│  │ 👩‍⚖️   │  Dra. Helena                 │
│  │ (foto)│  ● Falando...                │
│  └───────┘                              │
│                                         │
│  "Encontrei 3 cláusulas restritivas..." │
│                                         │
│  🎤 [Pressione para falar]              │
└─────────────────────────────────────────┘
```

- [ ] Integração com ElevenLabs (TTS)
- [ ] Integração com Whisper (STT)
- [ ] Avatar estático (foto) com indicador de estado
- [ ] Transcrição da conversa
- [ ] Custo estimado: ~$0.20/minuto

**Entregável:** Conversa por voz com "assistente"

### Fase 2: Avatar Básico (Q4 2026)
**Foco:** Avatar com lip-sync

- [ ] Integração com Simli.ai ou D-ID
- [ ] Lip-sync básico
- [ ] Animações de "pensando", "ouvindo"
- [ ] Beta fechado com clientes premium
- [ ] Coleta de feedback

**Entregável:** Avatar falante, single-agent

### Fase 3: Equipe Virtual Completa (2027)
**Foco:** Experiência completa de "video call"

- [ ] Múltiplos avatares
- [ ] Handoff entre agentes
- [ ] Simulação de "call" (joining, waiting room)
- [ ] Personalização de avatares
- [ ] Integração com ações (gerar documento enquanto conversa)

**Entregável:** Experiência completa conforme visão

### Fase 4: Plataforma (2027+)
**Foco:** Expandir além de licitações

- [ ] Framework reutilizável
- [ ] API para terceiros
- [ ] Licenciamento para outros SaaS
- [ ] Marketplace de "agentes"

**Entregável:** Helion como plataforma de agentes virtuais

---

## ⚠️ Riscos e Mitigações

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| Latência alta (>10s) | Média | Alto | Streaming, animações de "pensando" |
| Custo descontrolado | Alta | Alto | Limites por plano, monitoramento |
| Uncanny valley (avatar estranho) | Média | Alto | Escolher fornecedor premium, testes extensivos |
| Usuários não quererem | Baixa | Alto | Manter chat texto como alternativa |
| Concorrente copiar | Média | Médio | Executar rápido, patentear conceitos |
| Problemas de áudio (ruído) | Média | Médio | Noise cancellation, fallback para texto |

---

## 📊 Métricas de Sucesso

### Fase 1 (Voz Simples)

| Métrica | Meta |
|---------|------|
| % usuários que usam voz vs texto | >30% |
| NPS da feature | >50 |
| Tempo médio de conversa | 3-5 min |
| Custo médio por usuário/mês | <$10 |

### Fase 2+ (Avatar)

| Métrica | Meta |
|---------|------|
| % usuários que preferem avatar | >50% |
| Taxa de conversão (trial → pago) | +20% vs sem avatar |
| Churn reduction | -15% |
| Menções em mídia/social | Viral |
| Willingness to pay premium | +30% |

---

## 🎬 Conclusão

### O Que Temos

Uma visão de produto que:
- **Não existe no mercado** - Oceano azul total
- **É tecnicamente viável** - Stack disponível hoje
- **Tem timing certo** - Janela de oportunidade aberta
- **Diferencia absolutamente** - Impossível de copiar rápido
- **Escala além do produto** - Pode virar plataforma

### O Que Precisamos

1. **Validar o core primeiro** - MVP funcional de CRM
2. **Clientes pagantes** - Provar que o negócio funciona
3. **Capital para investir** - Feature cara de desenvolver
4. **Execução impecável** - Mal feito é pior que não fazer

### Recomendação

Manter esta visão como **norte estratégico**, executar o MVP primeiro, e implementar em fases conforme roadmap. A feature tem potencial de colocar o Helion no mapa global de inovação em SaaS.

---

## 📎 Anexos

### A. Fornecedores de Avatar (Benchmark)

| Fornecedor | Preço | Latência | Qualidade | Notas |
|------------|-------|----------|-----------|-------|
| D-ID | $0.05/s | ~2s | Alta | Mais maduro |
| HeyGen | $0.08/s | ~2s | Alta | Bom suporte |
| Simli.ai | $0.02/s | <1s | Média-Alta | Mais barato |
| Tavus | Custom | <1s | Alta | Novo, promissor |
| Synthesia | N/A | N/A | Alta | Não é real-time |

### B. Fornecedores de TTS (Benchmark)

| Fornecedor | Preço | Latência | Naturalidade | Português BR |
|------------|-------|----------|--------------|--------------|
| ElevenLabs | $0.30/1k chars | <1s | Excelente | Sim |
| PlayHT | $0.20/1k chars | <1s | Muito boa | Sim |
| Azure TTS | $0.01/1k chars | <1s | Boa | Sim |
| Google TTS | $0.004/1k chars | <1s | Média | Sim |

### C. Referências

- D-ID Streaming API: https://docs.d-id.com/
- ElevenLabs API: https://elevenlabs.io/docs
- Simli.ai: https://simli.ai/
- OpenAI Whisper: https://platform.openai.com/docs/guides/speech-to-text
- HeyGen: https://www.heygen.com/

---

> **Documento criado em:** Dezembro 2025  
> **Última atualização:** Dezembro 2025  
> **Autor:** Claude + Paulo (LZR Technologies)  
> **Classificação:** Confidencial
