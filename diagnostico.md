# 1. Evidencia técnica seleccionada

Evidencia 1: SHA-256 generado

Descripción: A continuación se muestra el resultado del cálculo del hash SHA-256 del archivo 00_AlejandroGonzalo.ipynb, que garantiza la integridad del archivo.

<img width="730" height="243" alt="image" src="https://github.com/user-attachments/assets/9d545ab5-3669-4e33-9121-ec357b667a6f" />

Evidencia 2: Registro de hash guardado en JSON

Descripción: El hash generado y la fecha de creación se guardan en un archivo registro_hash.json, lo que asegura la trazabilidad y la transparencia del proceso.

<img width="735" height="226" alt="image" src="https://github.com/user-attachments/assets/59326d3c-e1ca-4b5a-8143-0463bf0be25d" />

2. Explicación breve de lo conseguido

He creado un notebook reproducible en notebook, en el que implementé un proceso para garantizar la integridad de un archivo mediante el cálculo de su hash SHA-256. Este hash, junto con la fecha de creación, se guarda en un archivo JSON llamado registro_hash.json, asegurando la trazabilidad y la transparencia del proceso. Además, siguiendo el principio WORM, el notebook fue subido a GitHub utilizando un commit inmutable, lo que permite la reproducibilidad y verificación de los resultados a lo largo del tiempo.

3. Duda principal pendiente

Mi principal duda fue sobre cómo manejar posibles cambios en las versiones de las librerías y entornos de ejecución. Si alguna librería cambia o se actualiza, ¿cómo puedo asegurarme de que mi notebook siga siendo completamente reproducible? ¿Existen mejores prácticas para gestionar las dependencias a largo plazo sin perder la trazabilidad?

4. Autoevaluación rápida

Exactitud: 2
El cálculo del hash fue realizado correctamente y el archivo de registro se creó sin errores.

Explicabilidad: 2
El proceso está documentado adecuadamente. Cada celda de código tiene su explicación correspondiente en Markdown.

Economía: 2
El código es eficiente y limpio. No hay redundancias ni procesos innecesarios.

Comentario adicional:
El proceso de trazabilidad y control de versiones ha sido realizado correctamente. Sin embargo, sigo teniendo dudas sobre cómo manejar las versiones de las librerías para garantizar la reproducción exacta del entorno en el futuro.
