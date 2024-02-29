# Limpieza en la base de datos

# Tabla outcome

## Nulos
- Comenzamos observando los nulos de ambas tablas


<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/1.%20nulos%20intake.jpeg" alt="Texto alternativo" width="70%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/2.nulo%20outcome.jpeg" alt="Texto alternativo" width="70%">
</details>



- Detectamos que solo hay 33 nulos en la tabla outcome

- Todos los nulos pertenecen a la columna `outcome_type`

- Observamos los valores unicos de esa columna para imputar

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/3.%20distinct%20outcome.jpg" alt="Texto alternativo" width="70%">
</details>


- Al no ser representativo para la muestra (33 de 159562) se imputara a DISPOSAL ya que no podemos asignarle una relacion logica con alguno de los otros datos de la columna

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/4.update%20outcome.jpeg" alt="Texto alternativo" width="70%">
</details>


- Realizamos la comprobacion de los nulos.

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/5.%20nulos%20outcome.jpg" alt="Texto alternativo" width="70%">
</details>


## Nulos a mano
- Encontramos valores nulos pero hechos a maano (Como string y no vacios).
  
<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/6.%20null%20a%20mano.jpg" alt="Texto alternativo" width="70%">
</details>


### Sex_upon_outcome
- Verificamos los valores de `sex_upon_outcome`


<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/7.%20DISTINCT%20sex%20upon.jpg" alt="Texto alternativo" width="70%">
</details>


- Imputamos a "Desconocido" es lo mas logico.

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/8.%20update%20sex%20upon.jpg" alt="Texto alternativo" width="70%">
</details>


### age_upon_outcome

- Verificamos los valores de 'age_upon_outcome'

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/9.%20Mayores%20age%20upon.jpg" alt="Texto alternativo" width="70%">
</details>

- Imputaremos al valor maximo para que el impacto sea el menor posible




- Realizamos el update por 1 year

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/10.%20update%20nulos%20age.jpg" alt="Texto alternativo" width="70%">
</details>

## Valores inconsistentes

- Encontramos valores inconsistentes como edades negativas que asumo que fueron por error de tipeo.


<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/11.%20problema%20a%C3%B1os%20negativos.jpg" alt="Texto alternativo" width="70%">
</details>


- Procedemos a imputar/actualizar todos

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/12.%20update%20-1years.jpg" alt="Texto alternativo" width="70%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/13.%20update%20-2years.jpg" alt="Texto alternativo" width="70%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/14.%20update%20-3years.jpg" alt="Texto alternativo" width="70%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/15.%20update-4years.jpg" alt="Texto alternativo" width="70%">
</details>


  
# Tabla intake
## Nulos Tabla intake
- Encontramos nulos en la tabla **intake**. En el mismo tipo de columnas que existian la tabla outcome.

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/16%20.%20detecto%20null%20a%20mano%20en%20intake.jpg" alt="Texto alternativo" width="70%">
</details>



- Observamos las clumnas unicas para realizar la imputacion

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/17.%20sex%20upon%20detectado.jpg" alt="Texto alternativo" width="70%">
</details>


- Es claro que imputaremos y lo encasillamos en "Desconocido"
  
<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/18.%20sex%20update.jpg" alt="Texto alternativo" width="70%">
</details>


- En este caso para no modificar la muestra imputarems por el valr mas comun (moda) de la edad.

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/19.ver%20valores%20ageupon.jpg" alt="Texto alternativo" width="70%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/20.%20update%20age%20upon.jpg" alt="Texto alternativo" width="70%">
</details>

## Unificando segmentos

- En este caso encontramos que la columna "Otros" no esta bien definida y tenemos tambien "Desconocidos" por lo que procederemos a unirlos en la segmentacion "Otros" por una cuestion de orden

<details>
  <summary>Ver imagen</summary>
  
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/21.%20unknown.jpg" alt="Texto alternativo" width="70%">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/blob/facu/Imagenes/22.%20other%20up.jpg" alt="Texto alternativo" width="70%">
</details>


