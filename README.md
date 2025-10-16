# clirowsheet
Una herramienta CLI hecha en Python para agregar texto automáticamente a las últimas filas de un archivo .xlsx

Una herramienta útil para llenar bitacoras o archivos en excel. Se me hace muy tedioso abrir el excel a cada rato y llenar cada linea, prefiero hacerlo desde la terminal con una sola linea y ya.

## Ejemplo

### Antes del comando
<img width="530" height="182" alt="image" src="https://github.com/user-attachments/assets/3e0baa09-27d1-48de-b420-26ed90dcffd0" />

### Despues del comando 
```bash
python main.py texto1 test python
```

<img width="523" height="207" alt="image" src="https://github.com/user-attachments/assets/b7991a19-3570-440f-ac08-61db15dea15d" />


- ### `datet` & `datey`
  Se puede usar `datet` para la fecha de hoy (datetoday)
  
  Se puede usar `datey` para la fecha de ayer (dateyesterday)

  - Ejemplo
    ```bash
    python main.py fechas datet datey
    ```
    
    <img width="520" height="150" alt="image" src="https://github.com/user-attachments/assets/28fce317-46b4-47de-96cd-edb2823b53bf" />

## Requisitos
Solamente `pip install openpyxl`

## Recomendaciones
Para hacerlo más práctico y evitar ejecutar el script con `python main.py x x x`, lo mejor es convertirlo en un comando del sistema.
Esto se logra agregando un shebang en la primera línea del archivo (sin la extension .py) y moviéndolo a /usr/local/bin/, de modo que pueda ejecutarse directamente desde la terminal como cualquier otro comando.

Agrega `#!/usr/bin/python` al inicio del archivo (Debes asegurarte que el sistema tenga instalada la libreria).
En caso que uses conda o cualquier otro entorno virtual de python como conda usa `which python` y te dara una salida como `/home/user/miniconda3/envs/my_env/bin/python`
Entonces el shebang quedaria como `#!/home/user/miniconda3/envs/my_env/bin/python`

Despues de que agregues el shebang al archivo muevelo y renombra el comando como quieras

```bash
sudo mv main /usr/local/bin/
mv main comandopro #Para cambiar el nombre del comando
```

Ahora en la terminal puedes usar
```bash
comandopro test cli datet
```







    
