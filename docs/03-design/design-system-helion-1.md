# Design System - Helion

> **Versão:** 1.0  
> **Data:** Dezembro 2025  
> **Filosofia:** "Parece ter sido feito em 2026"

---

## 📐 1. FILOSOFIA DE DESIGN

### 1.1 Princípios Fundamentais

| Princípio | Descrição | Aplicação |
|-----------|-----------|-----------|
| **Velocidade** | João opera 120 licitações/mês. Cada clique conta. | Atalhos, bulk actions, preenchimento automático |
| **Clareza** | Ricardo quer números, não explicações. | Hierarquia visual clara, KPIs destacados |
| **Confiança** | Licitações envolvem dinheiro público. | Design profissional, não "jovem demais" |
| **Antecipação** | O sistema sabe o que você precisa antes de pedir. | IA invisível, sugestões contextuais |

### 1.2 Pilares de UX

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│   EFICIÊNCIA          PREVISIBILIDADE        CONFIANÇA     │
│   (menos cliques)     (padrões claros)       (sem sustos)  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 1.3 Regras de Ouro

1. **3-Click Rule:** Qualquer ação importante em no máximo 3 cliques
2. **Zero Surprise:** Feedback imediato para toda ação
3. **Smart Defaults:** Pré-preencher sempre que possível
4. **Keyboard First:** Power users usam teclado, não mouse

---

## 🎨 2. PALETA DE CORES

### 2.1 Cores Primárias

**Por que não azul corporativo?** Todos os concorrentes usam azul (#1976D2, #2196F3). Vamos com **Indigo** - ainda transmite confiança, mas é mais sofisticado.

#### Primary - Indigo
```css
--primary-50:  #EEF2FF;  /* Backgrounds sutis */
--primary-100: #E0E7FF;  /* Hover states */
--primary-200: #C7D2FE;  /* Borders */
--primary-300: #A5B4FC;  /* Icons secundários */
--primary-400: #818CF8;  /* Links hover */
--primary-500: #6366F1;  /* ⭐ COR PRINCIPAL - botões, links */
--primary-600: #4F46E5;  /* Hover em botões */
--primary-700: #4338CA;  /* Active states */
--primary-800: #3730A3;  /* Text emphasis */
--primary-900: #312E81;  /* Dark backgrounds */
```

#### Secondary - Slate (Neutros com personalidade)
```css
--slate-50:  #F8FAFC;  /* Page background (light mode) */
--slate-100: #F1F5F9;  /* Cards, containers */
--slate-200: #E2E8F0;  /* Borders, dividers */
--slate-300: #CBD5E1;  /* Disabled states */
--slate-400: #94A3B8;  /* Placeholder text */
--slate-500: #64748B;  /* Secondary text */
--slate-600: #475569;  /* Body text */
--slate-700: #334155;  /* Headings */
--slate-800: #1E293B;  /* Dark text */
--slate-900: #0F172A;  /* Page background (dark mode) */
```

### 2.2 Cores Semânticas

#### Success - Emerald
```css
--success-50:  #ECFDF5;
--success-100: #D1FAE5;
--success-500: #10B981;  /* ⭐ Principal */
--success-600: #059669;
--success-700: #047857;
```
**Uso:** Licitação ganha, documento aprovado, ação concluída

#### Warning - Amber
```css
--warning-50:  #FFFBEB;
--warning-100: #FEF3C7;
--warning-500: #F59E0B;  /* ⭐ Principal */
--warning-600: #D97706;
--warning-700: #B45309;
```
**Uso:** Prazo próximo (< 48h), atenção necessária

#### Error - Rose
```css
--error-50:  #FFF1F2;
--error-100: #FFE4E6;
--error-500: #F43F5E;  /* ⭐ Principal */
--error-600: #E11D48;
--error-700: #BE123C;
```
**Uso:** Prazo vencido, erro, documento faltando

#### Info - Sky
```css
--info-50:  #F0F9FF;
--info-100: #E0F2FE;
--info-500: #0EA5E9;  /* ⭐ Principal */
--info-600: #0284C7;
--info-700: #0369A1;
```
**Uso:** Informações, dicas, novidades

### 2.3 Cores de Status (Kanban)

```css
/* Status das Licitações */
--status-novo:        #6366F1;  /* Indigo - Novo/Captado */
--status-analise:     #8B5CF6;  /* Violet - Em Análise */
--status-preparacao:  #F59E0B;  /* Amber - Em Preparação */
--status-enviado:     #0EA5E9;  /* Sky - Proposta Enviada */
--status-disputa:     #EC4899;  /* Pink - Em Disputa */
--status-ganho:       #10B981;  /* Emerald - Ganho */
--status-perdido:     #64748B;  /* Slate - Perdido */
--status-contrato:    #14B8A6;  /* Teal - Em Contrato */
--status-entrega:     #F97316;  /* Orange - Em Entrega */
--status-pagamento:   #22C55E;  /* Green - Aguardando Pagamento */
--status-concluido:   #6B7280;  /* Gray - Concluído */
```

### 2.4 Cores Especiais

```css
/* IA / Agente Jurídico */
--ai-gradient-start: #818CF8;  /* Indigo 400 */
--ai-gradient-end:   #C084FC;  /* Purple 400 */
--ai-glow:           rgba(129, 140, 248, 0.3);

/* Glassmorphism */
--glass-bg:          rgba(255, 255, 255, 0.7);
--glass-border:      rgba(255, 255, 255, 0.3);
--glass-blur:        12px;

/* Dark Mode Overrides */
--dark-glass-bg:     rgba(15, 23, 42, 0.8);
--dark-glass-border: rgba(255, 255, 255, 0.1);
```

### 2.5 Aplicação de Cores

| Elemento | Light Mode | Dark Mode |
|----------|------------|-----------|
| Background | `slate-50` | `slate-900` |
| Cards | `white` | `slate-800` |
| Text Primary | `slate-800` | `slate-100` |
| Text Secondary | `slate-500` | `slate-400` |
| Borders | `slate-200` | `slate-700` |
| Primary Button | `primary-500` | `primary-500` |
| Links | `primary-600` | `primary-400` |

---

## 🔤 3. TIPOGRAFIA

### 3.1 Font Stack

**Headings:** Inter (Google Fonts)
```css
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

**Body:** Inter (consistência)
```css
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

**Mono (código, dados):** JetBrains Mono
```css
font-family: 'JetBrains Mono', 'Fira Code', 'Consolas', monospace;
```

**Por que Inter?**
- Excelente legibilidade em telas
- Suporte a números tabulares (alinhamento em tabelas)
- Variable font (pesos 100-900)
- Grátis e bem mantida

### 3.2 Escala Tipográfica

```css
/* Display - Hero, páginas especiais */
--text-display:   3rem;      /* 48px */
--leading-display: 1.1;

/* Headings */
--text-h1:        2.25rem;   /* 36px */
--text-h2:        1.875rem;  /* 30px */
--text-h3:        1.5rem;    /* 24px */
--text-h4:        1.25rem;   /* 20px */
--text-h5:        1.125rem;  /* 18px */
--text-h6:        1rem;      /* 16px */

/* Body */
--text-lg:        1.125rem;  /* 18px - Texto destacado */
--text-base:      1rem;      /* 16px - Padrão */
--text-sm:        0.875rem;  /* 14px - Secundário */
--text-xs:        0.75rem;   /* 12px - Labels, captions */

/* Line Heights */
--leading-tight:  1.25;
--leading-normal: 1.5;
--leading-relaxed: 1.625;
```

### 3.3 Font Weights

```css
--font-normal:    400;  /* Body text */
--font-medium:    500;  /* Emphasis, labels */
--font-semibold:  600;  /* Subheadings, buttons */
--font-bold:      700;  /* Headings */
```

### 3.4 Hierarquia de Texto

| Uso | Tamanho | Peso | Cor | Exemplo |
|-----|---------|------|-----|---------|
| Page Title | h1 (36px) | Bold | slate-800 | "Dashboard" |
| Section Title | h2 (30px) | Bold | slate-800 | "Licitações em Andamento" |
| Card Title | h3 (24px) | Semibold | slate-700 | "Pregão 123/2025" |
| Subsection | h4 (20px) | Semibold | slate-700 | "Documentos Anexados" |
| Body | base (16px) | Normal | slate-600 | Textos gerais |
| Secondary | sm (14px) | Normal | slate-500 | Descrições |
| Label | xs (12px) | Medium | slate-500 | "PRAZO" |
| Mono/Data | sm (14px) | Normal | slate-600 | "R$ 1.234.567,89" |

### 3.5 Números

```css
/* Usar números tabulares para alinhamento em tabelas */
font-variant-numeric: tabular-nums;

/* Valores monetários - sempre mono */
.currency {
  font-family: 'JetBrains Mono', monospace;
  font-variant-numeric: tabular-nums;
}
```

---

## 📐 4. ESPAÇAMENTO E GRID

### 4.1 Sistema de Espaçamento (8px base)

```css
--space-0:   0;
--space-1:   0.25rem;   /* 4px */
--space-2:   0.5rem;    /* 8px */
--space-3:   0.75rem;   /* 12px */
--space-4:   1rem;      /* 16px */
--space-5:   1.25rem;   /* 20px */
--space-6:   1.5rem;    /* 24px */
--space-8:   2rem;      /* 32px */
--space-10:  2.5rem;    /* 40px */
--space-12:  3rem;      /* 48px */
--space-16:  4rem;      /* 64px */
--space-20:  5rem;      /* 80px */
--space-24:  6rem;      /* 96px */
```

### 4.2 Grid System

**Container Widths:**
```css
--container-sm:   640px;
--container-md:   768px;
--container-lg:   1024px;
--container-xl:   1280px;
--container-2xl:  1536px;
```

**Layout Grid (Bento-style):**
```
┌────────────────────────────────────────────────────────┐
│ Sidebar │              Main Content                    │
│  240px  │              flex-1                          │
│         │                                              │
│ ┌─────┐ │  ┌──────────┬──────────┬──────────┐        │
│ │ Nav │ │  │  Widget  │  Widget  │  Widget  │        │
│ │     │ │  │   1x1    │   1x1    │   1x1    │        │
│ │     │ │  ├──────────┴──────────┼──────────┤        │
│ │     │ │  │      Widget         │  Widget  │        │
│ │     │ │  │        2x1          │   1x2    │        │
│ │     │ │  ├──────────┬──────────┤          │        │
│ │     │ │  │  Widget  │  Widget  │          │        │
│ │     │ │  │   1x1    │   1x1    │          │        │
│ └─────┘ │  └──────────┴──────────┴──────────┘        │
└────────────────────────────────────────────────────────┘
```

**Gap padrão:** 24px (space-6)

### 4.3 Breakpoints

```css
--breakpoint-sm:   640px;   /* Mobile landscape */
--breakpoint-md:   768px;   /* Tablet */
--breakpoint-lg:   1024px;  /* Laptop */
--breakpoint-xl:   1280px;  /* Desktop */
--breakpoint-2xl:  1536px;  /* Large desktop */
```

---

## 🧩 5. COMPONENTES

### 5.1 Botões

#### Variantes

```
┌─────────────────────────────────────────────────────────┐
│  Primary    │  Secondary  │  Ghost      │  Danger     │
│  ┌───────┐  │  ┌───────┐  │  ┌───────┐  │  ┌───────┐  │
│  │ Salvar│  │  │Cancelar│ │  │ Editar│  │  │Excluir│  │
│  └───────┘  │  └───────┘  │  └───────┘  │  └───────┘  │
│  bg-primary │  bg-slate   │  bg-transp  │  bg-error   │
│  text-white │  text-slate │  text-slate │  text-white │
└─────────────────────────────────────────────────────────┘
```

#### Especificações

| Variante | Background | Text | Border | Hover |
|----------|------------|------|--------|-------|
| Primary | primary-500 | white | none | primary-600 |
| Secondary | slate-100 | slate-700 | slate-200 | slate-200 |
| Ghost | transparent | slate-600 | none | slate-100 |
| Danger | error-500 | white | none | error-600 |
| Success | success-500 | white | none | success-600 |

#### Tamanhos

| Size | Height | Padding X | Font Size | Border Radius |
|------|--------|-----------|-----------|---------------|
| xs | 28px | 12px | 12px | 6px |
| sm | 32px | 14px | 14px | 6px |
| md | 40px | 16px | 14px | 8px |
| lg | 48px | 20px | 16px | 8px |
| xl | 56px | 24px | 18px | 10px |

#### Estados

```css
/* Focus - Acessibilidade */
.btn:focus-visible {
  outline: 2px solid var(--primary-500);
  outline-offset: 2px;
}

/* Loading */
.btn--loading {
  opacity: 0.7;
  pointer-events: none;
}

/* Disabled */
.btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
```

### 5.2 Cards

#### Card Padrão

```
┌─────────────────────────────────────────┐
│ ○ Header (opcional)            ⋮ Menu  │
├─────────────────────────────────────────┤
│                                         │
│  Conteúdo do Card                       │
│                                         │
│                                         │
├─────────────────────────────────────────┤
│ Footer (opcional)              [Action] │
└─────────────────────────────────────────┘
```

```css
.card {
  background: white;
  border: 1px solid var(--slate-200);
  border-radius: 12px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  overflow: hidden;
}

.card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--slate-300);
}

/* Dark mode */
.dark .card {
  background: var(--slate-800);
  border-color: var(--slate-700);
}
```

#### Card de Licitação (Kanban)

```
┌─────────────────────────────────────────┐
│ ● Em Análise              Yamaha Motor │
├─────────────────────────────────────────┤
│ Pregão Eletrônico 234/2025              │
│ Prefeitura de São Paulo                 │
│                                         │
│ 🏷 Motocicletas, Veículos               │
│                                         │
│ 💰 R$ 2.450.000,00                      │
├─────────────────────────────────────────┤
│ ⏰ 2 dias restantes        👤 João      │
└─────────────────────────────────────────┘
```

### 5.3 Inputs

#### Text Input

```css
.input {
  height: 40px;
  padding: 0 12px;
  font-size: 14px;
  border: 1px solid var(--slate-300);
  border-radius: 8px;
  background: white;
  transition: all 0.15s ease;
}

.input:hover {
  border-color: var(--slate-400);
}

.input:focus {
  border-color: var(--primary-500);
  box-shadow: 0 0 0 3px var(--primary-100);
  outline: none;
}

.input::placeholder {
  color: var(--slate-400);
}

/* Estados */
.input--error {
  border-color: var(--error-500);
}

.input--success {
  border-color: var(--success-500);
}
```

#### Select

```css
.select {
  /* Same as input */
  appearance: none;
  background-image: url("data:image/svg+xml,..."); /* Chevron down */
  background-repeat: no-repeat;
  background-position: right 12px center;
  padding-right: 36px;
}
```

#### Checkbox & Radio

```
☐ Checkbox unchecked       ○ Radio unchecked
☑ Checkbox checked         ● Radio checked
```

```css
.checkbox {
  width: 18px;
  height: 18px;
  border: 2px solid var(--slate-300);
  border-radius: 4px;
}

.checkbox:checked {
  background: var(--primary-500);
  border-color: var(--primary-500);
}
```

### 5.4 Badges / Tags

```
┌──────────┐  ┌──────────┐  ┌──────────┐
│ ● Novo   │  │ ● Urgente│  │ ● Ganho  │
└──────────┘  └──────────┘  └──────────┘
   Indigo        Amber        Emerald
```

```css
.badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 4px 10px;
  font-size: 12px;
  font-weight: 500;
  border-radius: 9999px; /* Pill shape */
}

.badge--primary {
  background: var(--primary-100);
  color: var(--primary-700);
}

.badge--success {
  background: var(--success-100);
  color: var(--success-700);
}

.badge--warning {
  background: var(--warning-100);
  color: var(--warning-700);
}

.badge--error {
  background: var(--error-100);
  color: var(--error-700);
}
```

### 5.5 Tabelas

```
┌─────────────────────────────────────────────────────────────┐
│ □  Licitação          Órgão           Valor      Prazo     │
├─────────────────────────────────────────────────────────────┤
│ □  PE 123/2025       Pref. SP     R$ 1.2M     2 dias  ●   │
│ □  PE 124/2025       Min. Saúde   R$ 3.4M     5 dias  ●   │
│ □  PE 125/2025       INSS         R$ 890K     Vencido ●   │
└─────────────────────────────────────────────────────────────┘
  ← 1 2 3 ... 10 →
```

```css
.table {
  width: 100%;
  border-collapse: collapse;
}

.table th {
  text-align: left;
  font-size: 12px;
  font-weight: 600;
  color: var(--slate-500);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 12px 16px;
  border-bottom: 1px solid var(--slate-200);
}

.table td {
  padding: 16px;
  border-bottom: 1px solid var(--slate-100);
  font-size: 14px;
}

.table tr:hover {
  background: var(--slate-50);
}
```

### 5.6 Modal / Dialog

```
┌─────────────────────────────────────────┐
│                               [×]       │
│                                         │
│   ⚠️                                    │
│                                         │
│   Confirmar Exclusão                    │
│                                         │
│   Tem certeza que deseja excluir        │
│   esta licitação? Esta ação não         │
│   pode ser desfeita.                    │
│                                         │
│         [Cancelar]  [Excluir]           │
│                                         │
└─────────────────────────────────────────┘
```

```css
.modal-overlay {
  background: rgba(15, 23, 42, 0.5);
  backdrop-filter: blur(4px);
}

.modal {
  background: white;
  border-radius: 16px;
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
  max-width: 480px;
  padding: 24px;
}
```

### 5.7 Toast / Notifications

```
┌─────────────────────────────────────────┐
│ ✓  Licitação salva com sucesso    [×]  │
└─────────────────────────────────────────┘
```

```css
.toast {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 16px;
  border-radius: 8px;
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
  font-size: 14px;
}

.toast--success {
  background: var(--success-50);
  border-left: 4px solid var(--success-500);
  color: var(--success-800);
}

.toast--error {
  background: var(--error-50);
  border-left: 4px solid var(--error-500);
  color: var(--error-800);
}

.toast--warning {
  background: var(--warning-50);
  border-left: 4px solid var(--warning-500);
  color: var(--warning-800);
}
```

### 5.8 Sidebar Navigation

```
┌──────────────────────┐
│  🌟 HELION           │
├──────────────────────┤
│                      │
│  ▣ Dashboard         │
│  ◉ Licitações        │  ← Active
│  ◎ Captação          │
│  ◎ Contratos         │
│  ◎ Entregas          │
│  ◎ Financeiro        │
│                      │
├──────────────────────┤
│  FERRAMENTAS         │
│  ◎ Agente Jurídico   │
│  ◎ Robô de Lances    │
│  ◎ Relatórios        │
│                      │
├──────────────────────┤
│  ◎ Configurações     │
│  ◎ Ajuda             │
└──────────────────────┘
```

```css
.sidebar {
  width: 240px;
  background: white;
  border-right: 1px solid var(--slate-200);
  height: 100vh;
  position: fixed;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 10px 16px;
  font-size: 14px;
  color: var(--slate-600);
  border-radius: 8px;
  margin: 2px 8px;
  transition: all 0.15s ease;
}

.nav-item:hover {
  background: var(--slate-100);
  color: var(--slate-800);
}

.nav-item--active {
  background: var(--primary-50);
  color: var(--primary-700);
  font-weight: 500;
}
```

---

## 🎭 6. ICONOGRAFIA

### 6.1 Biblioteca de Ícones

**Escolha:** Lucide Icons (fork do Feather Icons)
- Consistentes
- Leves (SVG)
- Open source
- Fácil integração com React

**URL:** https://lucide.dev

### 6.2 Tamanhos de Ícones

| Contexto | Tamanho | Uso |
|----------|---------|-----|
| Inline (text) | 16px | Junto a texto |
| Button | 18px | Dentro de botões |
| Navigation | 20px | Menu lateral |
| Card | 24px | Headers de cards |
| Empty State | 48px | Estados vazios |
| Hero | 64px | Destaque |

### 6.3 Ícones do Sistema

```
Dashboard    → LayoutDashboard
Licitações   → FileText
Captação     → Search
Contratos    → FileCheck
Entregas     → Truck
Financeiro   → DollarSign
Agente IA    → Bot / Sparkles
Robô Lances  → Zap
Relatórios   → BarChart3
Config       → Settings
Ajuda        → HelpCircle
Notificação  → Bell
Usuário      → User
Logout       → LogOut
Adicionar    → Plus
Editar       → Pencil
Excluir      → Trash2
Filtrar      → Filter
Buscar       → Search
Upload       → Upload
Download     → Download
Calendário   → Calendar
Prazo        → Clock
Dinheiro     → DollarSign
Documento    → FileText
Anexo        → Paperclip
Check        → Check
X            → X
Alerta       → AlertTriangle
Info         → Info
Success      → CheckCircle
Error        → XCircle
Expandir     → ChevronDown
Colapsar     → ChevronUp
Menu         → MoreHorizontal
```

### 6.4 Cor dos Ícones

```css
/* Ícones seguem a cor do texto pai */
.icon {
  color: currentColor;
}

/* Ícones de status */
.icon--success { color: var(--success-500); }
.icon--warning { color: var(--warning-500); }
.icon--error   { color: var(--error-500); }
.icon--info    { color: var(--info-500); }
```

---

## ✨ 7. MOTION & ANIMAÇÕES

### 7.1 Princípios

1. **Propósito > Decoração** - Toda animação deve ter função
2. **Rápido > Lento** - Usuários de licitação têm pressa
3. **Sutil > Chamativo** - Não distrair do conteúdo

### 7.2 Durations

```css
--duration-instant:  75ms;   /* Micro-feedback */
--duration-fast:     150ms;  /* Hovers, toggles */
--duration-normal:   200ms;  /* Transições padrão */
--duration-slow:     300ms;  /* Modais, expansões */
--duration-slower:   500ms;  /* Animações complexas */
```

### 7.3 Easing

```css
--ease-in:       cubic-bezier(0.4, 0, 1, 1);
--ease-out:      cubic-bezier(0, 0, 0.2, 1);
--ease-in-out:   cubic-bezier(0.4, 0, 0.2, 1);
--ease-bounce:   cubic-bezier(0.68, -0.55, 0.265, 1.55);
```

### 7.4 Animações Padrão

#### Hover em Cards
```css
.card {
  transition: transform var(--duration-fast) var(--ease-out),
              box-shadow var(--duration-fast) var(--ease-out);
}

.card:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
}
```

#### Entrada de Modal
```css
@keyframes modal-enter {
  from {
    opacity: 0;
    transform: scale(0.95) translateY(-10px);
  }
  to {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}

.modal {
  animation: modal-enter var(--duration-slow) var(--ease-out);
}
```

#### Toast Slide-in
```css
@keyframes toast-enter {
  from {
    opacity: 0;
    transform: translateX(100%);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
```

#### Loading Skeleton
```css
@keyframes shimmer {
  0% { background-position: -200% 0; }
  100% { background-position: 200% 0; }
}

.skeleton {
  background: linear-gradient(
    90deg,
    var(--slate-200) 25%,
    var(--slate-100) 50%,
    var(--slate-200) 75%
  );
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
}
```

#### Spinner
```css
@keyframes spin {
  to { transform: rotate(360deg); }
}

.spinner {
  width: 20px;
  height: 20px;
  border: 2px solid var(--slate-200);
  border-top-color: var(--primary-500);
  border-radius: 50%;
  animation: spin 0.6s linear infinite;
}
```

### 7.5 Micro-delights

#### Confetti (Licitação Ganha)
```javascript
// Usar biblioteca: canvas-confetti
confetti({
  particleCount: 100,
  spread: 70,
  origin: { y: 0.6 },
  colors: ['#6366F1', '#10B981', '#F59E0B']
});
```

#### Pulse (Novo Item)
```css
@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}

.new-item {
  animation: pulse 2s ease-in-out 3; /* 3 vezes */
}
```

### 7.6 AI Visual Feedback

```css
/* Gradiente animado quando IA está "pensando" */
@keyframes ai-thinking {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.ai-thinking {
  background: linear-gradient(
    90deg,
    var(--ai-gradient-start),
    var(--ai-gradient-end),
    var(--ai-gradient-start)
  );
  background-size: 200% 200%;
  animation: ai-thinking 2s ease infinite;
}

/* Glow pulsante */
@keyframes ai-glow {
  0%, 100% { box-shadow: 0 0 20px var(--ai-glow); }
  50% { box-shadow: 0 0 40px var(--ai-glow); }
}

.ai-active {
  animation: ai-glow 2s ease-in-out infinite;
}
```

---

## 🔔 8. FEEDBACK & ESTADOS

### 8.1 Estados de Componentes

| Estado | Visual | Exemplo |
|--------|--------|---------|
| Default | Normal | Botão padrão |
| Hover | Sutil highlight | Background levemente mais escuro |
| Focus | Ring de foco | Outline 2px primary |
| Active | Pressed | Scale 0.98, background mais escuro |
| Disabled | Opaco | Opacity 0.5, cursor not-allowed |
| Loading | Spinner | Substituir texto por spinner |
| Error | Vermelho | Border/background error |
| Success | Verde | Border/background success |

### 8.2 Empty States

```
┌─────────────────────────────────────────┐
│                                         │
│              📭                         │
│                                         │
│     Nenhuma licitação encontrada        │
│                                         │
│     Tente ajustar os filtros ou         │
│     aguarde novas captações             │
│                                         │
│         [Limpar Filtros]                │
│                                         │
└─────────────────────────────────────────┘
```

### 8.3 Error States

```
┌─────────────────────────────────────────┐
│                                         │
│              ⚠️                         │
│                                         │
│     Ops! Algo deu errado                │
│                                         │
│     Não conseguimos carregar as         │
│     licitações. Tente novamente.        │
│                                         │
│         [Tentar Novamente]              │
│                                         │
└─────────────────────────────────────────┘
```

### 8.4 Loading States

```
┌─────────────────────────────────────────┐
│  ▓▓▓▓▓▓▓▓▓░░░░░░░░  Skeleton           │
│  ▓▓▓▓▓▓▓▓▓▓▓▓░░░░░  Carregando...      │
│  ▓▓▓▓▓▓░░░░░░░░░░░                     │
└─────────────────────────────────────────┘
```

### 8.5 Alertas de Prazo

| Situação | Cor | Ícone | Mensagem |
|----------|-----|-------|----------|
| > 7 dias | slate | Clock | "X dias restantes" |
| 3-7 dias | info | Clock | "X dias restantes" |
| 1-2 dias | warning | AlertTriangle | "Prazo próximo!" |
| Hoje | error | AlertTriangle | "Vence hoje!" |
| Vencido | error | XCircle | "Prazo vencido" |

---

## ♿ 9. ACESSIBILIDADE

### 9.1 Contraste

**WCAG AA Mínimo:**
- Texto normal: 4.5:1
- Texto grande (18px+): 3:1
- Elementos interativos: 3:1

**Nossa paleta já atende:**
- primary-500 em branco: ✅ 4.5:1+
- slate-600 em branco: ✅ 5.7:1
- error-500 em branco: ✅ 4.5:1+

### 9.2 Focus Visible

```css
/* Sempre mostrar focus para navegação por teclado */
*:focus-visible {
  outline: 2px solid var(--primary-500);
  outline-offset: 2px;
}

/* Remover outline para mouse */
*:focus:not(:focus-visible) {
  outline: none;
}
```

### 9.3 Tamanhos Mínimos

- **Touch targets:** Mínimo 44x44px
- **Clickable areas:** Mínimo 32x32px
- **Font size:** Mínimo 14px para body, 12px para labels

### 9.4 Screen Readers

```html
<!-- Labels descritivos -->
<button aria-label="Excluir licitação PE 123/2025">
  <TrashIcon />
</button>

<!-- Status anunciado -->
<div role="status" aria-live="polite">
  Licitação salva com sucesso
</div>

<!-- Loading state -->
<button aria-busy="true" aria-disabled="true">
  <Spinner /> Salvando...
</button>
```

### 9.5 Navegação por Teclado

| Ação | Tecla |
|------|-------|
| Próximo item | Tab |
| Item anterior | Shift + Tab |
| Ativar | Enter / Space |
| Fechar modal | Escape |
| Navegação em lista | Arrow keys |

---

## 🌗 10. DARK MODE

### 10.1 Estratégia

**Abordagem:** Dark mode como opção, não padrão
**Detecção:** Respeitar `prefers-color-scheme` do sistema

### 10.2 Mapeamento de Cores

| Token | Light Mode | Dark Mode |
|-------|------------|-----------|
| --bg-page | slate-50 | slate-900 |
| --bg-card | white | slate-800 |
| --bg-elevated | white | slate-700 |
| --text-primary | slate-800 | slate-100 |
| --text-secondary | slate-500 | slate-400 |
| --border | slate-200 | slate-700 |
| --hover | slate-100 | slate-700 |

### 10.3 Implementação

```css
:root {
  /* Light mode (default) */
  --bg-page: var(--slate-50);
  --bg-card: white;
  --text-primary: var(--slate-800);
  /* ... */
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-page: var(--slate-900);
    --bg-card: var(--slate-800);
    --text-primary: var(--slate-100);
    /* ... */
  }
}

/* Manual toggle */
[data-theme="dark"] {
  --bg-page: var(--slate-900);
  --bg-card: var(--slate-800);
  --text-primary: var(--slate-100);
  /* ... */
}
```

### 10.4 Considerações

- **Imagens:** Não inverter, mas considerar overlay sutil
- **Shadows:** Aumentar opacidade em dark mode
- **Borders:** Mais visíveis em dark mode
- **Primary color:** Mesmo tom, funciona bem em ambos

---

## 📱 11. RESPONSIVIDADE

### 11.1 Abordagem

**Mobile-first:** Estilos base para mobile, adicionar para desktop

### 11.2 Layout por Breakpoint

| Breakpoint | Sidebar | Columns | Cards |
|------------|---------|---------|-------|
| < 640px | Hidden (hamburger) | 1 | Full width |
| 640-768px | Hidden | 2 | 50% |
| 768-1024px | Collapsed (icons) | 2-3 | 33% |
| 1024-1280px | Full | 3-4 | 25% |
| > 1280px | Full | 4+ | Bento grid |

### 11.3 Touch Optimizations

```css
@media (hover: none) {
  /* Remove hover effects em touch */
  .card:hover {
    transform: none;
  }
  
  /* Aumentar touch targets */
  .btn {
    min-height: 48px;
  }
}
```

---

## 🎯 12. PATTERNS ESPECÍFICOS

### 12.1 Kanban Board

```
┌─────────────────────────────────────────────────────────────────┐
│ Novo (5)    │ Análise (3)  │ Preparação (4) │ Enviado (2)      │
├─────────────┼──────────────┼────────────────┼──────────────────┤
│ ┌─────────┐ │ ┌─────────┐  │ ┌─────────┐    │ ┌─────────┐      │
│ │ Card 1  │ │ │ Card 4  │  │ │ Card 7  │    │ │ Card 11 │      │
│ └─────────┘ │ └─────────┘  │ └─────────┘    │ └─────────┘      │
│ ┌─────────┐ │ ┌─────────┐  │ ┌─────────┐    │ ┌─────────┐      │
│ │ Card 2  │ │ │ Card 5  │  │ │ Card 8  │    │ │ Card 12 │      │
│ └─────────┘ │ └─────────┘  │ └─────────┘    │ └─────────┘      │
│     ...     │     ...      │     ...        │                  │
└─────────────┴──────────────┴────────────────┴──────────────────┘
```

- Drag & drop para mover cards
- Scroll horizontal em mobile
- Contador em cada coluna
- Cor do header = cor do status

### 12.2 Dashboard Bento

```
┌────────────────────┬────────────────────┬──────────────────────┐
│                    │                    │                      │
│   KPI Card         │   KPI Card         │   KPI Card           │
│   Licitações       │   Taxa de          │   Valor Total        │
│   Ativas: 45       │   Sucesso: 67%     │   R$ 12.5M           │
│                    │                    │                      │
├────────────────────┴────────────────────┼──────────────────────┤
│                                         │                      │
│   Gráfico de Pipeline                   │   Próximos           │
│   (Donut ou Bar)                        │   Prazos             │
│                                         │   • PE 123 - 2d      │
│                                         │   • PE 124 - 3d      │
│                                         │   • PE 125 - 5d      │
├─────────────────────────────────────────┴──────────────────────┤
│                                                                │
│   Atividade Recente                                            │
│   ────────────────────────────────────────────────             │
│   • João moveu PE 123 para "Em Análise"          há 5 min     │
│   • Sistema captou 3 novas licitações            há 15 min    │
│   • Maria enviou proposta PE 120                 há 1 hora    │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

### 12.3 Agente Jurídico (AI Chat)

```
┌────────────────────────────────────────────────────────────────┐
│  🤖 Agente Jurídico                                      [−]  │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│  ┌──────────────────────────────────────────────────────────┐ │
│  │ 👤 Analise o edital PE 234/2025 e identifique cláusulas  │ │
│  │    restritivas que possam ser impugnadas                 │ │
│  └──────────────────────────────────────────────────────────┘ │
│                                                                │
│  ┌──────────────────────────────────────────────────────────┐ │
│  │ 🤖 Encontrei 3 potenciais cláusulas restritivas:         │ │
│  │                                                          │ │
│  │ 1. **Item 5.2** - Exigência de capital social mínimo    │ │
│  │    de R$ 500.000,00 (pode ser desproporcional)          │ │
│  │    📚 TCU Acórdão 1214/2018                             │ │
│  │                                                          │ │
│  │ 2. **Item 7.1** - Atestado com volume mínimo de 50%     │ │
│  │    (acima do usual de 30%)                              │ │
│  │    📚 TCU Acórdão 2088/2019                             │ │
│  │                                                          │ │
│  │ [Gerar Impugnação]  [Gerar Esclarecimento]              │ │
│  └──────────────────────────────────────────────────────────┘ │
│                                                                │
│  ┌──────────────────────────────────────────────────────────┐ │
│  │ ✏️ Digite sua mensagem...                         [➤]   │ │
│  └──────────────────────────────────────────────────────────┘ │
└────────────────────────────────────────────────────────────────┘
```

**Visual do AI:**
- Ícone com gradiente (ai-gradient)
- Mensagens do bot com background sutil
- Botões de ação inline
- Referências clicáveis (TCU)

---

## 🖼️ 13. BRAND ASSETS

### 13.1 Logo

**Nome:** Helion
**Conceito:** Sol (Helios) + tecnologia

```
       ☀️
    H E L I O N
```

**Variações:**
- Logo completo (ícone + texto)
- Logo compacto (só ícone)
- Logo invertido (para fundos escuros)

**Cores do logo:**
- Primary: Indigo (#6366F1)
- Accent: Amber (#F59E0B) - detalhe solar

### 13.2 Favicon

- 16x16, 32x32, 180x180 (Apple)
- SVG para escalabilidade
- Versão simplificada do ícone

### 13.3 OG Images

- 1200x630px para social sharing
- Background com gradiente sutil
- Logo + tagline

---

## 📋 14. CHECKLIST DE IMPLEMENTAÇÃO

### Fase 1 - Setup
- [ ] Configurar Tailwind CSS com tokens customizados
- [ ] Importar Inter e JetBrains Mono
- [ ] Instalar Lucide Icons
- [ ] Configurar dark mode toggle
- [ ] Criar componentes base (Button, Input, Card)

### Fase 2 - Componentes
- [ ] Badge/Tag
- [ ] Table
- [ ] Modal
- [ ] Toast
- [ ] Sidebar
- [ ] Dropdown
- [ ] Tooltip
- [ ] Tabs

### Fase 3 - Patterns
- [ ] Kanban Board
- [ ] Dashboard Bento
- [ ] Chat Interface (AI)
- [ ] Data Table com filtros
- [ ] Form layouts

### Fase 4 - Polish
- [ ] Animações e transições
- [ ] Empty states
- [ ] Error states
- [ ] Loading states
- [ ] Micro-delights

---

## 🔗 15. RECURSOS

### Tokens para Tailwind

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          50: '#EEF2FF',
          100: '#E0E7FF',
          200: '#C7D2FE',
          300: '#A5B4FC',
          400: '#818CF8',
          500: '#6366F1',
          600: '#4F46E5',
          700: '#4338CA',
          800: '#3730A3',
          900: '#312E81',
        },
        // ... demais cores
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', 'sans-serif'],
        mono: ['JetBrains Mono', 'monospace'],
      },
      borderRadius: {
        'sm': '6px',
        'DEFAULT': '8px',
        'md': '10px',
        'lg': '12px',
        'xl': '16px',
      },
    },
  },
}
```

### Links Úteis

- **Cores:** https://tailwindcss.com/docs/colors
- **Inter Font:** https://fonts.google.com/specimen/Inter
- **JetBrains Mono:** https://www.jetbrains.com/lp/mono/
- **Lucide Icons:** https://lucide.dev
- **Canvas Confetti:** https://www.npmjs.com/package/canvas-confetti

---

> **Próximo passo:** Criar protótipo navegável no V0/Figma com este Design System aplicado.
