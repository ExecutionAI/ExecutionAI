# ExecutionAI — Project Context & Dev Rules

## What We're Building

A **personal brand / agency landing page** for **ExecutionAI** — shared by Omar (lead generator) with high-profile business owners in Mexico as a first touchpoint. The page must be hyper-professional, inspire confidence, and convert curiosity into a conversation with Omar.

**Language:** Everything client-facing is in **Spanish**. Code and internal docs in English.

---

## Brand

| Field | Value |
|-------|-------|
| **Name** | ExecutionAI |
| **Positioning** | Software factory with 15+ years in technology, 7+ years leading global innovation projects at Uber. |
| **Pitch** | Incorporamos automatización e inteligencia artificial a los procesos internos de tu empresa — o directamente en la experiencia de tus clientes. |
| **Tone** | Hyper-professional, confident, sophisticated. No startup fluff. No generic AI aesthetics. |
| **Face** | Agency — no person. Brand identity only. |

---

## Target Audience

High-profile business owners in Mexico (Omar's leasing clients):
- Logistics companies
- Medical professionals / clinics
- General empresarios

**Pain points we address:**
1. Pierden dinero en procesos manuales y operación sin visibilidad en tiempo real
2. No tienen visibilidad del negocio en tiempo real
3. No están aprovechando los modelos de IA para generar contenido personalizado o automatizar interacciones con clientes

---

## Services (What ExecutionAI Does)

Fabrica de software de alta especializacion — adaptable a cualquier industria:

1. **Automatizacion de procesos internos** — eliminar trabajo manual, conectar sistemas, flujos automaticos
2. **Software a medida** — soluciones construidas especificamente para el negocio, no herramientas genericas
3. **Integracion de IA** — modelos de lenguaje para generacion de contenido personalizado, analisis, asistentes internos
4. **Visibilidad en tiempo real** — dashboards, reportes automaticos, datos accionables

---

## Page Goal & CTA

**One goal:** Get the visitor interested enough to talk to Omar.

- Primary CTA: "Habla con Omar" — WhatsApp: +525539669841 → https://wa.me/525539669841
- No chatbot. No forms. No friction.
- Secondary goal: credibility building through vertical use cases

---

## Page Structure (Agreed)

1. **Hero** — Headline + subheadline + CTA button
2. **Pain Points** — 3 puntos de dolor que reconocen inmediatamente
3. **Que hacemos** — 4 servicios principales con iconografia
4. **Verticales** — Conceptos de como ExecutionAI aplica en: logistica, salud, empresas de servicios (NO clientes reales, son conceptos ilustrativos)
5. **Por que ExecutionAI** — 15+ anos tecnologia, 7+ anos Uber global, fabrica de software
6. **CTA Final** — "Listo para hablar?" — WhatsApp con Omar

---

## Brand Assets — OFFICIAL (locked in)

### Colors (CSS variables)
```css
--bg:        #07070A   /* near-black background */
--surface:   #0F0F14   /* card surface */
--surface-2: #161620   /* elevated surface / hover */
--border:    #1E1E2A   /* visible borders */
--border-sub:#13131A   /* subtle dividers */
--txt:       #EEEAE3   /* primary text (warm off-white) */
--txt-2:     #8A8A96   /* secondary text */
--txt-muted: #4A4A58   /* muted / labels */
--accent:    #00D9FF   /* electric cyan — THE brand color */
--accent-dim:rgba(0,217,255,0.10)  /* accent backgrounds */
```

### Wordmark
`EXECUTION` in white (`--txt`) + `AI` in electric cyan (`--accent`)
Font: **Syne** weight 700, uppercase, letter-spacing 0.06em

### Typography
- Display / headings: **Syne** (Google Fonts) — weight 700–800
- Body: **Instrument Sans** (Google Fonts) — weight 400–600

### Design Direction
- Dark, premium, tech-forward — Vercel / Linear aesthetic
- Near-black backgrounds, off-white type, single cyan accent
- Razor-sharp spacing, subtle 1px borders, minimal motion
- Grid texture overlay (1px lines, 80px grid, 1.8% opacity)
- NOT default Tailwind palette, NOT generic AI purple/blue gradients

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Single `index.html` — Tailwind CDN + inline styles |
| Backend | None (static page only) |
| Dev server | `serve.mjs` (port 3000) |
| Screenshots | `screenshot.mjs` + Puppeteer |

---

## Frontend Dev Rules

### Always Do First
- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.

### Local Server
```bash
node serve.mjs   # serves at http://localhost:3000
```
- Never screenshot `file:///` — always use localhost
- Do at least **2 compare + fix rounds** before stopping

### Puppeteer Paths (Windows local)
```
Chrome: C:/Users/execu/.cache/puppeteer/chrome/win64-146.0.7680.31/chrome-win64/chrome.exe
```

### Anti-Generic Guardrails
- Never use default Tailwind palette (`indigo-500`, `blue-600`, etc.)
- Never flat `shadow-md` — use layered, color-tinted shadows
- Never same font for headings and body
- Never `transition-all` — only animate `transform` and `opacity`
- Every clickable element needs `hover`, `focus-visible`, and `active` states

---

## Coding Principles
- Single HTML file — no build tooling, no frameworks
- Mobile-first responsive
- Spanish for all client-facing copy
- Never `window.confirm()` — build branded modals if needed
- Keep it fast: no heavy libraries, no unnecessary dependencies
