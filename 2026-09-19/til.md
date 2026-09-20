# 📝 TIL — 2026-09-19

---

## 🐍 Python — Estrutura de Dados e Pilhas (aprofundamento)

---

### Pilha (Stack) — revisão e aprofundamento

```python
# Pilha com lista
pilha = []
pilha.append(10)   # push
pilha.append(20)
pilha.append(30)

print(pilha[-1])   # peek: 30
pilha.pop()        # pop: remove 30
print(pilha)       # [10, 20]

# Pilha com deque (mais eficiente)
from collections import deque
pilha = deque()
pilha.append(1)
pilha.append(2)
pilha.pop()
```

---

### Fila (Queue) — FIFO

```python
from collections import deque

fila = deque()
fila.append("primeiro")   # enqueue
fila.append("segundo")
fila.popleft()            # dequeue: remove "primeiro"
print(fila)               # deque(['segundo'])
```

---

### Comparação

| Estrutura | Ordem | Operações |
|---|---|---|
| **Pilha (Stack)** | LIFO | `append()` / `pop()` |
| **Fila (Queue)** | FIFO | `append()` / `popleft()` |
| **Lista** | Indexada | qualquer posição |

---

> *"A estrutura de dados certa resolve o problema com menos esforço."*
