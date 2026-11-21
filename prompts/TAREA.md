# Tarea: Mi prompt profesional

## Funcionalidad elegida

Calculadora de promedio final ponderado de notas en consola (Java) para docentes, que evalua si un estudiante aprueba o desaprueba un curso.

## Version 1: prompt basico

```text
Haz un programa en Java para calcular notas.
```
Que cambie: Es el pedido inicial desde cero, corto y sin detalles.

Por qué: Para observar como responde la IA cuando no tiene contexto ni reglas definidas.

Que mejoro en la respuesta: Genero un codigo base funcional, pero invento la cantidad de notas, los pesos y el formato de salida.

## Version 2: prompt normal

```
Actua como desarrollador Java. Crea un programa en consola para calcular el promedio ponderado de 3 notas de un estudiante (Practica 1 con 30%, Practica 2 con 30% y Examen Final con 40%) e indicar si aprobo (promedio mayor o igual a 13).
```

Que cambie: Agregue el rol de desarrollador Java, el contexto academico (3 notas con sus porcentajes) y la regla de aprobacion (>= 13).

Por que: En la version 1 la IA hacia un promedio simple en lugar de ponderado y no sabia la nota minima aprobatoria.

Que mejoro en la respuesta: La logica matematica del calculo ponderado y la condicion de aprobacion salieron exactas.

## Version 3: prompt final

```
Actua como desarrollador senior de Java. Estoy creando una herramienta academica para que los docentes calculen el promedio final de un estudiante en consola. Escribe un programa en Java que pida por teclado el nombre del alumno y 3 notas (Practica 1 con peso 30%, Practica 2 con peso 30% y Examen Final con 40%), calcule el promedio ponderado e indique si esta Aprobado (promedio >= 13) o Desaprobado. Restriccion: no uses librerias externas ni arreglos, solo la clase Scanner y variables primitivas. Usa este formato para la salida en consola: "Alumno: Juan Perez | Promedio: 14.5 | Estado: Aprobado". Explica brevemente la formula aplicada en 2 lineas y luego muestra el codigo Java completo y comentado.
```

Que cambie: Incorpore una restriccion tecnica (sin arreglos ni librerias externas), un ejemplo exacto de salida en consola y el formato de entrega (explicacion de 2 lineas + codigo comentado).

Por que: Faltaba controlar la complejidad del codigo y estandarizar como se imprime el resultado al usuario.

Que mejoro en la respuesta: Entrego una explicacion concisa, codigo limpio sin estructuras innecesarias y la salida formateada tal como se pidio.

## Componentes del promt final

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actua como desarrollador senior de Java. |
| Instruccion | Escribe un programa en Java que pida por teclado el nombre del alumno y 3 notas (...), calcule el promedio ponderado e indique si esta Aprobado o Desaprobado. Restriccion: no uses librerias externas ni arreglos, solo la clase Scanner y variables primitivas. |
| Contexto | Estoy creando una herramienta academica para que los docentes calculen el promedio final de un estudiante en consola. |
| Ejemplo | Usa este formato para la salida en consola: "Alumno: Juan Perez" |
| Formato | Explica brevemente la formula aplicada en 2 lineas y luego muestra el codigo Java completo y comentado. |

## Evaluación de resultado

| Criterio | Cumple |
|---|---|
| Calcula el promedio ponderado con los pesos exactos (30%, 30%, 40%) | Si |
| Respeta la restriccion de usar solo Scanner y variables primitivas | Si |
| Imprime la salida exactamente igual al ejemplo proporcionado | Si |
| Incluye la explicacion de 2 lineas antes del codigo comentado | Si |

## Errores que evite

1. Ser demasiado general: En la version 1 el pedido era muy abierto; lo evite detallando exactamente las 3 evaluaciones, sus porcentajes y la nota minima aprobatoria (13).

2. No indicar el formato: Para evitar respuestas desordenadas o textos muy largos, especifique que la explicacion debia tener maximo 2 lineas y di un ejemplo literal de como imprimir la salida en consola.