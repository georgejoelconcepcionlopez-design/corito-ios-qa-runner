# Corito iOS QA Runner (public controller)

Repositorio público de **solo control de CI** para ejecutar el QA de dispositivos de
iOS/macOS en runners de GitHub Actions.

No contiene código fuente de la app.

- Fuente privada: `corito-domino-flutter` (se clona en el runner mediante una
  **SSH deploy key de solo lectura** desde un **secret**).
- Único disparador permitido: `workflow_dispatch` (ninguna ejecución desde PR externos).
- Permisos del workflow: `contents: read` (mínimo privilegio).
- Runner: `macos-26` estándar (gratuito en repos públicos).
- Artefactos: solo resultados QA, logs sanitizados y screenshots; `retention-days: 1`.