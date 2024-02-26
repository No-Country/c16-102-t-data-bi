# Limpieza en la base de datos

# Tabla outcome

## Nulos
- Comenzamos observando los nulos de ambas tablas


<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/c04ec336-c620-4270-b9f3-9ebdffb885c6.jpeg" alt="Texto alternativo" width="75%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/76b0f877-c9a5-4033-86dd-4debb0725f83.jpeg" alt="Texto alternativo" width="50%">
</details>



- Detectamos que solo hay 33 nulos en la tabla outcome

- Todos los nulos pertenecen a la columna `outcome_type`

- Observamos los valores unicos de esa columna para imputar


![distinct](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/distinct%20outcome.jpg)

- Al no ser representativo para la muestra (33 de 159562) se imputara a DISPOSAL ya que no podemos asignarle una relacion logica con alguno de los otros datos de la columna

![uptadate](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update.jpeg)

- Realizamos la comprobacion de los nulos.

![compr](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Comprobacion.jpg)

## Nulos a mano
- Encontramos valores nulos pero hechos a maano (Como string y no vacios).

![mano](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/null%20a%20mano.jpg)

### Sex_upon_outcome
- Verificamos los valores de `sex_upon_outcome`

![outc](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/DISTINCT%20sex%20upon.jpg)

- Imputamos a "Desconocido" es lo mas logico.

![imp](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update%20sex%20upon.jpg)

### age_upon_outcome

- Verificamos los valores de 'age_upon_outcome'

![age](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/distinct%20age%20upon.jpg)

- Imputaremos al valor maximo para que el impacto sea el menor posible

![may](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Mayores%20age%20upon.jpg)

- Realizamos el update por 1 year

![upt](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update%20nulos%20age.jpg)


## Valores inconsistentes

- Encontramos valores inconsistentes como edades negativas que asumo que fueron por error de tipeo.

![pas](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/problema%20a%C3%B1os%20negativos.jpg)

- Procedemos a imputar/actualizar todos

  ![uno](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update%20-1years.jpg)
  ![dos](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update%20-2years.jpg)
  ![tres](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update%20-3years.jpg)
  ![cuatro](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/update-4years.jpg)
  
# Tabla intake
## Nulos Tabla intake
- Encontramos nulos en la tabla **intake**. En el mismo tipo de columnas que existian la tabla outcome.
![per](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/1.%20detecto%20null%20a%20mano%20en%20intake.jpg)

- Observamso las clumnas unicas para realizar la imputacion

![as](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/2.%20sex%20upon%20detectado.jpg)

- Es claro que imputaremos y lo encasillaremso en "Desconocido"

![imp](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/3.%20sex%20update.jpg)

- En este caso para no modificar la muestra imputarems por el valr mas comun (moda) de la edad.

![moda](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/4.ver%20valores%20ageupon.jpg)

![impu](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/5.%20update%20age%20upon.jpg)

## Unificando segmentos

- En este caso encontramos que la columna "Otros" no esta bien definida y tenemos tambien "Desconocidos" por lo que procederemos a unirlos en la segmentacion "Otros" por una cuestion de orden

![ot](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/6.%20unknown.jpg)

![xs](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/7.%20other%20up.jpg)


# Otros ajustes
