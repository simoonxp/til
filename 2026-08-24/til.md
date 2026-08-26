# 📝 TIL — 2026-08-24

---

## 🐍 Python — Estrutura de Dados (continuação)

---

### Algoritmos de Busca

```python
# Busca Linear — O(n)
def busca_linear(lista, alvo):
    for i, item in enumerate(lista):
        if item == alvo:
            return i
    return -1

# Busca Binária — O(log n) — lista deve estar ordenada
def busca_binaria(lista, alvo):
    esq, dir = 0, len(lista) - 1
    while esq <= dir:
        meio = (esq + dir) // 2
        if lista[meio] == alvo:
            return meio
        elif lista[meio] < alvo:
            esq = meio + 1
        else:
            dir = meio - 1
    return -1
```

---

### Algoritmos de Ordenação

```python
# Bubble Sort — O(n²)
def bubble_sort(lista):
    n = len(lista)
    for i in range(n):
        for j in range(0, n-i-1):
            if lista[j] > lista[j+1]:
                lista[j], lista[j+1] = lista[j+1], lista[j]
    return lista

# Python nativo — muito mais eficiente
lista_ordenada = sorted([3, 1, 4, 1, 5, 9, 2, 6])
```

---

### Complexidade de Tempo

| Algoritmo | Melhor caso | Pior caso |
|---|---|---|
| Busca Linear | O(1) | O(n) |
| Busca Binária | O(1) | O(log n) |
| Bubble Sort | O(n) | O(n²) |
| sorted() Python | O(n log n) | O(n log n) |

---

> *"Entender a complexidade é entender por que algumas soluções escalam e outras não."*
