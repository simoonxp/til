# 📝 TIL — 2026-08-21

**Aula:** Estatística — FATEC

---

## 📊 Tabela de Distribuição de Frequências

Uma forma de organizar dados agrupados em **classes (intervalos)**, facilitando a análise e visualização.

---

### Colunas da tabela

| Símbolo | Nome | O que significa |
|---|---|---|
| **Classes** | Classes / Intervalos | O intervalo de valores (ex: 1,0 └ 6,0) |
| **xᵢ** | Ponto Médio | Valor central da classe: `(limite inferior + limite superior) / 2` |
| **fᵢ** | Frequência Absoluta | Quantas vezes os valores aparecem naquela classe |
| **fᵢᶏ** | Frequência Relativa | Proporção da classe em relação ao total: `fᵢ / n` |
| **Fᵢ** | Frequência Acumulada | Soma das frequências até aquela classe |
| **Fᵢᶏ** | Frequência Relativa Acumulada | Soma das frequências relativas até aquela classe |

---

### Exemplo prático (do quadro)

| Classes | fᵢ |
|---|---|
| 1,0 ├ 6,0 | 8 |
| 6,0 ├ 11,0 | 11 |
| 11,0 ├ 16,0 | 9 |
| 16,0 ├ 21,0 | 10 |
| 21,0 ├ 26,0 | 9 |
| 26,0 ├ 31,0 | 1 |
| 31,0 ├ 36,0 | 1 |
| **TOTAL** | **49** |

---

### Como calcular cada coluna

```
xᵢ  = (limite inferior + limite superior) / 2
fᵢᶏ = fᵢ / n  (onde n = total de dados)
Fᵢ  = fᵢ da classe atual + Fᵢ da classe anterior
Fᵢᶏ = fᵢᶏ da classe atual + Fᵢᶏ da classe anterior
```

**Por que importa:** A tabela de distribuição de frequências é a base da estatística descritiva — usada para resumir grandes conjuntos de dados e identificar padrões.
