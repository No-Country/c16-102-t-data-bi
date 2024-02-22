# Bienvenid@s a Cat & Perry, Prediciendo Sonrisas 


  
<p align="center">
  <img src="https://github.com/No-Country/c16-102-t-data-bi/assets/159388590/f27af524-c140-427d-a1c2-09ee79bdd6d9" alt="Cat Perry">
</p>



*Este proyecto tiene como objetivo a traves de los datos mejorar las condiciones de adopcion de los animales, para esto aplicaremos analisis de datos y Machine Learning.*

## Equipo :man: :woman: :man: :woman:  :woman: 

**Miranda Lucas [@x3naroth](https://www.github.com/x3naroth):**

- [ETL](https://github.com/No-Country/c16-102-t-data-bi/blob/main/Connect_and_populate.ipynb)

- Aprendizaje automático: En desarrollo
  

- [@octokatherine](https://www.github.com/octokatherine)

  
**Castillo Dora  [@Docasti](https://www.github.com/docasti):**

- [Analista de datos](https://github.com/No-Country/c16-102-t-data-bi/blob/limpieza-datos/intakes_outcomes_1.ipynb)
  
- [Extracción y Transformación de Datos](https://github.com/No-Country/c16-102-t-data-bi/blob/limpieza-datos/limpiezaML.ipynb)

**Ariza Laura [@laura-ariza](https://www.github.com/laura-ariza):**

- Analista de datos

- Analista BI

**Tapia Estefanía [@TefiTapia](https://www.github.com/TefiTapia):**
- Analista de datos
- Analista BI
  
**Facundo Cuello [@facu-cuello](https://www.github.com/facu-cuello):**

- Analista de datos
- ETL
- Machine Learning


## :pencil: Acerca del proyecto :pencil:

Este proyecto tiene como objetivo utilizar el poder de los datos para aumentar las tasas de adopción de animales en refugios. Para ello, se implementarán diversas técnicas de análisis de datos y Machine Learning.

El objetivo del proyecto es el "Análisis de Adopciones y Abandono de Mascotas" es desarrollar un dasboard que permita al equipo de adopción del refugio de animales gestionar de manera eficiente el proceso de adopción y seguimiento de mascotas.

Este dashboard diseñado deberá abordar las necesidades y requerimientos identificados en las user stories confeccionadas en la etapa inicial. [LINK](https://github.com/No-Country/c16-102-t-data-bi/blob/limpieza-datos/userstories.rtf).

Al abordar estos aspectos, el dashboard logrará su objetivo de proporcionar al equipo de adopción del refugio de animales una herramienta efectiva para gestionar el proceso de adopción y seguimiento de mascotas, mejorando así la eficiencia y la experiencia tanto para el equipo como para los adoptantes potenciales.

## 🛠 Herramientas utilizadas 🛠
En este proyecto, hemos utilizado las siguientes tecnologías:

- **SQL**:
  - ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)  

- **Limpieza tansformacion, Analisis y exploracion de datos Python**:
  - ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

- **Machine Learning**:
  - ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
  - ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
  - ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
  - ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
  - ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
 

- **Organización**:
   - ![Trello](https://img.shields.io/badge/Trello-%23026AA7.svg?style=for-the-badge&logo=Trello&logoColor=white)
   - ![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)
   - ![Discord](https://img.shields.io/badge/Discord-%235865F2.svg?style=for-the-badge&logo=discord&logoColor=white)
     
     
## :mailbox: Contacto :mailbox:
![Ln](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)
![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)
![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)
![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)


<img src="https://static-00.iconduck.com/assets.00/linkedin-original-icon-256x256-bckcotyp.png" width="32">
<img src="https://static-00.iconduck.com/assets.00/linkedin-original-icon-256x256-bckcotyp.png" width="32">
<img src="https://static-00.iconduck.com/assets.00/linkedin-original-icon-256x256-bckcotyp.png" width="32">
<img src="https://static-00.iconduck.com/assets.00/linkedin-original-icon-256x256-bckcotyp.png" width="32">
<img src="https://static-00.iconduck.com/assets.00/linkedin-original-icon-256x256-bckcotyp.png" width="32">
------------------------------------------------


# Limpieza datos

## Nulos
- Comenzamos observando los nulos de ambas tablas
![Tabla2](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/c04ec336-c620-4270-b9f3-9ebdffb885c6.jpeg)

![Tabla1](https://github.com/No-Country/c16-102-t-data-bi/blob/facu/76b0f877-c9a5-4033-86dd-4debb0725f83.jpeg)

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



<!--
**facu-cuello/facu-cuello** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
