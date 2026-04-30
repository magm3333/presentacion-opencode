# Guion Oral

## Slide 01 - Portada
Presentar la charla como una demo practica de OpenCode + Plannotator centrada en el desarrollo de QRGen.

## Slide 18 - OpenCode: Plugins y Plannotator
Explicar los pasos tecnicos: instalacion de la herramienta, inicializacion con `/init` y el registro manual en `.opencode/opencode.json` usando la clave `plugin` (en singular).

## Slide 29 - Primer Prompt QRGen
Lanzar la demo real. Establecer el rol de Ingeniero Senior y el stack. Pedir especificamente las 6 fases: 
1- Estructura + Auto-deploy
2- Generación QR (MVP) "Usa el estilo y layout de magm3333.github.io/qrgen (Split-View de 2 columnas)"
3- Descarga en formatos JPG y PNG Y temas oscuro y claro
4- Editor de planillas que permita subir una imagen y solocar el qr generado automáticamente encima, poder rotarlo, moverlo y cambiarle de tamaño y descargar el resultado en SVG y PNG
5- Login/Logout
6- Ajustes y Agregados finales como exportacion de plantillas, etc
No implementes todavía.

## Slide 31 - Metodo de Demo: QRGen (Ejemplos)
Mostrar los hitos. Aclarar que estos son ejemplos de como la IA organiza el trabajo segun nuestro pedido inicial.

## Slide 32 - ¡A Crear!
Presentar la filosofia del flujo asistido: no es una linea recta aburrida, es un circulo creativo. Planeamos, anotamos como humanos, dejamos que la IA construya, validamos la App y volvemos al plan para pulir. Crear con OpenCode se siente como jugar mientras construis algo real.

## Slide 33 - OpenCode: Agnostico y Extensible
Remarcar la libertad de eleccion: no estamos atados a una empresa. OpenCode soporta los principales proveedores y permite extenderse mediante Servidores MCP y Plugins propios. 

Mencionar el "Caso Belo vs Anthropic" como un warning: aunque la herramienta es agnostica, el comportamiento de la IA puede variar drasticamente. Anthropic suele ser mas preciso en ejecucion de codigo que otros modelos (como los disponibles en Belo), por lo que elegir el motor adecuado es una decision de ingenieria.

## Slide 34 - La IA no "Piensa"
Aclaracion conceptual importante: la herramienta no tiene razonamiento consciente. Es un motor matematico que predice el siguiente paso basado en probabilidades y en el contexto que le damos. Por eso el control humano es fundamental para evitar "alucinaciones".

## Slide 35 - El Humano es el Arquitecto
La herramienta es un ejercito de robots constructores, pero el arquitecto sos vos. Si no sabes diseñar el plan y no sabes pensar la solucion, la IA solo va a construir desorden mas rapido. La potencia viene de tu criterio tecnico.

## Slide 36 - Recomendacion: Potencia vs Tarea
Tip de eficiencia: usa los modelos mas potentes (como Claude 3.5 Sonnet) para la fase de PLANIFICACION, donde hace falta mas "cerebro". Para tareas tecnicas repetitivas o implementacion de codigo estandar, podes usar modelos mas ligeros y rapidos.

## Slide 37 - Cierre
Despedida. Resaltar la eficiencia y el control. Link al repo. ¡Gracias por su atencion!
