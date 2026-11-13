# Guardianes EHS — impresión A4 corregida

Esta versión conserva el ranking, lectura de Excel, logos y animaciones.

## Corrección
- Las barras se dibujan en formato vectorial SVG al imprimir, para conservar el avance y los colores aunque el navegador desactive los fondos.
- El puntero de avance de cada equipo se coloca en su posición correcta antes de imprimir.
- Preparado para A4 horizontal con los 8 equipos.

## Uso
1. Reemplaza `index.html` en GitHub o en tu carpeta de Live Server. Mantén los PNG en la misma carpeta.
2. Carga el Excel y pulsa **ACTUALIZAR RANKING**.
3. Pulsa **Imprimir ranking A4**.
4. En la ventana de impresión selecciona **A4**, **Horizontal**, márgenes predeterminados o mínimos y escala 100%. Si el navegador muestra dos páginas, comprueba primero que no esté seleccionado **Vertical**; de ser necesario elige escala 90%.

Los colores de las barras ya no dependen de la opción «Gráficos de fondo». Para conservar los fondos de las tarjetas y el encabezado, activa esa opción.

La lectura de Excel utiliza una librería externa y necesita Internet.
