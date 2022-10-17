---
theme: takahashi
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## tRPC
  Durchgängige typsichere APIs leicht gemacht
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS
css: unocss
---


trpc
# Durchgängige typsichere APIs

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/sophiabrandt/webworker-hannover-trpc-talk" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---

Sophia Brandt
<div>
<a href="https://www.newcubator.com" target="_blank" alt="Newcubator"
class="text-xl icon-btn opacity-50 !border-none !hover:text-black">
Software-Entwicklerin @newcubator GmbH</a>
</div>

<div>
<a href="https://twitter.com/hisophiabrandt" target="_blank" alt="Twitter"
class="text-xl icon-btn text-blue opacity-50 !border-none !hover:text-blue">
<carbon-logo-twitter />@hisophiabrandt</a>
</div>

<ul>
<li class="text-sm">TypeScript</li>
<li class="text-sm">Go</li>
<li class="text-sm">Kommandozeile: (Neo)Vim, Tmux, Fish Shell</li>
<li class="text-sm">Esperanto 💚</li>
</ul>

---

tRPC - 

was & wozu? ✅

---

full-stack TypeScript

---

automatische Typsicherheit

---

Framework-unabhängig

---

Developer Experience

---

modular

---

leichtgewichtig

---

Fernzugriff auf den BackendCode

---

🚫 Schema

🚫 Sprache (Query Language)

---

Keine Codegenerierung

---

"reduziertes REST"

---

# T3 Stack Demo

```ts
pnpm dlx create-t3-app@latest
```

---

tRPC
❌

---

nur: TS Monorepos

---

APIs von Drittanbietern

---

andere Programmiersprachen als TS

---

TS Development Performance (viele Endpunkte)

---

Support für alles außer React


---

🥊 trpc vs GraphQL


---

GraphQL

---

Schema Definition

---

geteilte Sprache zwischen Backend & Frontend

---

löst

Kommunikations-/

Organisationsprobleme

---

```mermaid {theme: 'neutral', scale: 0.8}
sequenceDiagram
    Database->>+Backend: SQL/NoSQL  
    Backend-->>-Database: ORMS, etc.
    Note over Backend,Frontend: GraphQL Schema
    Backend->>+Frontend: Go, Rust, Java, etc.
    Frontend-->>-Backend: TypeScript, Elm, etc.
```

---

```mermaid {theme: 'neutral', scale: 0.8}
sequenceDiagram
    Database->>+Backend: SQL/NoSQL  
    Backend-->>-Database: ORMS, etc.
    Backend->>+Frontend: tRPC (TypeScript)
    Frontend-->>-Backend: tRPC (TypeScript)
```

---

gRPC?

---

Hat **nichts** mit tRPC zu tun

---

remote procedure calls

---

Kommunikation zwischen Servern

(verteilte Systeme)

---

trpc?

---

Kommunikation zwischen BE & FE
