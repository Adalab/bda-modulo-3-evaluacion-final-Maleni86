# Fase 1: Exploración y Limpieza
## Exploración Inicial:
### Analizo los datos del primer dataframe Customer Flight Activity:
- Analizo la información de las columnas, una por una, si presentan datos atípicos, negativos, nulos y/o duplicados.
- Reviso cuantos valores únicos por columnas hay.
- Exploro si tiene valores nulos y veo que no tiene ningún valor nulo.
- Encontramos que hay 1864 duplicados, por ello vamos a identificar donde se encuentran y veremos como tratarlos.
- Analizo cuales son las filas duplicadas y las reviso con sus filas originales, para verificar si existe algún patrón.
- Analizando los datos decido eliminar las filas duplicadas, ya que no me aportan ningún valor.
- Elimino las filas duplicadas, en una variable diferente y compruebo que ya no hayan duplicados.

### Analizo los datos del segundo dataframe Customer Loyalty History:

- Después de revisar una por una las columnas, sus tipos y su estadística, reviso cuantos valores únicos por columnas hay.
- Reviso si hay filas que están duplicadas en mi dataframe, y veo que no hay duplicados.
- Analizo si hay nulos, en recuento y en porcentaje por columna y veo que las columnas: Salary, Cancellation Year y Cancellation Month presentan valores nulos.
- Analizo primero los datos nulos de la columnas Salary.
- Como el salario de College debería estar entre el salario de High Schooll or Below y de Bachelor, calculamos la mediana de ambas columnas para reemplazar los valores nulos del salario de College por dicho resultado.
- Calculo la mediana entre ambas columnas y vemos que es muy similar a la media (72451) pero al ser más robusta elijo la mediana.
- Reemplazamos los datos nulos de Salary por la mediana obtenida y así ya no tenemos valores nulos en esa columna.
- Ahora analizo los valores nulos de las columnas Cancellation Year y Cancellation Month, observamos que tienen los valores nulos en las mismas filas, y por el signicado de cada una (cancelación de la membresía AÑO/MES) concluyo que los nulos son los clientes que aún tienen su membresía Activa.
- Después de este análisis decido convertir las columnas de "Cancellation Month" y "Cancellation Year" en una columna adicional al final llamada "Status", con dos variables "Activo" los NaN e "Inactivo" los que se dieron de baja en algún mes/año.
- Hago una ultima exploración para verificar como quedan mis columnas en mi nuevo df_limpio.

### Finalmente uno mis dos df limpios en un solo dataframe.
Verifico que todas mis filas y columnas se haya fusionados correctamente y paso a la siguiente fase de visualización.










