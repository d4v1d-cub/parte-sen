# Parte diario del SEN

**Sitio:** https://d4v1d-cub.github.io/parte-sen/

Página web que muestra la evolución diaria del Sistema Eléctrico Nacional (SEN) de Cuba a partir del parte que publica cada día la Unión Eléctrica (UNE): demanda, disponibilidad, déficit y afectación en el horario pico, la lectura de la mañana, las cifras del día anterior y el estado de las unidades térmicas.

## Qué muestra

- **Resumen:** la afectación pronosticada en el parte más reciente y qué parte de la demanda prevista representa.
- **Período:** botones para los últimos 7 días, 30 días, 90 días, 1 año o todo el registro, y fechas «Desde» y «Hasta» para elegir un intervalo concreto.
- **Magnitudes:** se eligen las que se quieren graficar, agrupadas en *Horario pico*, *Mañana (06:00)*, *Datos reales* y *Generación*.
- **Gráficas:** una por tipo de unidad (MW, MWh, porcentaje y número de unidades), con el valor de cada día al pasar el ratón o tocar la gráfica. Los colores se asignan según las magnitudes marcadas. A partir de la novena magnitud marcada a la vez, los colores se repiten con línea discontinua.
- **Tabla:** los datos del período elegido, en una tabla desplegable.
- **Descarga:** los datos completos en formato CSV.

## De dónde salen los datos

Las cifras de cada fecha se refieren a ese día. El pronóstico sale del parte de la UNE de esa fecha. Los datos reales (afectación máxima, energía solar y afectación en La Habana) salen del parte del día siguiente, que los informa como «día anterior». Así, el pronóstico y lo que de verdad ocurrió quedan en la misma fecha.

Los datos se toman del parte publicado en los canales de Telegram de la [Unión Eléctrica](https://t.me/une_cuba) y de la [Empresa Eléctrica de La Habana](https://t.me/EmpresaElectricaDeLaHabana). Cuando un dato no aparece en ese parte, solo se incluye si lo corroboran dos fuentes diferentes. Si un dato no puede confirmarse, ese día queda sin valor, y la línea de la gráfica une los puntos de los días que sí lo tienen.

Este sitio no está afiliado a la Unión Eléctrica ni a la Empresa Eléctrica de La Habana.

## Cómo funciona

1. Una tarea automática revisa cada día, por la tarde (hora de Cuba), el parte publicado y lo registra en una hoja de cálculo de Google.
2. La hoja está publicada en la web en formato CSV.
3. Esta página lee ese CSV cada vez que alguien la abre. Los datos nuevos aparecen sin tener que cambiar el código.

La página es un único archivo, `index.html`, sin dependencias que instalar. Usa [D3](https://d3js.org/) desde una CDN para dibujar las gráficas. Se adapta a móviles y al modo oscuro del sistema.

## Archivos

| Archivo | Contenido |
|---|---|
| `index.html` | La página completa: estructura, estilos y código. |
| `README.md` | Este archivo. |

## Actualizar la página

Para cambiar la página, sube una nueva versión de `index.html` con el mismo nombre (**Add file › Upload files › Commit changes**). GitHub Pages la publica en uno o dos minutos.
