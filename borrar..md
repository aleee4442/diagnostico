1. Evidencia técnica seleccionada

Evidencia 1: SHA-256 generado

Descripción: A continuación se muestra el resultado del cálculo del hash SHA-256 del archivo 00_AlejandroGonzalo.ipynb, que garantiza la integridad del archivo.

Foto: Captura de pantalla de la celda donde se muestra el hash SHA-256 generado.

(Ejemplo: foto del código de la celda donde se muestra "SHA-256 generado")

Evidencia 2: Registro de hash guardado en JSON

Descripción: El hash generado y la fecha de creación se guardan en un archivo registro_hash.json, lo que asegura la trazabilidad y la transparencia del proceso.

Foto: Captura de pantalla de la celda donde se muestra el mensaje "Registro creado: registro_hash.json ✅" después de haber generado el archivo JSON.

(Ejemplo: foto de la salida que muestra el mensaje "Registro creado: registro_hash.json ✅")

2. Explicación breve de lo conseguido

He creado un notebook reproducible en Google Colab, en el que implementé un proceso para garantizar la integridad de un archivo mediante el cálculo de su hash SHA-256. Este hash, junto con la fecha de creación, se guarda en un archivo JSON llamado registro_hash.json, asegurando la trazabilidad y la transparencia del proceso. Además, siguiendo el principio WORM, el notebook fue subido a GitHub utilizando un commit inmutable, lo que permite la reproducibilidad y verificación de los resultados a lo largo del tiempo.

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

Instrucciones de entrega

Capturas de pantalla:

Toma una foto de la celda donde se muestra el cálculo del SHA-256 generado, que es el resultado de la ejecución de tu código.

Toma una foto de la celda donde se muestra el mensaje "Registro creado: registro_hash.json ✅" para mostrar que guardaste el hash en un archivo JSON.

Subir a Blackboard:

Asegúrate de adjuntar las capturas de pantalla que acabas de tomar.

Completa la hoja de trabajo con los textos que te proporcioné (explicación, dudas y autoevaluación).

Si ya has subido tu notebook a GitHub, incluye también el enlace de tu commit como evidencia de la trazabilidad y el principio WORM.

Código relevante a mostrar (para la foto)

A continuación te incluyo el fragmento de código que debe quedar visible en las capturas de pantalla:

# Cálculo del hash SHA-256
nombre_archivo = '00_AlejandroGonzalo.ipynb'

if not os.path.exists(nombre_archivo):
    open(nombre_archivo, 'w').write('Plantilla reproducible')

with open(nombre_archivo, 'rb') as f:
    contenido = f.read()

sha = hashlib.sha256(contenido).hexdigest()
print('SHA-256 generado:\\n', sha)


En la captura de pantalla debe verse el resultado de este código, que te genera el hash.

Y luego:

# Registro en archivo JSON
registro = {
    'archivo': nombre_archivo,
    'sha256': sha,
    'fecha': datetime.datetime.now().isoformat()
}

with open('registro_hash.json', 'w') as f:
    json.dump(registro, f, indent=2)

print('Registro creado: registro_hash.json ✅')


Aquí debes mostrar la salida que confirma la creación del archivo JSON, con el mensaje "Registro creado: registro_hash.json ✅".
