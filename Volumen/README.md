## Exploración de datos de volumen por papa


En presente directorio se procedió a extraer datos de los departamentos con mayor cantidad de registros de papa, en específico las siguientes:


``` py
departamentos = [
    {"name": "Apurimac", "code": "030000"},
    {"name": "Arequipa", "code": "040000"},
    {"name": "Ayacucho", "code": "050000"},
    {"name": "Huancavelica", "code": "090000"},
    {"name": "Huánuco", "code": "100000"},
    {"name": "Ica", "code": "110000"},
    {"name": "Junín", "code": "120000"},
    {"name": "La Libertad", "code": "130000"},
    {"name": "Lima", "code": "150000"},
    {"name": "Pasco", "code": "190000"}
]
```

La extracción de datos de la API del MIDRAGI se realizó en el notebook `VolumenDiario.ipynb`, donde se guardaron los datos en dos dataframes, diferentes pues a partir de mayo de 2020, se dejó de extraer datos de la papa PERRICHOLI. 


La lectura la puede realizar en el notebook `LeerDatosVolumen.ipynb` donde coloqué un diccionario de dataframes.


Al final en la carpeta `/completas` se guardaron las tablas con las papas ya unidas, recordar que perricholi solo tiene datos hasta mayor de 2020.