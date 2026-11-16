# Ordenar tres números (de menor a mayor)

Algoritmo en PSeInt que recibe 3 números reales y los ordena de menor a mayor, mostrando paso a paso cada comparación y cada intercambio. Funciona también cuando hay números iguales.

## Trabajo en grupo

Este algoritmo se desarrolló en grupo, durante la clase, entre:

- Christian Camilo Benitez Gomez
- Jose Daniel Pabon Villanueva
- Juan Pablo Aparicio Rojas
- Oscar David Zapata Ossa

Por eso los algoritmos de los integrantes del grupo son muy parecidos entre sí.

## Versiones

Se hicieron dos versiones del mismo algoritmo, ambas basadas en el método de la burbuja:

| Versión | Archivo | Idea |
| --- | --- | --- |
| Ciclos y arreglo | `OrdenarTresNumeros_ciclos.psc` | Guarda los números en un arreglo de 3 posiciones y usa un `Para` dentro de otro `Para`. |
| Condicionales | `OrdenarTresNumeros_condicionales.psc` | Usa tres variables (`a`, `b`, `c`) y `Si` consecutivos, sin ciclos. |

## Cómo funciona

1. Se leen los tres números.
2. **Pasada 1:** se compara la posición 1 con la 2 y la 2 con la 3. Si el de la izquierda es mayor, se intercambian. Al final de esta pasada, el mayor queda en la última posición.
3. **Pasada 2:** se compara otra vez la posición 1 con la 2.
4. Se muestra el resultado final.

Para 3 números bastan 2 pasadas.

## Números iguales

La comparación usa `>` (estrictamente mayor), no `>=`. Si dos números son iguales no se intercambian: el algoritmo solo lo informa como "ya están en orden" y sigue. Así no hace intercambios innecesarios y el resultado es correcto.

## Pruebas de escritorio

| Entrada | Pasada 1 | Pasada 2 | Resultado |
| --- | --- | --- | --- |
| 3, 1, 2 | [1, 3, 2] → [1, 2, 3] | ya en orden | [1, 2, 3] |
| 1, 2, 3 | ya en orden, ya en orden | ya en orden | [1, 2, 3] |
| 2, 2, 1 | ya en orden → [2, 1, 2] | [1, 2, 2] | [1, 2, 2] |
| 4, 4, 4 | ya en orden, ya en orden | ya en orden | [4, 4, 4] |
