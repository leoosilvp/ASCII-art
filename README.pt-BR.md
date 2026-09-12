<div align="center">

<img src="./assets/svg/logo.svg" width="350" />
</div>

<p align="center">
  <img alt="License" src="https://img.shields.io/badge/Licença-MIT-blue.svg">
  <img alt="PRs Welcome" src="https://img.shields.io/badge/Versão-1.0.8-brightgreen.svg">
</p>

<p align="center">
  <a href="./README.md">Inglês</a> ·
  <a href="./README.pt-BR.md"><strong>Português (BR)</strong></a>
</p>

<p align="center">
  Uma biblioteca de referência completa de caracteres <strong>Unicode/ASCII</strong> para desenho em terminal — bordas, blocos, setas, formas geométricas e símbolos — organizada por categoria e tipo, com exemplos práticos de uso.
</p>

---

## 📑 Índice

- [Sobre](#-sobre)
- [Como usar](#-como-usar)
- [1. Bordas & Caixas](#1-bordas--caixas)
  - [1.1 Bordas simples](#11-bordas-simples)
  - [1.2 Bordas duplas](#12-bordas-duplas)
  - [1.3 Bordas grossas](#13-bordas-grossas)
  - [1.4 Bordas arredondadas](#14-bordas-arredondadas)
  - [1.5 Combinações e junções (T e +)](#15-combinações-e-junções-t-e-)
  - [1.6 Cruzamentos mistos](#16-cruzamentos-mistos)
- [2. Linhas](#2-linhas)
  - [2.1 Linhas retas e tracejadas](#21-linhas-retas-e-tracejadas)
  - [2.2 Diagonais](#22-diagonais)
- [3. Blocos e Preenchimentos](#3-blocos-e-preenchimentos)
- [4. Formas Geométricas](#4-formas-geométricas)
  - [4.1 Quadrados](#41-quadrados)
  - [4.2 Círculos](#42-círculos)
  - [4.3 Losangos](#43-losangos)
  - [4.4 Triângulos](#44-triângulos)
  - [4.5 Espirais e cantos curvos](#45-espirais-e-cantos-curvos)
- [5. Setas](#5-setas)
  - [5.1 Básicas](#51-básicas)
  - [5.2 Duplas](#52-duplas)
  - [5.3 Decorativas](#53-decorativas)
  - [5.4 Curvas e rotação](#54-curvas-e-rotação)
- [6. Símbolos & Ícones](#6-símbolos--ícones)
  - [6.1 Estrelas](#61-estrelas)
  - [6.2 Check / erro / status](#62-check--erro--status)
  - [6.3 Matemática](#63-matemática)
  - [6.4 Diversos e tipografia](#64-diversos-e-tipografia)
  - [6.5 Corações](#65-corações)
  - [6.6 Clima & natureza](#66-clima--natureza)
  - [6.7 Técnicos & alerta](#67-técnicos--alerta)
  - [6.8 Naipes de cartas](#68-naipes-de-cartas)
  - [6.9 Música](#69-música)
  - [6.10 Caixas de seleção e marcadores](#610-caixas-de-seleção-e-marcadores)
  - [6.11 Pontos e marcadores de lista](#611-pontos-e-marcadores-de-lista)
- [7. Divisores & Cabeçalhos Prontos](#7-divisores--cabeçalhos-prontos)
- [8. Conjunto Essencial (Cheat Sheet)](#8-conjunto-essencial-cheat-sheet)
- [9. Aplicação Real: Interfaces de CLI (estilo Claude Code)](#9-aplicação-real-interfaces-de-cli-estilo-claude-code)
  - [9.1 Banner de boas-vindas](#91-banner-de-boas-vindas)
  - [9.2 Caixa de prompt do usuário](#92-caixa-de-prompt-do-usuário)
  - [9.3 Indicador de "pensando" (spinner + streaming)](#93-indicador-de-pensando-spinner--streaming)
  - [9.4 Cartão de chamada de ferramenta (tool call)](#94-cartão-de-chamada-de-ferramenta-tool-call)
  - [9.5 Diff de código (edição de arquivo)](#95-diff-de-código-edição-de-arquivo)
  - [9.6 Plano de execução (checklist de tarefas)](#96-plano-de-execução-checklist-de-tarefas)
  - [9.7 Barra de progresso e status de build](#97-barra-de-progresso-e-status-de-build)
  - [9.8 Rodapé de status (footer)](#98-rodapé-de-status-footer)
  - [9.9 Composição completa (tela de sessão)](#99-composição-completa-tela-de-sessão)
- [Contribuindo](#-contribuindo)
- [Licença](#-licença)

---

## 📖 Sobre

Este repositório organiza **todos os caracteres de desenho** normalmente usados para criar ASCII art, diagramas de terminal, banners e interfaces em modo texto. Em vez de uma lista solta de símbolos, cada categoria traz:

- os **caracteres isolados**, para consulta rápida;
- quando aplicável, um **exemplo de uso prático** (uma caixa, um divisor, uma barra de progresso), mostrando como combiná-los.

## 🚀 Como usar

1. Localize a categoria desejada no índice.
2. Copie o conteúdo do bloco de código correspondente — **nunca copie do texto renderizado**, apenas do bloco `text`, para preservar o alinhamento exato dos caracteres.
3. Cole em um terminal, editor de código, README ou qualquer aplicação que use fonte **monoespaçada**.

> ⚠️ Estes caracteres só se alinham corretamente em fontes monoespaçadas (ex.: `Courier New`, `Consolas`, `Menlo`, `Fira Code`, `JetBrains Mono`). Em fontes proporcionais, o alinhamento se perde.

---

## 1. Bordas & Caixas

Caracteres de desenho de caixa (*box-drawing characters*), usados para criar molduras, tabelas e painéis em modo texto.

### 1.1 Bordas simples

**Caracteres:**
```text
┌ ┐ └ ┘   (cantos)
─ │       (linhas horizontal e vertical)
├ ┤ ┬ ┴ ┼ (junções em T e cruz)
```

**Exemplo — caixa com divisória interna:**
```text
┌─────────────┐
│   TÍTULO    │
├─────────────┤
│  conteúdo   │
└─────────────┘
```

### 1.2 Bordas duplas

**Caracteres:**
```text
╔ ╗ ╚ ╝
═ ║
╠ ╣ ╦ ╩ ╬
```

**Exemplo:**
```text
╔═════════════╗
║   TÍTULO    ║
╠═════════════╣
║  conteúdo   ║
╚═════════════╝
```

### 1.3 Bordas grossas

**Caracteres:**
```text
┏ ┓ ┗ ┛
━ ┃
┣ ┫ ┳ ┻ ╋
```

**Exemplo:**
```text
┏━━━━━━━━━━━━━┓
┃  DESTAQUE   ┃
┣━━━━━━━━━━━━━┫
┃  conteúdo   ┃
┗━━━━━━━━━━━━━┛
```

### 1.4 Bordas arredondadas

**Caracteres:**
```text
╭ ╮ ╰ ╯
```

**Exemplo:**
```text
╭─────────────╮
│   suave     │
╰─────────────╯
```

### 1.5 Combinações e junções (T e +)

Como cada estilo de borda organiza suas junções — útil para saber qual caractere usar ao emendar linhas de um mesmo grupo:

```text
Simples:     ┌ ┬ ┐        Duplas:   ╔ ╦ ╗        Grossas:  ┏ ┳ ┓
             ├ ┼ ┤                  ╠ ╬ ╣                  ┣ ╋ ┫
             └ ┴ ┘                  ╚ ╩ ╝                  ┗ ┻ ┛
```

### 1.6 Cruzamentos mistos

Para quando uma linha grossa cruza uma fina, ou vice-versa (semi-junções):

```text
┼ ┽ ┾ ┿
╀ ╁ ╂ ╃ ╄ ╅ ╆ ╇
╈ ╉ ╊ ╋
```

---

## 2. Linhas

### 2.1 Linhas retas e tracejadas

```text
Sólida:      ─   │
Grossa:      ━   ┃
Tracejada:   ┄ ┅ (2 traços)   ┈ ┉ (4 traços)
Pontilhada:  ┆ ┇   ┊ ┋
Meia-linha:  ╴ ╶ ╸ ╺   (horizontais parciais)
             ╵ ╷ ╹ ╻   (verticais parciais)
```

### 2.2 Diagonais

```text
╱  (barra para cima)
╲  (barra para baixo)
╳  (cruzamento diagonal)
／ ＼  (versões largas, full-width)
⟋ ⟍   (versões matemáticas)
```

---

## 3. Blocos e Preenchimentos

Usados para barras de progresso, gráficos de intensidade e sombreamento.

**Blocos verticais parciais (largura variável):**
```text
█ ▉ ▊ ▋ ▌ ▍ ▎ ▏
```

**Blocos horizontais parciais (altura variável):**
```text
▁ ▂ ▃ ▄ ▅ ▆ ▇ █
```

**Meios-blocos e complementos:**
```text
▀ (metade superior)   ▄ (metade inferior)
▐ (metade direita)    ▔ (traço superior)
```

**Densidade de sombreamento (do mais claro ao mais denso):**
```text
░  ▒  ▓  █
```

**Exemplo — barra de progresso:**
```text
[██████████▓▓▓▓░░░░░░] 62%
```

---

## 4. Formas Geométricas

### 4.1 Quadrados

```text
■ □       (preenchido / vazio)
▪ ▫       (pequenos)
◼ ◻       (grandes)
▢         (contorno arredondado)
▰ ▱       (estilo indicador)
▣ ▤ ▥ ▦ ▧ ▨ ▩   (com padrões internos)
```

### 4.2 Círculos

```text
● ○           (preenchido / vazio)
◉ ◎           (com anel)
◌ ◍           (pontilhado / meio-preenchido)
◯             (grande, vazio)
◐ ◑ ◒ ◓       (quadrantes preenchidos)
◔ ◕           (fatias preenchidas)
◖ ◗           (metades esquerda/direita)
```

### 4.3 Losangos

```text
◆ ◇   (preenchido / vazio)
◈     (com contorno interno)
◊     (pequeno, vazio)
⬖ ⬗ ⬘ ⬙   (meio-losangos direcionais)
```

### 4.4 Triângulos

```text
▲ △   (para cima)
▼ ▽   (para baixo)
◀ ◁   (para esquerda)
▶ ▷   (para direita)
◢ ◣ ◤ ◥   (triângulos de canto)
```

### 4.5 Espirais e cantos curvos

```text
◜ ◝ ◞ ◟   (quartos de círculo, cantos)
◠ ◡       (arcos superior/inferior)
◩ ◪ ◫ ◬   (quadrados com corte diagonal)
```

---

## 5. Setas

### 5.1 Básicas

```text
← ↑ → ↓
↔ ↕
↖ ↗ ↘ ↙
```

### 5.2 Duplas

```text
⇐ ⇑ ⇒ ⇓
⇔ ⇕
⇖ ⇗ ⇘ ⇙
```

### 5.3 Decorativas

```text
➔ ➜ ➝ ➞ ➟
➠ ➢ ➣ ➤ ➥
➦ ➧ ➨ ➩ ➪
➫ ➬ ➭ ➮ ➯
➱ ➲ ➳ ➵ ➸
```

### 5.4 Curvas e rotação

```text
⟵ ⟶ ⟷     (setas longas)
⟸ ⟹ ⟺     (setas longas duplas)
⤴ ⤵         (curva para cima / para baixo)
↩ ↪         (retorno esquerda / direita)
↶ ↷         (curva aberta)
↺ ↻         (rotação anti-horária / horária)
```

---

## 6. Símbolos & Ícones

### 6.1 Estrelas

```text
★ ☆   (preenchida / vazia)
✦ ✧   (diamante)
✩ ✪ ✫ ✬ ✭ ✮ ✯ ✰   (variações decorativas)
⋆ ⭑ ⭒
```

### 6.2 Check / erro / status

```text
✓ ✔   (confirmado)
☑ ☒   (caixa marcada / com X)
✕ ✖ ✗ ✘   (variações de X)
❌ ⭕   (emoji-símbolo de erro / círculo)
```

### 6.3 Matemática

```text
+ − × ÷        (operadores básicos)
± ∓            (mais/menos)
= ≠ ≈ ≃ ≅      (igualdade e aproximação)
< > ≤ ≥ ≪ ≫    (comparação)
∞              (infinito)
√ ∛ ∜          (raízes)
∑ ∏            (somatório / produtório)
∫ ∬ ∭          (integrais)
∂ ∆ ∇          (derivadas / operadores)
∝ ∴ ∵          (proporcional / logo / porque)
```

### 6.4 Diversos e tipografia

```text
§ ¶ † ‡    (seção, parágrafo, obelisco)
© ® ™      (direitos autorais, marca)
° ℃ ℉      (grau, celsius, fahrenheit)
№ ※ ⁂ ⁕ ⁑ ⁙   (numeral, referência, asterismo)
```

### 6.5 Corações

```text
♥ ♡   (preenchido / vazio)
❤ ❣ ❥   (variações sólidas)
ღ       (estilizado)
```

### 6.6 Clima & natureza

```text
☀ ☼   (sol)
☁     (nuvem)
☂ ☔   (guarda-chuva / chuva)
☃ ❄   (boneco de neve / floco)
☾ ☽   (lua)
☄ ⚡   (cometa / raio)
```

### 6.7 Técnicos & alerta

```text
⚙ ⚒ ⚔   (engrenagem, ferramentas, espadas)
⚓        (âncora)
☢ ☣      (radioativo / biológico)
⚠ ⛔      (atenção / proibido)
♻        (reciclagem)
```

### 6.8 Naipes de cartas

```text
♠ ♤   (espadas: preenchido / vazio)
♥ ♡   (copas)
♦ ♢   (ouros)
♣ ♧   (paus)
```

### 6.9 Música

```text
♪ ♫ ♩ ♬   (notas)
♭ ♮ ♯     (bemol, bequadro, sustenido)
𝄞          (clave de sol)
```

### 6.10 Caixas de seleção e marcadores

```text
☐ ☑ ☒   (vazia / marcada / com X)
□ ■     (vazio / preenchido)
▢ ▣     (com contorno / com padrão)
◻ ◼     (grandes)
○ ●     (círculo vazio / preenchido)
```

### 6.11 Pontos e marcadores de lista

```text
· • ‧       (pontos simples)
‣ ⁃         (marcador de item)
⁌ ⁍         (marcadores ornamentais)
⁎ ⁕ ⁑ ⁂ ※   (asteriscos e referências)
```

---

## 7. Divisores & Cabeçalhos Prontos

Combinações prontas para separar seções em documentos de texto puro.

**Linha simples:**
```text
────────────────────────────────────────
```

**Linha dupla:**
```text
════════════════════════════════════════
```

**Onda:**
```text
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```

**Cabeçalho simples:**
```text
┌──────────────────────────────┐
│           TÍTULO AQUI        │
└──────────────────────────────┘
```

**Cabeçalho duplo:**
```text
╔══════════════════════════════╗
║           SEÇÃO              ║
╚══════════════════════════════╝
```

**Cabeçalho grosso (destaque):**
```text
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃           DESTAQUE           ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛
```

**Cabeçalho arredondado (nota/aviso suave):**
```text
╭──────────────────────────────╮
│             NOTA             │
╰──────────────────────────────╯
```

---

## 8. Conjunto Essencial (Cheat Sheet)

Os caracteres mais usados na prática para montar caixas, medidores e diagramas rapidamente, reunidos em um único bloco de consulta:

```text
█ ▓ ▒ ░       blocos de preenchimento
▀ ▄ ▌ ▐       meios-blocos
┌ ┐ └ ┘ ─ │   bordas simples
├ ┤ ┬ ┴ ┼     junções simples
╔ ╗ ╚ ╝ ═ ║   bordas duplas
╠ ╣ ╦ ╩ ╬     junções duplas
┏ ┓ ┗ ┛ ━ ┃   bordas grossas
┣ ┫ ┳ ┻ ╋     junções grossas
╭ ╮ ╰ ╯       cantos arredondados
● ○ ■ □ ◆ ◇   formas básicas
▲ △ ▼ ▽       triângulos
★ ☆           estrelas
← ↑ → ↓ ↖ ↗ ↘ ↙   setas
```

---

## 9. Aplicação Real: Interfaces de CLI (estilo Claude Code)

Esta seção mostra como os caracteres das seções anteriores se combinam para construir **interfaces reais de linha de comando** — o tipo de UI usada por agentes de IA em terminal (ex.: Claude Code), ferramentas de build e assistentes interativos. Cada exemplo é um componente independente que pode ser copiado e adaptado.

> 💡 **Princípio de design:** interfaces de CLI profissionais usam bordas arredondadas (`╭ ╮ ╰ ╯`) para caixas de entrada/conteúdo, bordas simples para painéis secundários, e reservam cor semântica (verde/vermelho/amarelo) — aqui representada por símbolos (`✓ ✗ ⚠`) — para status. Evite bordas grossas ou duplas em excesso: elas competem visualmente com o conteúdo.

### 9.1 Banner de boas-vindas

Tela inicial exibida ao abrir a ferramenta — nome do produto, versão e contexto do diretório atual.

```text
╭──────────────────────────────────────────────────────────────╮
│                                                              │
│   ██████╗ ██╗      ██╗                                       │
│  ██╔════╝ ██║      ██║      Assistente de linha de comando   │
│  ██║      ██║      ██║      v2.4.1                           │
│  ╚██████╗ ███████╗ ██║      ~/projetos/meu-app               │
│   ╚═════╝ ╚══════╝ ╚═╝                                       │
│                                                              │
╰──────────────────────────────────────────────────────────────╯

  Digite sua tarefa ou /help para ver os comandos disponíveis.
```

### 9.2 Caixa de prompt do usuário

O campo de entrada é o elemento mais recorrente da interface — sempre com borda arredondada e um indicador de foco.

```text
╭─ Você ────────────────────────────────────────────────────╮
│ > refatore o módulo de autenticação para usar JWT         │
╰──────────────────────────────────────────────────────── ⏎ ╯
```

**Variante com contexto anexado (arquivo/imagem carregados):**
```text
╭─ Você ────────────────────────────────────────────────────╮
│ 📎 auth.controller.ts                                     │
│ > por que esse endpoint está retornando 401?              │
╰──────────────────────────────────────────────────────── ⏎ ╯
```

### 9.3 Indicador de "pensando" (spinner + streaming)

Estado transitório enquanto o modelo processa — combina um spinner animável com uma linha de status discreta.

```text
⠋ Analisando a estrutura do projeto...
```

**Ciclo de frames do spinner (renderize um por vez, em sequência, a cada ~80ms):**
```text
⠋ ⠙ ⠹ ⠸ ⠼ ⠴ ⠦ ⠧ ⠇ ⠏
```

**Com tempo decorrido e opção de interrupção:**
```text
⠴ Gerando resposta...  (12s · esc para interromper)
```

### 9.4 Cartão de chamada de ferramenta (tool call)

Cada ação do agente (leitura de arquivo, execução de comando, busca) é exibida como um bloco compacto, com estado inicial, em progresso e concluído.

**Em execução:**
```text
● Executando bash
  └─ npm run test -- --watch=false
```

**Concluído com sucesso:**
```text
✓ Executando bash
  └─ npm run test -- --watch=false
  └─ 47 passed, 0 failed (3.2s)
```

**Falha:**
```text
✗ Executando bash
  └─ npm run build
  └─ Erro: Cannot find module 'zod' (linha 12)
```

**Leitura de arquivo:**
```text
✓ Lendo arquivo
  └─ src/services/auth.service.ts (128 linhas)
```

### 9.5 Diff de código (edição de arquivo)

Ao propor mudanças, o agente exibe um diff compacto — linha removida marcada com `−`, linha adicionada com `+`, contexto sem prefixo.

```text
✓ Editado src/services/auth.service.ts

   10   export function login(user: User) {
   11 −   const token = generateLegacyToken(user);
   11 +   const token = jwt.sign({ sub: user.id }, SECRET, { expiresIn: "1h" });
   12     return token;
   13   }

  1 adição · 1 remoção
```

### 9.6 Plano de execução (checklist de tarefas)

Quando o agente decompõe uma tarefa complexa em etapas, exibindo progresso incremental.

```text
╭─ Plano ─────────────────────────────────────────────────╮
│ ✓ Ler arquivos de configuração existentes               │
│ ✓ Instalar dependência jsonwebtoken                     │
│ ● Refatorar auth.service.ts para emitir JWT             │
│ ○ Atualizar middleware de verificação de token          │
│ ○ Rodar suíte de testes                                 │
╰─────────────────────────────────────────────────────────╯
```

*Legenda: `✓` concluído · `●` em andamento · `○` pendente*

### 9.7 Barra de progresso e status de build

```text
Compilando projeto...
[████████████████████████░░░░░░░░░░] 68%  ·  17/25 arquivos
```

**Painel de status com múltiplas métricas:**
```text
┌─ Status da sessão ─────────────────────────────────────┐
│ Tokens usados     ▓▓▓▓▓▓▓▓▓░░░░░░░░░░░  42%            │
│ Arquivos tocados  4                                    │
│ Testes            ✓ 47 passando                        │
│ Tempo de sessão   00:04:12                             │
└────────────────────────────────────────────────────────┘
```

### 9.8 Rodapé de status (footer)

Linha fixa na parte inferior do terminal, com atalhos e contexto — comum em CLIs interativas.

```text
────────────────────────────────────────────────────────────
 ⏎ enviar   ⇧⏎ nova linha   ⌃C interromper   /help ajuda
```

### 9.9 Composição completa (tela de sessão)

Exemplo combinando os componentes anteriores em uma tela única, tal como apareceria durante uma sessão real:

```text
╭──────────────────────────────────────────────────────────╮
│  CLI Agent  v2.4.1 · ~/projetos/meu-app                  │
╰──────────────────────────────────────────────────────────╯

╭─ Você ────────────────────────────────────────────────────╮
│ > refatore o módulo de autenticação para usar JWT         │
╰───────────────────────────────────────────────────────────╯

● Lendo arquivo
  └─ src/services/auth.service.ts

✓ Editado src/services/auth.service.ts
   11 −   const token = generateLegacyToken(user);
   11 +   const token = jwt.sign({ sub: user.id }, SECRET, { expiresIn: "1h" });

  1 adição · 1 remoção

╭─ Plano ─────────────────────────────────────────────────╮
│ ✓ Refatorar auth.service.ts para emitir JWT             │
│ ● Atualizar middleware de verificação de token          │
│ ○ Rodar suíte de testes                                 │
╰─────────────────────────────────────────────────────────╯

⠴ Atualizando auth.middleware.ts... (4s · esc para interromper)

────────────────────────────────────────────────────────────
 ⏎ enviar   ⇧⏎ nova linha   ⌃C interromper   /help ajuda
```

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Para adicionar conteúdo:

1. Faça um fork deste repositório.
2. Adicione o conjunto de caracteres na categoria correspondente (ou proponha uma nova seção, se necessário).
3. Sempre inclua, quando fizer sentido, um pequeno **exemplo de uso** — não apenas a lista de caracteres.
4. Use blocos de código com a linguagem `text` para preservar o alinhamento.
5. Atualize o [Índice](#-índice) ao criar uma nova seção ou subseção.
6. Ao alterar um arquivo de idioma, atualize o outro também (`README.md` ↔ `README.pt-BR.md`) para manter os dois sincronizados.
7. Abra um Pull Request descrevendo o que foi adicionado.

### Diretrizes de estilo
- Agrupe caracteres por família (bordas, setas, formas etc.) em vez de listas soltas e sem contexto.
- Prefira exemplos com no máximo ~40 colunas de largura.
- Numere as seções e subseções seguindo o padrão já existente (`1.`, `1.1`, etc.).
- Evite conteúdo protegido por direitos autorais (emojis de marcas, personagens, etc.).

---

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE) — sinta-se livre para usar, copiar e distribuir.