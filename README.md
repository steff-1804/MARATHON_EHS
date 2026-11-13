# Guardianes EHS — Ranking mejorado

## Cómo abrir
1. Descomprime el ZIP sin separar la carpeta `logos` del archivo `index.html`.
2. En Visual Studio Code, abre la carpeta y ejecuta `index.html` con Live Server.
3. Mantén conexión a Internet: la lectura de Excel usa SheetJS desde un CDN.
4. Selecciona uno o varios Excel y pulsa **ACTUALIZAR RANKING**.
5. Para consultar puntajes, selecciona **Mes individual** o **Acumulado**, el mes inicial y la cantidad de meses. La meta se calcula como meses seleccionados × meta mensual.
6. El umbral satisfactorio es configurable (70% por defecto).

## Estructuras admitidas
- La hoja `Total de marathon` del Excel maestro original: bloques de equipos en horizontal, con `MES` y `PUNTAJE OBTENIDO`.
- Tabla: `EQUIPO | MES | PUNTAJE OBTENIDO` (opcional `PUNTOS ADICIONALES` o `TOTAL`).
- Matriz: `EQUIPO | ENERO | FEBRERO | MARZO ...`.
- Matriz transpuesta: `MES | 1RX | CAI | CND ...`.
- Hoja individual de un equipo/mes con etiquetas `P obtenidos` y `Puntos adicionales`, o celdas C65 y C66 cuando se puede reconocer el equipo y el mes.
- Varios archivos: si se repite un equipo y mes, el último archivo cargado reemplaza al anterior. Evita duplicar totales.

## Interpretación del medidor
- Cada equipo con al menos un puntaje en el período se considera evaluado.
- El equipo alcanza el nivel satisfactorio cuando sus puntos son al menos el porcentaje configurado de la meta del período.
- Verde: más de la mitad de los evaluados alcanza el umbral.
- Rojo: más de la mitad está bajo el umbral.
- Amarillo: empate.
- Sin datos: no se muestra un diagnóstico.
- Puntajes superiores a la meta aparecen con la marca EXCESO; el valor numérico real no se recorta.

## Limitaciones importantes
- No existe lectura universal de cualquier diseño de Excel: las estructuras no identificables se reportan en observaciones, sin inventar puntajes.
- Si una fórmula de Excel no tiene un valor calculado guardado, puede que no sea legible. Abre el archivo en Excel, recalcula y guarda antes de subirlo.
- La página no sube los archivos a un servidor; se leen en el navegador. Al recargar la página, debes volver a cargar el Excel.
