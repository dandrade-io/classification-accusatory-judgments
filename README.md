## **Clasificación de Comentarios Acusatorias**
### **Machine Learning - Proyecto Final**

**Integrantes:**
 - Isabella Tulcán
 - Daniel Andrade
 - Jarod Sierra

## **Introducción y Metodología**
### **Introducción**
El presente proyecto tiene como finalidad analizar los comentarios de los procesos de contratación pública en Ecuador utilizando modelos de aprendizaje supervisado tradicionales junto con técnicas de representación de texto (Regresión Logística y Random Forest) y feature extraction (TF-IDF y Transfer Learning), con el objetivo de detectar si los comentarios indican ser acusatorios o no.

Para cada variante de modelo se realizará su respectiva optimización de hiperpárametos mediante CV (cross-validation). Finalmente, se compará el rendimiento entre los distintos modelos con la finalidad de determinar aquel más idóneo.

### **Metodología**
- No se aplicarán técnicas de aumento de datos.
- El proceso de preprocesamiento del texto será el siguiente: corregir faltas ortográficas; remover stop words, urls y similares; finalmente, applicar lemmatization
- Entrenar modelos de Regresión Logística y Random Forest con técnicas de TF-IDF y Transfer Learning.
- Comparar el rendimiento de los modelos a través del test de hipótesis con $\alpha = 0.05$