# 🔬 Análise de Perfis Oculares com K-Means Clustering

Este projeto realiza uma análise de perfis oculares baseada em medidas biométricas, utilizando o algoritmo de agrupamento **K-Means**. O objetivo é auxiliar na identificação de padrões como **miopia, hipermetropia** e olhos **normais**, aplicável em diagnósticos oftalmológicos e cálculo de lentes intraoculares.

---

## 📋 Variáveis analisadas:

- **AL** — Comprimento axial do olho  
- **ACD** — Profundidade da câmara anterior  
- **WTW** — Distância branco a branco  
- **K1** — Curvatura no meridiano menos curvo  
- **K2** — Curvatura no meridiano mais curvo  

---

## 🧠 Contexto Médico

A **biometria ocular** mede estruturas essenciais do olho e é fundamental em cirurgias como a de catarata.

Principais responsáveis pelo foco da luz:
- Córnea (`K1`, `K2`) — cerca de 42 dioptrias.
- Comprimento axial (`AL`) — cerca de 18 dioptrias.

**Classes de olhos:**
- Emétrope — normal  
- Miopia — olhos longos e curvatura reduzida  
- Hipermetropia — olhos curtos e curvatura elevada  
- Astigmatismo — diferenças de curvatura nos meridianos  

---

## 💻 Metodologia

**1️⃣ Pré-processamento:**  
- Limpeza de dados nulos.  
- Normalização com `StandardScaler` para uniformizar as escalas.

**2️⃣ Escolha do Número de Grupos (`k`):**  
- Definição via **Método do Cotovelo**.

**3️⃣ Agrupamento com K-Means:**  
- Algoritmo aplicado após normalização.
- Visualizações com:
  - Pairplot (exploração inicial)
  - Matriz de correlação (`K1` e `K2` = correlação forte de 0.92)
  - PCA + ScatterPlot para visualização dos clusters.

---

## 📊 Conclusão

- Miopia: `AL > 18` e `K1/K2 < 42`.  
- Hipermetropia: `AL < 18` e `K1/K2 > 42`.  
- Clusters formados: casos de **miopia** bem separados e olhos **normais**.  
- Dados de hipermetropia possivelmente ausentes no conjunto.

---

## 📚 Fontes

- https://www.draandreia.com.br/?page_id=1027  
- https://medium.com/pizzadedados/kmeans-e-metodo-do-cotovelo-94ded9fdf3a9  

