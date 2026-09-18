# 📝 TIL — 2026-09-17

---

## 🐍 Python — Pilha (Stack) e Estrutura de Dados

---

### O que é uma Pilha?

Pilha é uma estrutura de dados do tipo **LIFO** (Last In, First Out) — o último elemento inserido é o primeiro a sair.

---

### Implementação em Python

```python
# Usando lista como pilha
pilha = []

# Empilhar (push)
pilha.append(1)
pilha.append(2)
pilha.append(3)
print(pilha)  # [1, 2, 3]

# Desempilhar (pop)
topo = pilha.pop()
print(topo)   # 3
print(pilha)  # [1, 2]

# Ver o topo sem remover
topo = pilha[-1]
print(topo)   # 2

# Verificar se está vazia
vazia = len(pilha) == 0
```

---

### Casos de uso

| Uso | Exemplo |
|---|---|
| Desfazer ações | Ctrl+Z em editores |
| Navegação | Botão "voltar" do navegador |
| Chamadas de função | Call stack do Python |
| Verificação de parênteses | Compiladores |

---

> *"Entender estruturas de dados é entender como o computador pensa."*
