# Ejercicio 3 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Escribir en YAML la siguiente estructura de datos en JSON {uno: "dos", tres: [4, 5, "Seis", {siete: 8, nueve: [10, 11]}]}

El siguiente texto concuerda con la estructura que usa ansible en sus scripts.

```
---
uno: "dos"
tres:
  - 4
  - 5
  - "Seis"
  - siete: 8
    nueve:
      - 10
      - 11
```
