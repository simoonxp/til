# 📝 TIL — 2026-08-18

**Aula:** Banco de Dados 2 — FATEC

---

## 🔒 Controle de Concorrência

### 1. Bloqueios (Locks) — S e X

Quando várias transações acessam o banco ao mesmo tempo, os locks evitam conflitos:

| Tipo | Nome | Leitura | Escrita |
|---|---|---|---|
| **S** | Shared (Compartilhado) | ✅ | ❌ |
| **X** | Exclusive (Exclusivo) | ❌ | ✅ |

- **Lock S** → várias transações podem ler ao mesmo tempo
- **Lock X** → só uma transação por vez, bloqueia todas as outras

---

### 2. Protocolo 2PL (Two-Phase Locking)

Garante serializabilidade dividindo a transação em duas fases:

| Fase | O que acontece |
|---|---|
| **Crescimento** | Só pode **adquirir** locks |
| **Encolhimento** | Só pode **liberar** locks |

> Após liberar o primeiro lock, não pode mais adquirir novos.

---

### 3. 2PL Estrito e 2PL Rigoroso

| Variação | Quando libera os locks |
|---|---|
| **2PL Estrito** | Libera locks X somente após commit/abort |
| **2PL Rigoroso** | Libera **todos** os locks (S e X) somente após commit/abort |

---

### 4. Protocolo 2PC (Two-Phase Commit) — Replicação Distribuída

Garante que todos os nós de um banco distribuído confirmem ou cancelem juntos:

| Fase | O que acontece |
|---|---|
| **Preparação** | Coordenador pergunta a todos: *"Pode fazer commit?"* |
| **Commit/Abort** | Todos disseram sim → commit. Algum disse não → abort em todos |

> Ou todos confirmam, ou ninguém confirma.

---

## 🔄 Replicação Distribuída

### 5. Replicação Master-Slave

Um nó principal (Master) recebe todas as escritas e replica para os escravos (Slaves).

| Aspecto | Detalhe |
|---|---|
| **Escrita** | Sempre no Master |
| **Leitura** | Pode ser feita nos Slaves |
| **Confirmação** | Pode ser síncrona ou assíncrona |
| **Falha do Master** | Um Slave é promovido a novo Master |
| **Limitação** | Gargalo no Master para escritas; Slaves podem ter dados desatualizados |

---

### 6. Replicação Masterless (P2P)

Não há um nó principal — qualquer nó pode receber leitura ou escrita.

| Aspecto | Detalhe |
|---|---|
| **Escrita** | Qualquer nó aceita |
| **Problema** | Conflitos de escrita concorrente |
| **Solução** | Votação entre nodos (quorum) |

**Como funciona a votação (Quorum):**
- Para escrever, o nó precisa da confirmação da maioria dos outros nós
- Se dois nós receberem escritas diferentes ao mesmo tempo, a que tiver mais votos vence
- Garante consistência sem precisar de um nó central

> **Por que importa:** Masterless é mais resiliente (sem ponto único de falha), mas exige estratégias para resolver conflitos de escrita.
