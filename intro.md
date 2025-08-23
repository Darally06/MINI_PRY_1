# **Predicción de prestamos DEFAULT**

Este sample book presenta la implementación de un modelo de red neuronal multicapa, el cual tiene el objetivo de predecir si un préstamo será un default o pagado en su totalidad. 

El dataset reúne los registros históricos de la empresa Lending Club. 


## **Leading Club**

Es una compañía estadounidense de préstamo entre particulares, con sede en San Francisco (California). 

Lending club permite a sus prestatarios crear listas de préstamos en su página web aportando datos de ellos mismos y de los préstamos que les gustaría obtener. Todos los préstamos son préstamos a particulares no asegurados que pueden rondar entre 1.000 y 35.000 dólares. En función de la puntuación de crédito del prestatario, el historial de crédito, de la cantidad solicitada y del ratio entre ingresos y gastos del prestatario, Lending Club determina si el prestatario es digno de confianza y asigna a los préstamos que son aprobados un grado de crédito que determina la tasas y el tipo de interés a pagar. 


## **El problema de estudio**
El objetivo es predecir si un préstamo emitido resultará en `default(1)` o `pagado(0)`. 

Se quiere identificar correctamente cuales son los prestatarios que van a incumplir con el pago de su préstamo. 

Queremos reducir el error de costo y los errores **FALSE NEGATIVE**, los casos en que se predice que NO incumplirán, pero si incumplen. Este es el error más costoso para los bancos, ya que se presta dinero a un prestatario que no va a pagar.

Para el modelo se realiza estandarización `StandardScaler` de las variables numéricas y codificación `OneHotEncoder` para las variables categóricas. 

Se dividió el dataset de datos de manera estratificada (80-20).

Aplicamos técnicas para el balanceo de clases en el conjunto de entrenamiento.

```{tableofcontents}
```
