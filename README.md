# **sales-predictions**


## Descripción
En este repositorio se desarolla un proyecto de predicción de ventas. El objetivo es ayudar al distribuidor comprender las propiedades de los productos y los puntos de venta que desempeñan un papel crucial en la predicción de los ingresos en base a datos históricos proporcionados por el distribuidor. Se realizá el analisis de datos, limpieza y se ejecutan modelos de aprendizaje automático(regresión lineal y árbol de regresión) para encontrar el mejor modelo que permita al distribuidor predecir su nivel de venta.

## Datos

#### Matriz de Correlación
![Matriz de correlación](https://user-images.githubusercontent.com/125110281/228056617-2df35b75-fabe-447d-9bdd-b4c6dea4e5d7.png)


Una vista a nuestra matriz de correlación nos muestra que el "Item_MRP", precio máximo de venta al público, es la variable con mayor correlación positiva con la variable de ventas. Es decir, la que tiene un mayor efecto en el comportamiento de las ventas. El resto de predictores tienen correlaciones débiles.

#### Distribución de ventas por tipo de tienda
![Conteo de ventas](https://user-images.githubusercontent.com/125110281/228056586-ded33778-aed0-46be-aabb-6f0b4ec3e21b.png)
Mediante esta distribucion se puede evidenciar que en la "Grosery Store" tenemos muchas más ventas de valores pequeños, es decir, se realizan muchas compras pero generalmente la factura final tiene un precio bajo. Por otra parte, "Supermarket Type 1" es la que mayor venta tiene y además es la que por cada venta factura valores más alto en comparación a las otras tiendas. 

#### Distribución de ingresos por tipo de tienda

<img width="750" alt="750" src="https://user-images.githubusercontent.com/125110281/228057291-c6f88049-241c-4dc4-a740-7b0cbb017738.png">

<img width="51" alt="Screen Shot 2023-03-29 at 10 33 13 AM" src="https://user-images.githubusercontent.com/125110281/228626496-a0b43ab5-95c0-4962-b2ae-df6a12046a1f.png">
0: Grosery Store
1:Supermarket Type 1
2:Supermarket Type 2
3:Supermarket Type 3

La distribución de ingresos por tipo de tienda nos muestra que aproximadamente el 70% de los ingresos vienen de las tiendas "Supermarket Type 1". Les sigue "Supermarket Type 3" con el 19%. La "Grosery Store" es la que menor ingreso genera con solo el 1.98% de los ingresos.

#### Productos vendidos
<img width="750" alt="600" src="https://user-images.githubusercontent.com/125110281/228057949-c5f2a5aa-4f41-416b-af24-178e1288af50.png">

En cuanto a los tipos de producto vendidos, podemos encontrar que las frutas y vegetales, junto con los Snacks son las categorías mas vendidas. Los mariscos por otra parte son la categoria menos vendida.

## Resultados

Para la predicción de ventas se realizó dos modelos de aprendizaje automático, en donde se obtuvo los siguientes resultados:

### Regresion lineal
* R^2 Train: 0.51
* R^2 Test: 0.5
* RMSE Error Train: 1208.86
* RMSE Error Test: 1168.7

### Árbol de regresion
* R^2 Train: 0.6
* R^2 Test: 0.59
* RMSE Error Train: 1082.65
* RMSE Error Test: 1057.44

## Conclusiones
Se pudo evidenciar que el precio de venta al público es determinante para las ventas de los diferentes productos. Adicionalmente, los supermercados son las tiendas que más ingresos generan. Se debe dar enfoque a esas plazas si se quiere incrementar las ventas.
Se recomienda usar el modelo de árbol de regresión debido a su capacidad de ajustar el modelo de predicción a los datos reales y los de prueba. Logró obtener un R^2 mayor, por lo que explica mejor el comportamiento de los datos, y obtuvo un error de predicción menor que la regresión lineal. Es decir, si se quiere predecir los valores de venta, el modelo generado por árboles de regresión, nos brindara una predicción mas exacta.


