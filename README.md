# Lotomos: Ruta de Orientación Social con Inteligencia Artificial

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LM Studio](https://img.shields.io/badge/LLM%20Local-LM%20Studio-1E4D40?style=for-the-badge)
![IEEE Format](https://img.shields.io/badge/Documentaci%C3%B3n-Formato%20IEEE-1F3A52?style=for-the-badge)
![Bogotá D.C.](https://img.shields.io/badge/Alcance-Bogot%C3%A1%20D.C.-0F172A?style=for-the-badge)

> **Asistente de orientación social para Bogotá D.C.** que combina un **motor de reglas determinista en Python** con un **modelo de lenguaje (LLM) ejecutado localmente mediante LM Studio** para orientar a ciudadanos y gestores sociales sin enviar información personal a servicios en la nube.

---

## Componentes del proyecto

* **Aplicación en Python + LM Studio:** Captura y valida el perfil del ciudadano (grupo Sisbén, RUI, edad, ingresos, discapacidad, situación laboral, interés en emprender, entre otros). Filtra un catálogo de programas de referencia mediante reglas explícitas (`evaluar()`) y redacta en español claro una explicación y una **Ruta recomendada**.
* **Sitio web:** Portal web de Lotomos orientado a presentar la solución, su enfoque y la guía de orientación para usuarios.
* **Artículo académico en formato IEEE:** Documento técnico estructurado bajo normas IEEE con resumen, palabras clave, arquitectura en tres capas, catálogo y lógica de filtrado, resultados/discusión, conclusiones y referencias.

---

## Arquitectura en tres capas

| Capa | Función principal | Enfoque técnico |
| :--- | :--- | :--- |
| **1. Captura e interacción** | Solicita y valida los datos del perfil ciudadano en consola. | Validación numérica y normalización del grupo Sisbén. |
| **2. Filtrado por reglas** | Contrasta el perfil frente al catálogo de programas de referencia. | Motor determinista (*Rules as Code*) sin intervención del LLM. |
| **3. Inferencia con IA local** | Redacta explicación, categorías y *Ruta recomendada*. | Conexión local a LM Studio (`http://localhost:1234/v1`) con privacidad de datos. |

---

## Estructura del repositorio

```text
Lotomos-Proyecto/
├── src/        # Código en Python y lógica de filtrado / LM Studio
├── web/        # Archivos de la página web del proyecto
├── docs/       # Artículo y recursos en formato IEEE
└── README.md   # Documentación general del repositorio
