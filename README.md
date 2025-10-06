# SPL-PM-algoritmo-Dijkstra
sistema que importa topologias de rede, modela ativos como vértices com atributos (ex.: CVE score, exposição, privilégio) e arestas com custo (latência, credencial necessária). Gera os caminhos de menor custo desde um nó atacante a ativos críticos usando Dijkstra e sugere contramedidas priorizadas.

# SPL-PM – Simulador de Propagação Lateral e Priorização de Mitigações 
<div align="center">
  <img src="https://github.com/LucaLSN/SPL-PM-algoritmo-Dijkstra/blob/master/dijkstra-img.jpeg" alt="ilustração do algoritmo de Dijkstra" width="500"/>
</div>

##  Visão Geral
O **SPL-PM** é uma ferramenta educacional e prática para simular movimentos laterais de atacantes em uma rede modelada como grafo em seu background.  
Ele utiliza o algoritmo de **Dijkstra** para calcular os caminhos de menor custo até ativos críticos e sugere **mitigações priorizadas**.

- -->  Foco em cibersegurança defensiva (Threat Modeling, Blue Team).
- -->  Baseado em teoria dos grafos (networkx, Dijkstra).
- -->  Ajuda a priorizar defesas em redes complexas.

---

## Funcionalidades esperadas (MVP)
- [ ] Importar topologia de rede em CSV/JSON.
- [ ] Modelar ativos (nós) com atributos:
- [ ] CVSS, exposição, privilégios.
- [ ] Calcular caminho mínimo de ataque com Dijkstra.
- [ ] Exibir o grafo e destacar o caminho encontrado.
- [ ] Gerar relatório com recomendações básicas de mitigação.

---

## 📂 Estrutura de Entrada (exemplo JSON)
```json
{
  "nodes": [
    {"id": "A", "role": "Attacker", "cvss": 0},
    {"id": "B", "role": "Servidor", "cvss": 7.5},
    {"id": "C", "role": "Banco de Dados", "cvss": 9.8}
  ],
  "edges": [
    {"source": "A", "target": "B", "weight": 1},
    {"source": "B", "target": "C", "weight": 2}
  ]
}
