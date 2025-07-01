# 🤖 Clasificador de Opiniones y Reclamos en Videos de TikTok

**Modelo de Machine Learning que identifica si un video en TikTok contiene una opinión o un reclamo, utilizando variables estructurales y análisis textual.**

## 📌 Objetivo del proyecto

Desarrollar un clasificador robusto basado en aprendizaje automático que permita distinguir entre opiniones y reclamos en videos de TikTok, apoyándose en texto transcrito y metadatos de engagement.

## 🧠 Tecnologías utilizadas

- Python 3.x
- Scikit-learn, XGBoost, Random Forest
- Pandas, NumPy, Matplotlib, Seaborn
- Jupyter Notebook
- Técnicas de NLP y análisis de importancia de variables (SHAP/LIME)

## 🧪 Resultados del modelo

| Clasificador   | Precisión | Recall | AUC   |
|----------------|-----------|--------|-------|
| Random Forest  | 78%       | 86%    | 0.83  |
| XGBoost        | 81%       | 100%   | 0.84  |
| 🔥 XGBoost (validación cruzada) | ~100%     | ~100%  | 1.000 |

✔️ El modelo mantiene un AUC perfecto incluso al eliminar la variable dominante `video_view_count`, demostrando generalización genuina.

## 🔍 Características clave

- **Resistente a sobreajuste**: limpieza textual y análisis de variables irrelevantes.
- **Alto valor predictivo del texto transcrito**: palabras como “claim”, “opinion” o “media” son determinantes.
- **Modelo explicable**: análisis de importancia de variables con enfoque ético.
- **Transferible**: el pipeline es adaptable a nuevas plataformas y campañas.

## 🗂️ Estructura del repositorio

📁 data/             → Datos anonimizados o de ejemplo 
📁 notebooks/        → Construcción y evaluación de modelos 
📁 docs/             → Informe en PDF y presentación ejecutiva 
📄 README.md         → Este archivo




## 🔄 Próximos pasos

- Probar con datos en vivo de nuevas campañas
- Incluir explicabilidad visual (SHAP/LIME)
- Integrar modelo a dashboards internos para reputación digital
- Escalar el pipeline a múltiples idiomas o redes

## 👤 Autor

Creado por **Juan** — Analista de Datos apasionado por la ética algorítmica y la inteligencia social digital.

## 📄 Licencia

Este proyecto se encuentra bajo la licencia [MIT](LICENSE).

