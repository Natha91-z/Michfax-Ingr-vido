# 🚀 Michfax Ingrávido — Explorador de Evidencia en Seguridad contra Incendios Espaciales
### Spacecraft Fire Safety Evidence Explorer (Bilingual: EN / ES)

**Equipo / Team:** Cóndor Ingrávido  
**Reto / Challenge:** NASA Space Apps Challenge 2026 — *Flame in Freefall*  
**Autora / Author:** Nathalia Gutiérrez Pinilla  
**Fecha / Date:** 15 de noviembre de 2026  

---

## 🎯 ¿Qué problema resuelve? / What problem does it solve?

**ES:** La mayoría de los estudios espaciales analizan cómo se comporta una llama en microgravedad. **Michfax Ingrávido** responde a la pregunta crítica de la tripulación: *cuando algo empieza a arder en la Estación Espacial Internacional (ISS), un hábitat lunar o una nave rumbo a Marte, ¿sonará la alarma antes de que el aire se vuelva tóxico?*

**EN:** Most space combustion studies ask how flames behave in microgravity. **Michfax Ingrávido** asks the crew's critical question: *when something starts to burn on the ISS, a lunar habitat, or a spacecraft bound for Mars, will the alarm sound before the cabin air becomes hazardous?*

---

## ✨ Funcionalidades principales / Key Features

* **01 · El punto ciego del detector (SAME-2):** Gráfica interactiva y tabla comparativa del diámetro de partículas de humo fresco vs. envejecido (720 s), demostrando por qué el detector de dispersión de luz de la ISS falla frecuentemente con **Teflón** y **Kapton**.
* **02 · Toxicidad temprana y lector CSV de NASA PSI (Saffire VI):** Visualización en tiempo real de concentraciones de Monóxido de Carbono (CO) frente a los límites SMAC de la NASA (100 ppm / 24h y 425 ppm / 1h), con soporte para subir archivos `.csv` propios desde **NASA Physical Sciences Informatics (PSI)**.
* **03 · Explicador de escenarios basado en reglas:** Motor transparente sin alucinaciones que evalúa riesgos según el entorno (ISS, Luna, Marte), el material y el estado de la ventilación, citando cada hallazgo.
* **04 · Verificación en vivo de huecos de evidencia (NASA NTRS API):** Consulta directa a la API oficial de NASA NTRS (`api.ntrs.nasa.gov`) para comprobar en tiempo real la escasez de datos publicados sobre detección de humo en gravedad lunar (`0.165 g`, `34% O₂`) y marciana (`0.38 g`).
* **05 · Recomendaciones de ingeniería:** Propuestas basadas en evidencia (detección multimomento MPASS, sensores combinados de gas CO/CO₂ y pruebas de humo en gravedad lunar).
* **07 · Bibliografía verificada automáticamente:** Validación dinámica de metadatos y enlaces oficiales mediante la API REST de NASA NTRS.

---

## 🛠️ Tecnologías y Datos Abiertos de la NASA / Tech Stack & NASA Open Data

* **Frontend:** HTML5, CSS3 (diseño responsivo oscuro), JavaScript (Vanilla ES6+).
* **Visualización de datos:** [Chart.js](https://chartjs.org)
* **APIs y Repositorios Oficiales de la NASA:**
  * **NASA Technical Reports Server (NTRS) OpenAPI:** `https://nasa.gov` (consulta de metadatos y búsqueda de literatura en tiempo real sin necesidad de API Key).
  * **NASA Physical Sciences Informatics (PSI):** Datos experimentales de combustión (SAME-2, Saffire VI, BASS-II).

---

## 🚀 Cómo ejecutar el proyecto localmente / How to run locally

1. Clona o descarga este repositorio:
   ```bash
   git clone https://github.com/Natha91-z/Michfax-Ingr-vido.git
   ```
2. Abre la carpeta en **Visual Studio Code**.
3. Para evitar restricciones CORS del navegador al consultar la API de la NASA (`fetch`), abre el archivo `index.html` usando una extensión de servidor local (como **Live Server**) o mediante Python:
   ```bash
   python -m http.server 8000
   ```
4. Abre `http://localhost:8000` en tu navegador.

---

## 📚 Fuentes Científicas / Scientific References

1. **Urban, D. L., et al. (2012).** *Particle Morphology and Size Results from the Smoke Aerosol Measurement Experiment-2 (SAME-2)*. NASA NTRS `20130000422`.
2. **Meyer, M. E., et al. (2018).** *Evaluation of spacecraft smoke detector performance in the low-gravity environment*. Fire Safety Journal, 98.
3. **Urban, D. L., et al. (2024).** *Preliminary Results from the Saffire VI Experiment*. ICES-2024-365 / NASA NTRS `20240002981`.
4. **Olson, S., et al. (2019).** *Flammability Limits from BASS-II Testing in Microgravity Compared to Normal Gravity Limits*. 49th ICES.
5. **Urban, D. L., et al. (2017).** *Saffire: A Novel Approach to Study of Spacecraft Fire Safety Using Un-manned Spacecraft*. NASA NTRS `20180005168`.
6. **Ferkul, P., et al. (2026).** *Material Flammability at Lunar and Martian Gravity*. LPSC 2026 / NASA NTRS `20260001966`.
7. **NASA Physical Sciences Informatics (PSI):** Combustion Science Investigations (`psi.nasa.gov`).

---

## ⚠️ Aviso / Disclaimer

*Este proyecto fue creado para el NASA Space Apps Challenge 2026 y no es un producto oficial de la NASA. Se utilizó asistencia de inteligencia artificial (Claude de Anthropic y Gemini de Google) para estructurar literatura científica y código fuente; todas las cifras y citas fueron verificadas contra las publicaciones originales.*
