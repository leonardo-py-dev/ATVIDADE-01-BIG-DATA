# Plano de Implementação - Página de Apresentação de Business Intelligence

Este plano descreve os passos para criar uma página de apresentação de BI de alto nível com um estilo de design "Futurista Corporativo".

## Revisão do Usuário Necessária

> [!IMPORTANT]
> Esta implementação sobrescreve completamente `HTML/interface.html` e `CSS/style.css` que estavam vazios.

## Alterações Propostas

### Arquitetura CSS (`CSS/style.css`)

- **Variáveis (`:root`)**:
  - Cores: Carvão Profundo (#0B0E14), Secundária (#171C26 + opacidade), Índigo (#6366F1), Esmeralda (#10B981), Rose (#F43F5E).
  - Fontes: 'Inter', sans-serif.
  - Efeitos: Filtros de brilho (Glow), bordas de vidro (`1px solid rgba(255,255,255,0.1)`).
- **Reset Global**: Box-sizing, remoção de margens/preenchimentos.
- **Tipografia**:
  - `line-height: 1.6` para o corpo.
  - `letter-spacing: -0.02em` para títulos.
- **Layout**: FLEXBOX e GRID para responsividade (Foco em 1920x1080 + Tablet).
- **Animações e Transições**:
  - **Animações de Entrada**: `@keyframes fade-in-up` para entrada escalonada de elementos.
  - **Efeitos de Hover**: `transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1)` para cards e botões.
  - **Rolagem Suave**: `html { scroll-behavior: smooth; }`
- **Componentes**:
  - `.card`: Efeito Glassmorphism, transições no hover (elevação e brilho).
  - `.glow-bg`: Brilhos de fundo em posição fixa.
  - `.comparison-card`: Layout específico para comparar conceitos.

### Estrutura HTML (`HTML/interface.html`)

- **Head**: Meta tags, Título, Link do Google Fonts (Inter).
- **Body**:
  - **Elementos de Brilho de Fundo**: Divs para iluminação ambiente.
  - **Cabeçalho**:
    - Título: "Business Intelligence"
    - Subtítulo: "Da Informação à Inteligência Estratégica"
    - _Animação_: Fade in vindo do topo.
  - **Conteúdo Principal**:
    - **Seção 1: O Que é BI?**
      - Definição conceitual.
      - Representação visual do ciclo: Coleta -> Tratamento -> Análise -> Visualização -> Decisão.
      - _Animação_: Fade-in escalonado dos passos do ciclo.
    - **Seção 2: Por Que BI? (Impacto)**
      - Cards para: Redução de Incerteza, Padrões Invisíveis, ROI.
      - _Animação_: Cards deslizam para cima ao rolar (usando Intersection Observer).
    - **Seção 3: O Ecossistema de Dados**
      - **Cards de Comparação**:
        - BI vs Big Data (Navio vs Oceano).
        - BI vs Data Science (Descritivo vs Preditivo).
        - Data Warehouse vs Data Lake (Biblioteca vs Armazém).
      - _Animação_: Cards aparecem com ênfase.
  - **Rodapé**: Copyright/Encerramento.

## Plano de Verificação

### Verificação Manual

- **Abrir `HTML/interface.html` em um navegador.**
- **Verificação Visual e de Animação**:
  - Verificar se os elementos aparecem suavemente ao carregar.
  - Checar estados de hover para transições estritamente "suaves".
  - Validar a estética "Futurista Corporativo".
- **Responsividade**:
  - Verificar integridade do layout em 1920x1080 e visualização em Tablet.
