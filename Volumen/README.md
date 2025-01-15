## Potato Volume Data Exploration

In this directory, data extraction focused on departments with the highest records of potato production. Specifically, the following departments were considered:


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

Data extraction from the MIDRAGI API was conducted in the notebook VolumenDiario.ipynb, where the information was saved into two separate dataframes. This distinction was necessary because, starting in May 2020, data for the PERRICHOLI potato variety ceased to be collected.

You can load the data in the notebook LeerDatosVolumen.ipynb, where a dictionary of dataframes has been provided for convenience.

Finally, the combined potato data tables were saved in the /completas folder. Please note that the PERRICHOLI variety only includes data up to May 2020.