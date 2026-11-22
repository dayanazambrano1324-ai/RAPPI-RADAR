# Rappi Radar — proyecto Android

Este ZIP incluye un flujo de compilación en la nube mediante GitHub Actions, para que puedas generar el APK sin tener computador.

## Compilar desde el teléfono
1. Crea/inicia sesión en una cuenta de GitHub desde Chrome.
2. Crea un repositorio nuevo (por ejemplo `rappi-radar`).
3. En el repositorio, usa Add file > Upload files y sube el contenido de este ZIP ya descomprimido. Asegúrate de incluir la carpeta oculta `.github/workflows`.
4. Abre la pestaña Actions y ejecuta `Build Rappi Radar APK` si no se ejecutó automáticamente.
5. Cuando termine correctamente, entra a la ejecución y descarga el artefacto `RappiRadar-debug-apk`.
6. Descomprime el artefacto y encontrarás `app-debug.apk`. Android puede pedir autorización para instalar desde Chrome/Archivos.

## Reglas de cálculo
- Individual: pago mostrado / kilómetros mostrados.
- Adicional: prioriza el pago adicional claramente identificado y lo divide por los km adicionales.
- Menos de $2.000/km: MALO; $2.000–$2.999/km: BUENO; $3.000/km o más: EXCELENTE.

## Limitaciones
Este es un prototipo experimental. El APK de depuración no está probado en Rappi real. La lectura automática solo funcionará si Rappi expone el texto a Accesibilidad. Si los datos están dibujados como imagen, habrá que agregar captura autorizada por Android y OCR. No acepta ni rechaza pedidos automáticamente. No uses la clasificación como garantía de rentabilidad hasta validar con pedidos reales.
