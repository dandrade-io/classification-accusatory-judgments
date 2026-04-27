## **Clasificación de Comentarios Acusatorias**
### **Machine Learning - Proyecto Final**

**Integrantes:**
 - Isabella Tulcán
 - Daniel Andrade
 - Jarod Sierra
 
 ---

## **Introducción y Metodología**
### **Introducción**
El presente proyecto tiene como finalidad analizar los comentarios de los procesos de contratación pública en Ecuador utilizando modelos de aprendizaje supervisado tradicionales junto con técnicas de representación de texto (Regresión Logística y Random Forest) y feature extraction (TF-IDF y Transfer Learning), con el objetivo de detectar si los comentarios indican ser acusatorios o no.

Para cada variante de modelo se realizará su respectiva optimización de hiperpárametos mediante CV (cross-validation). Finalmente, se compará el rendimiento entre los distintos modelos con la finalidad de determinar aquel más idóneo.

### **Metodología**
- No se aplicarán técnicas de aumento de datos.
- El proceso de preprocesamiento del texto será el siguiente: corregir faltas ortográficas; remover stop words, urls y similares; finalmente, applicar lemmatization
- Entrenar modelos de Regresión Logística y Random Forest con técnicas de TF-IDF y Transfer Learning.
- Comparar el rendimiento de los modelos a través del test de hipótesis con $\alpha = 0.05$

## **Conclusiones**

Este proyecto buscó clasificar comentarios acusatorios en procesos de contratación pública ecuatoriana, utilizando cuatro combinaciones de modelos y técnicas de representación de texto.

### Hallazgos principales

1. El desbalance de clases (97:3) fue el principal desafío. Las métricas de accuracy resultaron engañosas, por lo que fue necesario priorizar F1-score, recall y AUC para evaluar correctamente la capacidad de detección de la clase minoritaria.

2. TF-IDF y SBERT ofrecen representaciones complementarias. El t-SNE mostró que ninguna representación genera clusters perfectamente separables, pero los embeddings SBERT capturan mejor la semántica contextual necesaria para este problema.

3. La Regresión Logística con TF-IDF y el Random Forest con SBERT fueron los mejores modelos de cada grupo. Ambos alcanzaron accuracy $\geq 0.95$ con una detección razonable de la clase acusatoria.

4. El test de Wilcoxon no encontró diferencias estadísticamente significativas entre los modelos finalistas ($p \geq 0.05$), lo que indica que ambos son equivalentes en términos de accuracy. En este caso, se recomienda preferir TF-IDF + Regresión Logística por su menor costo computacional y mayor interpretabilidad.

5. Las curvas de aprendizaje revelan un ajuste perfecto en entrenamiento pero una brecha con validación, atribuible al desbalance de clases y no necesariamente a sobreajuste clásico.

---

**Link Colab**: https://colab.research.google.com/drive/1BOD_TOoJYODrsMEduNNsiikhvRX0bbwK?usp=sharing