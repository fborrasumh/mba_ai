# Laboratorio IA · MBA-UMH — 20 apps de obligado uso

Suite de 20 simuladores docentes con IA para el **Máster Universitario en Administración y Dirección de Empresas (MBA)** de la UMH (tit_m_198), alineados con el plan de estudios oficial.

## Arquitectura (kernel compartido)

- Single-file HTML + vanilla JavaScript, sin frameworks ni backend.
- Modelo `gpt-4o-mini` vía API de OpenAI; clave en `localStorage` (`ia_openai_key`), compartida entre todas las apps del mismo dominio.
- Flujo en 3 fases: **Caso generado por IA → Simulación conversacional en rol → Evaluación con rúbrica (JSON estructurado)**.
- Historial de sesiones en **IndexedDB** (una base por app: `mba_umh_<id>`).
- Exportación de informe: **Markdown** descargable e **impresión/PDF** del navegador.

## Catálogo por asignatura

| Asignatura | Apps |
|---|---|
| Administración y Dirección Estratégica | EstrategIA · ComitéDirectivo·AI |
| Dirección de Operaciones, Innovación y Calidad | LeanOps·AI · AuditorIA |
| Creación de Empresas y Emprendimiento | Canvas·AI · PitchLab·AI · ValidaIdea·AI |
| Gestión Laboral y Dirección del Comportamiento | Negocia·AI · FeedbackPro·AI · Selecta·AI |
| Decisiones de Marketing | MarketingPlan·AI · FocusGroup·AI |
| Dirección Económica-Financiera | RatioLab·AI · InvertIA |
| Derecho Empresarial | LexEmpresa·AI |
| Prácticas Externas | DiarioPrácticas·AI |
| Optativas | SimulaEmpresa·AI · MétodoLab·AI |
| Trabajo Fin de Máster | TFM·Coach · Tribunal·AI |

## Despliegue en GitHub Pages

1. Crea un repositorio (p. ej. `mba-umh-ia`).
2. Sube el contenido de esta carpeta `docs/` (o toda la carpeta).
3. Settings → Pages → Source: rama `main`, carpeta `/docs` (o raíz).
4. La URL será `https://<usuario>.github.io/mba-umh-ia/`.

## Uso docente propuesto

El estudiante realiza las sesiones marcadas por cada asignatura, exporta el informe con transcripción + rúbrica y lo entrega como evidencia de evaluación continua. La nota de la rúbrica es orientativa: la calificación final la fija el profesorado.
