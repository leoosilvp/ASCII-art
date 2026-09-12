<div align="center">

<img src="./assets/svg/logo.svg" width="350" />
</div>

<p align="center">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-blue.svg">
  <img alt="PRs Welcome" src="https://img.shields.io/badge/Version-1.0.8-brightgreen.svg">
</p>

<p align="center">
  <a href="./README.md"><strong>English</strong></a> ·
  <a href="./README.pt-BR.md">Português (BR)</a>
</p>

<p align="center">
  A complete reference library of <strong>Unicode/ASCII</strong> characters for terminal drawing — borders, blocks, arrows, geometric shapes, and symbols — organized by category and type, with practical usage examples.
</p>

---

## 📑 Table of Contents

- [About](#-about)
- [How to use](#-how-to-use)
- [1. Borders & Boxes](#1-borders--boxes)
  - [1.1 Simple borders](#11-simple-borders)
  - [1.2 Double borders](#12-double-borders)
  - [1.3 Heavy borders](#13-heavy-borders)
  - [1.4 Rounded borders](#14-rounded-borders)
  - [1.5 Combinations and junctions (T and +)](#15-combinations-and-junctions-t-and-)
  - [1.6 Mixed crossings](#16-mixed-crossings)
- [2. Lines](#2-lines)
  - [2.1 Straight and dashed lines](#21-straight-and-dashed-lines)
  - [2.2 Diagonals](#22-diagonals)
- [3. Blocks and Fills](#3-blocks-and-fills)
- [4. Geometric Shapes](#4-geometric-shapes)
  - [4.1 Squares](#41-squares)
  - [4.2 Circles](#42-circles)
  - [4.3 Diamonds](#43-diamonds)
  - [4.4 Triangles](#44-triangles)
  - [4.5 Spirals and curved corners](#45-spirals-and-curved-corners)
- [5. Arrows](#5-arrows)
  - [5.1 Basic](#51-basic)
  - [5.2 Double](#52-double)
  - [5.3 Decorative](#53-decorative)
  - [5.4 Curved and rotation](#54-curved-and-rotation)
- [6. Symbols & Icons](#6-symbols--icons)
  - [6.1 Stars](#61-stars)
  - [6.2 Check / error / status](#62-check--error--status)
  - [6.3 Mathematics](#63-mathematics)
  - [6.4 Miscellaneous and typography](#64-miscellaneous-and-typography)
  - [6.5 Hearts](#65-hearts)
  - [6.6 Weather & nature](#66-weather--nature)
  - [6.7 Technical & warning](#67-technical--warning)
  - [6.8 Card suits](#68-card-suits)
  - [6.9 Music](#69-music)
  - [6.10 Checkboxes and markers](#610-checkboxes-and-markers)
  - [6.11 Bullets and list markers](#611-bullets-and-list-markers)
- [7. Dividers & Ready-Made Headers](#7-dividers--ready-made-headers)
- [8. Essential Set (Cheat Sheet)](#8-essential-set-cheat-sheet)
- [9. Real-World Use: CLI Interfaces (Claude Code style)](#9-real-world-use-cli-interfaces-claude-code-style)
  - [9.1 Welcome banner](#91-welcome-banner)
  - [9.2 User prompt box](#92-user-prompt-box)
  - [9.3 "Thinking" indicator (spinner + streaming)](#93-thinking-indicator-spinner--streaming)
  - [9.4 Tool call card](#94-tool-call-card)
  - [9.5 Code diff (file edit)](#95-code-diff-file-edit)
  - [9.6 Execution plan (task checklist)](#96-execution-plan-task-checklist)
  - [9.7 Progress bar and build status](#97-progress-bar-and-build-status)
  - [9.8 Status footer](#98-status-footer)
  - [9.9 Full composition (session screen)](#99-full-composition-session-screen)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📖 About

This repository organizes **all the drawing characters** commonly used to build ASCII art, terminal diagrams, banners, and text-mode interfaces. Instead of a loose list of symbols, each category includes:

- the **individual characters**, for quick reference;
- where applicable, a **practical usage example** (a box, a divider, a progress bar) showing how to combine them.

## 🚀 How to use

1. Find the category you need in the table of contents.
2. Copy the content from the corresponding code block — **never copy from the rendered text**, only from the `text` block, to preserve exact character alignment.
3. Paste it into a terminal, code editor, README, or any application using a **monospace font**.

> ⚠️ These characters only align correctly in monospace fonts (e.g. `Courier New`, `Consolas`, `Menlo`, `Fira Code`, `JetBrains Mono`). In proportional fonts, alignment is lost.

---

## 1. Borders & Boxes

Box-drawing characters, used to create frames, tables, and panels in text mode.

### 1.1 Simple borders

**Characters:**
```text
┌ ┐ └ ┘   (corners)
─ │       (horizontal and vertical lines)
├ ┤ ┬ ┴ ┼ (T-junctions and cross)
```

**Example — box with internal divider:**
```text
┌─────────────┐
│    TITLE    │
├─────────────┤
│   content   │
└─────────────┘
```

### 1.2 Double borders

**Characters:**
```text
╔ ╗ ╚ ╝
═ ║
╠ ╣ ╦ ╩ ╬
```

**Example:**
```text
╔═════════════╗
║    TITLE    ║
╠═════════════╣
║   content   ║
╚═════════════╝
```

### 1.3 Heavy borders

**Characters:**
```text
┏ ┓ ┗ ┛
━ ┃
┣ ┫ ┳ ┻ ╋
```

**Example:**
```text
┏━━━━━━━━━━━━━┓
┃  HIGHLIGHT  ┃
┣━━━━━━━━━━━━━┫
┃   content   ┃
┗━━━━━━━━━━━━━┛
```

### 1.4 Rounded borders

**Characters:**
```text
╭ ╮ ╰ ╯
```

**Example:**
```text
╭─────────────╮
│    smooth   │
╰─────────────╯
```

### 1.5 Combinations and junctions (T and +)

How each border style organizes its junctions — useful for knowing which character to use when joining lines from the same family:

```text
Simple:      ┌ ┬ ┐        Double:   ╔ ╦ ╗        Heavy:    ┏ ┳ ┓
             ├ ┼ ┤                  ╠ ╬ ╣                  ┣ ╋ ┫
             └ ┴ ┘                  ╚ ╩ ╝                  ┗ ┻ ┛
```

### 1.6 Mixed crossings

For when a heavy line crosses a thin one, or vice versa (semi-junctions):

```text
┼ ┽ ┾ ┿
╀ ╁ ╂ ╃ ╄ ╅ ╆ ╇
╈ ╉ ╊ ╋
```

---

## 2. Lines

### 2.1 Straight and dashed lines

```text
Solid:        ─   │
Heavy:        ━   ┃
Dashed:       ┄ ┅ (2 dashes)   ┈ ┉ (4 dashes)
Dotted:       ┆ ┇   ┊ ┋
Half-line:    ╴ ╶ ╸ ╺   (partial horizontals)
              ╵ ╷ ╹ ╻   (partial verticals)
```

### 2.2 Diagonals

```text
╱  (upward slash)
╲  (downward slash)
╳  (diagonal cross)
／ ＼  (full-width variants)
⟋ ⟍   (mathematical variants)
```

---

## 3. Blocks and Fills

Used for progress bars, intensity charts, and shading.

**Partial vertical blocks (variable width):**
```text
█ ▉ ▊ ▋ ▌ ▍ ▎ ▏
```

**Partial horizontal blocks (variable height):**
```text
▁ ▂ ▃ ▄ ▅ ▆ ▇ █
```

**Half-blocks and complements:**
```text
▀ (upper half)   ▄ (lower half)
▐ (right half)   ▔ (upper line)
```

**Shading density (lightest to densest):**
```text
░  ▒  ▓  █
```

**Example — progress bar:**
```text
[██████████▓▓▓▓░░░░░░] 62%
```

---

## 4. Geometric Shapes

### 4.1 Squares

```text
■ □       (filled / empty)
▪ ▫       (small)
◼ ◻       (large)
▢         (rounded outline)
▰ ▱       (indicator style)
▣ ▤ ▥ ▦ ▧ ▨ ▩   (with internal patterns)
```

### 4.2 Circles

```text
● ○           (filled / empty)
◉ ◎           (with ring)
◌ ◍           (dotted / half-filled)
◯             (large, empty)
◐ ◑ ◒ ◓       (filled quadrants)
◔ ◕           (filled slices)
◖ ◗           (left/right halves)
```

### 4.3 Diamonds

```text
◆ ◇   (filled / empty)
◈     (with inner outline)
◊     (small, empty)
⬖ ⬗ ⬘ ⬙   (directional half-diamonds)
```

### 4.4 Triangles

```text
▲ △   (upward)
▼ ▽   (downward)
◀ ◁   (leftward)
▶ ▷   (rightward)
◢ ◣ ◤ ◥   (corner triangles)
```

### 4.5 Spirals and curved corners

```text
◜ ◝ ◞ ◟   (quarter circles, corners)
◠ ◡       (upper/lower arcs)
◩ ◪ ◫ ◬   (squares with diagonal cut)
```

---

## 5. Arrows

### 5.1 Basic

```text
← ↑ → ↓
↔ ↕
↖ ↗ ↘ ↙
```

### 5.2 Double

```text
⇐ ⇑ ⇒ ⇓
⇔ ⇕
⇖ ⇗ ⇘ ⇙
```

### 5.3 Decorative

```text
➔ ➜ ➝ ➞ ➟
➠ ➢ ➣ ➤ ➥
➦ ➧ ➨ ➩ ➪
➫ ➬ ➭ ➮ ➯
➱ ➲ ➳ ➵ ➸
```

### 5.4 Curved and rotation

```text
⟵ ⟶ ⟷     (long arrows)
⟸ ⟹ ⟺     (long double arrows)
⤴ ⤵         (curve up / curve down)
↩ ↪         (return left / right)
↶ ↷         (open curve)
↺ ↻         (counter-clockwise / clockwise rotation)
```

---

## 6. Symbols & Icons

### 6.1 Stars

```text
★ ☆   (filled / empty)
✦ ✧   (diamond)
✩ ✪ ✫ ✬ ✭ ✮ ✯ ✰   (decorative variants)
⋆ ⭑ ⭒
```

### 6.2 Check / error / status

```text
✓ ✔   (confirmed)
☑ ☒   (checked box / with X)
✕ ✖ ✗ ✘   (X variants)
❌ ⭕   (error emoji-symbol / circle)
```

### 6.3 Mathematics

```text
+ − × ÷        (basic operators)
± ∓            (plus/minus)
= ≠ ≈ ≃ ≅      (equality and approximation)
< > ≤ ≥ ≪ ≫    (comparison)
∞              (infinity)
√ ∛ ∜          (roots)
∑ ∏            (summation / product)
∫ ∬ ∭          (integrals)
∂ ∆ ∇          (derivatives / operators)
∝ ∴ ∵          (proportional / therefore / because)
```

### 6.4 Miscellaneous and typography

```text
§ ¶ † ‡    (section, paragraph, dagger)
© ® ™      (copyright, trademark)
° ℃ ℉      (degree, celsius, fahrenheit)
№ ※ ⁂ ⁕ ⁑ ⁙   (numero, reference mark, asterism)
```

### 6.5 Hearts

```text
♥ ♡   (filled / empty)
❤ ❣ ❥   (solid variants)
ღ       (stylized)
```

### 6.6 Weather & nature

```text
☀ ☼   (sun)
☁     (cloud)
☂ ☔   (umbrella / rain)
☃ ❄   (snowman / snowflake)
☾ ☽   (moon)
☄ ⚡   (comet / lightning)
```

### 6.7 Technical & warning

```text
⚙ ⚒ ⚔   (gear, tools, swords)
⚓        (anchor)
☢ ☣      (radioactive / biohazard)
⚠ ⛔      (warning / prohibited)
♻        (recycling)
```

### 6.8 Card suits

```text
♠ ♤   (spades: filled / empty)
♥ ♡   (hearts)
♦ ♢   (diamonds)
♣ ♧   (clubs)
```

### 6.9 Music

```text
♪ ♫ ♩ ♬   (notes)
♭ ♮ ♯     (flat, natural, sharp)
𝄞          (treble clef)
```

### 6.10 Checkboxes and markers

```text
☐ ☑ ☒   (empty / checked / with X)
□ ■     (empty / filled)
▢ ▣     (outlined / patterned)
◻ ◼     (large)
○ ●     (empty / filled circle)
```

### 6.11 Bullets and list markers

```text
· • ‧       (simple dots)
‣ ⁃         (item marker)
⁌ ⁍         (ornamental markers)
⁎ ⁕ ⁑ ⁂ ※   (asterisks and reference marks)
```

---

## 7. Dividers & Ready-Made Headers

Ready-to-use combinations for separating sections in plain-text documents.

**Simple line:**
```text
────────────────────────────────────────
```

**Double line:**
```text
════════════════════════════════════════
```

**Wave:**
```text
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```

**Simple header:**
```text
┌──────────────────────────────┐
│          TITLE HERE          │
└──────────────────────────────┘
```

**Double header:**
```text
╔══════════════════════════════╗
║           SECTION            ║
╚══════════════════════════════╝
```

**Heavy header (highlight):**
```text
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃           HIGHLIGHT          ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛
```

**Rounded header (note/soft warning):**
```text
╭──────────────────────────────╮
│              NOTE            │
╰──────────────────────────────╯
```

---

## 8. Essential Set (Cheat Sheet)

The most commonly used characters for quickly building boxes, gauges, and diagrams, gathered in a single reference block:

```text
█ ▓ ▒ ░       fill blocks
▀ ▄ ▌ ▐       half-blocks
┌ ┐ └ ┘ ─ │   simple borders
├ ┤ ┬ ┴ ┼     simple junctions
╔ ╗ ╚ ╝ ═ ║   double borders
╠ ╣ ╦ ╩ ╬     double junctions
┏ ┓ ┗ ┛ ━ ┃   heavy borders
┣ ┫ ┳ ┻ ╋     heavy junctions
╭ ╮ ╰ ╯       rounded corners
● ○ ■ □ ◆ ◇   basic shapes
▲ △ ▼ ▽       triangles
★ ☆           stars
← ↑ → ↓ ↖ ↗ ↘ ↙   arrows
```

---

## 9. Real-World Use: CLI Interfaces (Claude Code style)

This section shows how the characters from the previous sections combine to build **real command-line interfaces** — the kind of UI used by terminal-based AI agents (e.g. Claude Code), build tools, and interactive assistants. Each example is a standalone component that can be copied and adapted.

> 💡 **Design principle:** professional CLI interfaces use rounded borders (`╭ ╮ ╰ ╯`) for input/content boxes, simple borders for secondary panels, and reserve semantic color (green/red/yellow) — represented here by symbols (`✓ ✗ ⚠`) — for status. Avoid overusing heavy or double borders: they visually compete with the content.

### 9.1 Welcome banner

Initial screen shown when opening the tool — product name, version, and current directory context.

```text
╭──────────────────────────────────────────────────────────╮
│                                                          │
│   ██████╗ ██╗      ██╗                                   │
│  ██╔════╝ ██║      ██║      Command-line assistant       │
│  ██║      ██║      ██║      v2.4.1                       │
│  ╚██████╗ ███████╗ ██║      ~/projects/my-app            │
│   ╚═════╝ ╚══════╝ ╚═╝                                   │
│                                                          │
╰──────────────────────────────────────────────────────────╯

  Type your task or /help to see available commands.
```

### 9.2 User prompt box

The input field is the most recurring element of the interface — always with a rounded border and a focus indicator.

```text
╭─ You ──────────────────────────────────────────────────────╮
│ > refactor the auth module to use JWT                      │
╰──────────────────────────────────────────────────────── ⏎ ╯
```

**Variant with attached context (loaded file/image):**
```text
╭─ You ──────────────────────────────────────────────────────╮
│ 📎 auth.controller.ts                                      │
│ > why is this endpoint returning 401?                      │
╰──────────────────────────────────────────────────────── ⏎ ╯
```

### 9.3 "Thinking" indicator (spinner + streaming)

Transient state while the model is processing — combines an animatable spinner with a discreet status line.

```text
⠋ Analyzing project structure...
```

**Spinner frame cycle (render one at a time, in sequence, every ~80ms):**
```text
⠋ ⠙ ⠹ ⠸ ⠼ ⠴ ⠦ ⠧ ⠇ ⠏
```

**With elapsed time and interrupt option:**
```text
⠴ Generating response...  (12s · esc to interrupt)
```

### 9.4 Tool call card

Each agent action (file read, command execution, search) is shown as a compact block, with pending, in-progress, and completed states.

**Running:**
```text
● Running bash
  └─ npm run test -- --watch=false
```

**Completed successfully:**
```text
✓ Running bash
  └─ npm run test -- --watch=false
  └─ 47 passed, 0 failed (3.2s)
```

**Failed:**
```text
✗ Running bash
  └─ npm run build
  └─ Error: Cannot find module 'zod' (line 12)
```

**File read:**
```text
✓ Reading file
  └─ src/services/auth.service.ts (128 lines)
```

### 9.5 Code diff (file edit)

When proposing changes, the agent shows a compact diff — removed line marked with `−`, added line with `+`, context lines with no prefix.

```text
✓ Edited src/services/auth.service.ts

   10   export function login(user: User) {
   11 −   const token = generateLegacyToken(user);
   11 +   const token = jwt.sign({ sub: user.id }, SECRET, { expiresIn: "1h" });
   12     return token;
   13   }

  1 addition · 1 removal
```

### 9.6 Execution plan (task checklist)

When the agent breaks a complex task into steps, showing incremental progress.

```text
╭─ Plan ──────────────────────────────────────────────────╮
│ ✓ Read existing configuration files                     │
│ ✓ Install jsonwebtoken dependency                       │
│ ● Refactor auth.service.ts to issue JWTs                │
│ ○ Update token verification middleware                  │
│ ○ Run test suite                                        │
╰─────────────────────────────────────────────────────────╯
```

*Legend: `✓` done · `●` in progress · `○` pending*

### 9.7 Progress bar and build status

```text
Building project...
[████████████████████████░░░░░░░░░░] 68%  ·  17/25 files
```

**Status panel with multiple metrics:**
```text
┌─ Session status ───────────────────────────────────────┐
│ Tokens used       ▓▓▓▓▓▓▓▓▓░░░░░░░░░░░  42%            │
│ Files touched     4                                    │
│ Tests             ✓ 47 passing                         │
│ Session time      00:04:12                             │
└────────────────────────────────────────────────────────┘
```

### 9.8 Status footer

Fixed line at the bottom of the terminal, with shortcuts and context — common in interactive CLIs.

```text
────────────────────────────────────────────────────────────
 ⏎ send   ⇧⏎ new line   ⌃C interrupt   /help help
```

### 9.9 Full composition (session screen)

Example combining the previous components into a single screen, as it would appear during a real session:

```text
╭──────────────────────────────────────────────────────────╮
│  CLI Agent  v2.4.1 · ~/projects/my-app                   │
╰──────────────────────────────────────────────────────────╯

╭─ You ──────────────────────────────────────────────────────╮
│ > refactor the auth module to use JWT                      │
╰────────────────────────────────────────────────────────────╯

● Reading file
  └─ src/services/auth.service.ts

✓ Edited src/services/auth.service.ts
   11 −   const token = generateLegacyToken(user);
   11 +   const token = jwt.sign({ sub: user.id }, SECRET, { expiresIn: "1h" });

  1 addition · 1 removal

╭─ Plan ──────────────────────────────────────────────────╮
│ ✓ Refactor auth.service.ts to issue JWTs                │
│ ● Update token verification middleware                  │
│ ○ Run test suite                                        │
╰─────────────────────────────────────────────────────────╯

⠴ Updating auth.middleware.ts... (4s · esc to interrupt)

────────────────────────────────────────────────────────────
 ⏎ send   ⇧⏎ new line   ⌃C interrupt   /help help
```

---

## 🤝 Contributing

Contributions are welcome! To add content:

1. Fork this repository.
2. Add the character set to the corresponding category (or propose a new section, if needed).
3. Whenever it makes sense, include a small **usage example** — not just the list of characters.
4. Use code blocks with the `text` language to preserve alignment.
5. Update the [Table of Contents](#-table-of-contents) when creating a new section or subsection.
6. If you change one language file, update the other (`README.md` ↔ `README.pt-BR.md`) so both stay in sync.
7. Open a Pull Request describing what was added.

### Style guidelines
- Group characters by family (borders, arrows, shapes, etc.) rather than loose, context-free lists.
- Prefer examples no wider than ~40 columns.
- Number sections and subsections following the existing pattern (`1.`, `1.1`, etc.).
- Avoid copyrighted content (brand emojis, characters, etc.).

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — feel free to use, copy, and distribute it.