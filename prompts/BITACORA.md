# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: Gemini

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|---|---|---|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

En el primer chat la IA respondio correctamente TiendaTec y Java Swing porque el dato estaba guardado dentro de su ventana de contexto. Al abrir un chat nuevo la ventana de contexto inicia vacia, pero debido a la memoria que tenía activada, recordó la conversación anterior y me dió todo el contexto de eso.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|---|---|---|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 67.1% | (escribe los 5 nombres que te salieron en 0.5) |
| 1 | 44.9% | (escribe los 5 nombres que te salieron en 1) |
| 1.8 | 32.2% | (escribe los 5 nombres que te salieron en 1.8) |

Al subir la temperatura las probabilidades se reparten mas entre todas las opciones, haciendo que las respuestas sean mas variadas y menos predecibles. Sin embargo, el simulador nunca inventa un nombre nuevo porque la temperatura no agrega conocimiento al modelo, solo cambia que tan arriesgado es al elegir entre las palabras que ya conoce.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona el objetivo del sistema | Si | Si |
| Menciona a los usuarios principales | No | Si |
| Tiene exactamente 3 funcionalidades | No | Si |
| Esta en 3 parrafos | No | Si |
| Lo usaria en un informe real | No | Si |

## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa en Java usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto | para gestionar los productos de una tienda |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java. |

### Evolucion por niveles

- **Nivel 1:** La IA no generó nada, solo preguntó que tipo de app necesitaba.

- **Nivel 2 (+ Rol):** Adopto un enfoque mas tecnico de programador, pero el tema del programa siguio siendo aleatorio.
- **Nivel 3 (+ Contexto):** El codigo se enfoco en gestionar productos de una tienda, aunque la IA invento los atributos.
- **Nivel 4 (+ Instruccion):** Creo exactamente la clase Producto con los cuatro atributos solicitados (codigo, nombre, precio y stock).
- **Nivel 5 (+ Formato y Ejemplo):** Ordeno la respuesta poniendo primero la explicacion de la clase, luego el codigo y respeto el estilo de nomenclatura de los metodos.