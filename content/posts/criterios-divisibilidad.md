+++
draft = false
title = 'Criterios de Divisibilidad'
categories = ['Matemática', 'Notebook']
tags = ['Divisibilidad', 'Primos', 'Matemática']
description = 'Guía de criterios de divisibilidad'
math = true
+++

Sean $a$ y $b$ números enteros. Se dice que **$a$ es divisible entre $b$** si el residuo de $a \div b$ es cero.

> **Número primo:** solo es divisible entre sí mismo y la unidad.  
> **Número compuesto:** además es divisible entre otros números.

---
- **Divisible entre 2:** si termina en 0, 2, 4, 6 u 8.  
  *Ejemplo:* 246 termina en 6 → divisible entre 2.

- **Divisible entre 3:** si la suma de sus dígitos es múltiplo de 3.  
  *Ejemplo:* $2+7=9$ → 9 es múltiplo de 3 → 27 divisible entre 3.

- **Divisible entre 4:** si sus últimos 2 dígitos son 0 o múltiplo de 4.  
  *Ejemplo:* 3216 → “16” → $16\div4=4$.

- **Divisible entre 5:** si termina en 0 o 5.  
  *Ejemplo:* 3425 termina en 5.

- **Divisible entre 6:** si es divisible entre 2 **y** entre 3.  
  *Ejemplo:* 258 → termina en 8 (÷2) y $2+5+8=15$ (÷3).

- **Divisible entre 7:**  
  Tomar el último dígito, multiplicarlo por 2 y restarlo al resto del número.  
  *Ejemplo con 343:*  
    1. Último dígito: 3  
    2. $3\times2=6$  
    3. $34-6=28$  
    4. $28\div7=4$ → sí es divisible

- **Divisible entre 8:** si los últimos 3 dígitos son 0 o múltiplo de 8.  
  *Ejemplo:* 7432 → “432” → $432\div8=54$.

- **Divisible entre 9:** si la suma de sus dígitos es múltiplo de 9.  
  *Ejemplo:* $4+9+2+3=18$, 18 múltiplo de 9.

- **Divisible entre 10:** si termina en 0.  
  *Ejemplo:* 8250 termina en 0.

- **Divisible entre 11:**  
  Sumar dígitos en posiciones impares y pares, restar ambas sumas.  
  Si el resultado es 0 o múltiplo de 11 → divisible.  
  *Ejemplo:*  
  - 1452 → impares: $1+5=6$ → pares: $4+2=6$ → diferencia 0 → divisible.

- **Divisible entre 12:** si es divisible entre 3 **y** entre 4.  
  *Ejemplo:* 6384 → “84” ÷4 = 21 → suma $6+3+8+4=21$ → múltiplo de 3.