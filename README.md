# README - Transformación de Datos en Power BI

## Descripción

Se realizó la transformación de un archivo de Excel utilizando Power Query en Power BI Desktop con el objetivo de limpiar, normalizar y preparar los datos para su análisis.

---

## Transformaciones realizadas

Las transformaciones se realizaron en el siguiente orden:

1. Se importó el archivo Excel a Power BI Desktop.
2. Se renombraron las columnas utilizando nombres descriptivos en formato **snake_case**.
3. Se corrigieron los tipos de datos de cada columna.
4. Se reemplazaron los valores de texto **"NULL"** por valores nulos (`null`).
5. Se eliminaron registros duplicados en la tabla de productos.
6. Se normalizó la estructura separando la información en dos tablas:
   - Producto
   - Ubicación

---

## Tipos de datos utilizados

Se asignó el tipo de dato adecuado a cada columna según su contenido.

| Columna | Tipo de dato |
|---------|--------------|
| id_producto | Número entero |
| product_name | Texto |
| color | Texto |
| stock_recomendado | Número entero |
| punto_reposicion | Número entero |
| costo | Moneda |
| precio | Moneda |
| dias_fabricacion | Número entero |
| fecha_inicio_venta | Fecha |
| fecha_fin_venta | Fecha |
| categoria | Texto |
| subcategoria | Texto |
| id_ubicacion | Número entero |
| ubicacion | Texto |

La asignación de estos tipos permite realizar cálculos, filtros y análisis correctamente dentro de Power BI.
<img width="2720" height="1538" alt="image" src="https://github.com/user-attachments/assets/2b617aae-d980-4c2e-8ce1-93c5e60b38d5" />

---

## Tratamiento de valores nulos y duplicados

Las columnas contenían el texto **"NULL"**, el cual impedía convertir correctamente algunos campos al tipo de dato correspondiente.

Para resolver este problema, se reemplazó el texto **"NULL"** por valores nulos (`null`) mediante la opción **Reemplazar valores** de Power Query.

Posteriormente se modificaron los tipos de datos de las columnas de fecha.

En cuanto a los registros duplicados, se verificó la información y se eliminaron los duplicados de la tabla **Producto**, manteniendo un único registro por **id_producto**.

La tabla **Ubicación** no fue depurada por duplicados ya que un mismo producto puede encontrarse almacenado en distintas ubicaciones, por lo que esos registros representan información válida.

---

## Normalización de datos

Se dividió la información en dos consultas independientes para evitar redundancia y facilitar el modelo de datos.

### Tabla Producto

Contiene la información propia de cada producto:

- id_producto
- product_name
- color
- stock_recomendado
- punto_reposicion
- costo
- precio
- dias_fabricacion
- fecha_inicio_venta
- fecha_fin_venta
- categoria
- subcategoria

### Tabla Ubicación

Contiene la información de almacenamiento de cada producto:

- id_producto
- id_ubicacion
- ubicacion

Ambas tablas se relacionan mediante la columna **id_producto**, permitiendo mantener un modelo de datos normalizado y evitando la duplicación de información.
<img width="2692" height="1588" alt="image" src="https://github.com/user-attachments/assets/af8c9cc0-9e85-4457-bc0e-698602df1224" />

---

## Resultado

Al finalizar las transformaciones:

- El archivo se carga correctamente en Power BI Desktop.
- Las columnas poseen nombres descriptivos.
- Los tipos de datos son correctos.
- Los valores nulos fueron tratados adecuadamente.
- La información quedó organizada en dos tablas relacionadas, facilitando el análisis y la creación de visualizaciones.# README - Transformación de Datos en Power BI

-<img width="2864" height="1618" alt="image" src="https://github.com/user-attachments/assets/0a97b7a3-8163-4edb-b714-32acbb4b2d66" />
<img width="1354" height="872" alt="image" src="https://github.com/user-attachments/assets/b1f4dd33-893e-49c4-a5a0-d96cccecb2e5" />



