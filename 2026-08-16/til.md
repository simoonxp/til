# 📝 TIL — 2026-08-16

## 📊 Excel — Fórmula `=FILTRO()`

---

Aprendi a usar a fórmula `=FILTRO()` para separar dados de uma tabela por categoria automaticamente.

**Fórmula usada:**
```excel
=FILTRO(A:A; B:B="Marketing")
```

**Como funciona:**
- `A:A` → a coluna que você quer trazer (ex: nomes)
- `B:B="Marketing"` → a condição do filtro

**Exemplo prático:**

Tabela original:

| Nome | Área |
|---|---|
| Rafael | Marketing |
| Mariana | TI |
| Gilson | Finanças |
| Gabriela | Marketing |
| Larissa | Marketing |
| ... | ... |

Resultado separado por área:

| Marketing | Finanças | TI |
|---|---|---|
| Rafael | Gilson | Mariana |
| Gabriela | Guilherme | Isabela |
| Larissa | Eduardo | Thiago |
| Pedro | Ana | Rodrigo |
| João | Fernanda | André |
| Carolina | Juliana | |
| Victor | | |

**Por que importa:** Em vez de filtrar manualmente, a fórmula separa os dados automaticamente e atualiza sozinha quando a tabela muda.

---

## 🗄️ Banco de Dados 2 — FATEC — Bloqueios e Protocolos de Concorrência

---

### 🔒 Bloqueios (Locks) — S e X

Quando várias transações acessam o banco ao mesmo tempo, os locks evitam conflitos:

| Tipo | Nome | Permite leitura? | Permite escrita? |
|---|---|---|---|
| **S** | Shared Lock (Compartilhado) | ✅ Sim | ❌ Não |
| **X** | Exclusive Lock (Exclusivo) | ❌ Não | ✅ Sim |

- **Lock S** → várias transações podem ler ao mesmo tempo
- **Lock X** → só uma transação por vez pode escrever, bloqueando todas as outras

---

### 🔁 Protocolo 2PL (Two-Phase Locking)

Garante serializabilidade dividindo a transação em duas fases:

| Fase | O que acontece |
|---|---|
| **Fase de Crescimento** | A transação só pode **adquirir** locks |
| **Fase de Encolhimento** | A transação só pode **liberar** locks |

> Após liberar o primeiro lock, não pode mais adquirir novos.

**Variações:**

- **2PL Estrito** → libera os locks X só após o commit/abort
- **2PL Rigoroso** → libera **todos** os locks (S e X) só após o commit/abort

---

### 🤝 Protocolo de Commit em Duas Fases (2PC)

Usado em bancos de dados distribuídos para garantir que todos os nós confirmem ou cancelem juntos:

| Fase | O que acontece |
|---|---|
| **Fase 1 — Preparação** | Coordenador pergunta a todos os nós: *"Pode fazer commit?"* |
| **Fase 2 — Commit/Abort** | Se todos disseram sim → commit. Se algum disse não → abort em todos |

> **Por que importa:** Garante que em um sistema distribuído, ou todos confirmam a transação ou ninguém confirma.
