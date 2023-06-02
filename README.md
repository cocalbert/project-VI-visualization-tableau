# project-VI-visualization-tableau
import pandas as pd

df1 = pd.read_csv('airbnb_nyc_clean.csv.csv')
df2 = pd.read_csv('AB_NYC_2019.csv.csv')

# Realizar el "join" utilizando la función merge de pandas
# Especifica las columnas en las que quieres hacer el "join"
df_merged = pd.merge(df1, df2, on='name')

# Guardar el resultado en un nuevo archivo CSV
df_merged.to_csv('archivo_merged.csv', index=False)

