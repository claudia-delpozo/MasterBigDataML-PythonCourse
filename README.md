# MasterBigDataML-PythonCourse
# Análisis de Salarios en Data Science

## Descripción
Este repositorio contiene un análisis de los salarios en diferentes roles dentro del campo de Data Science. Se han realizado diversas transformaciones sobre los datos originales, incluyendo la conversión de formatos, normalización y extracción de información clave.

Los datos provienen de la siguiente fuente en Kaggle:
[Employee Salaries for Different Job Roles](https://www.kaggle.com/datasets/inductiveanks/employee-salaries-for-different-job-roles)

## Estructura del Repositorio

```
MasterBigDataML-PythonCourse/
│-- ds_salaries.csv             # Datos originales
│-- ds_salaries.norm.csv        # Datos normalizados
│-- ds_salaries_pc.csv          # Datos con punto y coma como separador
│-- ds_salaries_Claudia_delPozo.ipynb  # Notebook con el análisis
│-- puestos_trabajo.py          # Script MapReduce para calcular los salarios máximos por cargo
│-- README.md                   # Descripción del proyecto
│-- images/                      # Capturas de pantalla (opcional)
```

## Transformaciones realizadas

1. **Conversión de formato**: Se transformó el archivo CSV original de comas a punto y coma como separador.
2. **Normalización**: Se eliminaron columnas irrelevantes y se codificaron variables categóricas.
3. **Análisis de frecuencia**: Se extrajo la distribución de los diferentes puestos de trabajo.
4. **MapReduce con MRJob**: Se utilizó un script de MapReduce para encontrar los salarios máximos por puesto y país.

## Ejecución del Proyecto

### Uso del Notebook
Para ejecutar el análisis en Python:
```bash
jupyter notebook ds_salaries_Claudia_delPozo.ipynb
```

### Ejecución del script MapReduce
Si tienes `mrjob` instalado, puedes ejecutar el script en local:
```bash
python puestos_trabajo.py ds_salaries_pc.csv > max_salaries.txt
```

## Ejemplo de Salida
Un ejemplo del resultado esperado tras ejecutar el script:
```bash
('Data Scientist', 'US'), 450000
('Machine Learning Engineer', 'GB'), 124333
('Data Analyst', 'IN'), 6072
```
