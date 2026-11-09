# laboratorio: código seguro y modelo owasp

## 1. datos generales

- **nombre completo:** viana pamela galdamez gonzalez
- **carnet:** n/a
- **correo electrónico:** vianagaldamez01@gmail.com
- **asignatura:** lenguajes de programación con aspectos de seguridad
- **técnico:** tsu en ciberseguridad
- **tutor:** dámaris alas
- **periodo de realización:** del 02 al 08 de noviembre de 2026

## 2. descripción del proyecto

Este laboratorio consiste en desarrollar una aplicación web utilizando Python, implementando controles básicos de seguridad basados en buenas prácticas y el modelo OWASP.

Se aplican mecanismos de validación de entradas, consultas parametrizadas, protección de contraseñas, registro de eventos de autenticación y detección de incidentes de seguridad.

Además, se implementa un detector de intentos fallidos de inicio de sesión que genera alertas de seguridad y registra una acción simulada de bloqueo de usuario en el archivo `respuesta.log`.

Se calculan las métricas **MTTD (Mean Time to Detect)** y **MTTR (Mean Time to Respond)** para evaluar los tiempos de detección y respuesta ante los incidentes.

## 3. estructura del proyecto

```text
laboratorio-las/
│
├── templates/
│   ├── login.html
│   └── registro.html
│
├── app.py
├── crearDB.py
├── detector.py
├── eventos.log
├── respuesta.log
├── usuarios.db
├── requirements.txt
└── README.md
```

## 4. ejecución del proyecto

### paso 1. clonar el repositorio

```bash
git clone https://github.com/Vianix2026/laboratorio-las.git
```

### paso 2. ingresar al directorio del proyecto

```bash
cd laboratorio-las
```

### paso 3. crear y activar el entorno virtual

```bash
python3 -m venv venv
source venv/bin/activate
```

### paso 4. instalar las dependencias

```bash
pip install -r requirements.txt
```

### paso 5. inicializar la base de datos

```bash
python3 crearDB.py
```

### paso 6. ejecutar la aplicación web

```bash
python3 app.py
```

La aplicación estará disponible en el navegador en:

```text
http://127.0.0.1:5000
```

## 5. detección de incidentes de seguridad

Para realizar las pruebas de detección:

1. Ejecutar la aplicación web.
2. Realizar al menos tres intentos fallidos de inicio de sesión desde la aplicación.
3. Repetir el procedimiento para tres escenarios diferentes.
4. Ejecutar el detector de seguridad desde una segunda terminal:

```bash
python3 detector.py
```

5. Verificar las alertas generadas en la terminal.
6. Revisar el archivo `respuesta.log` para verificar el registro de la acción simulada de bloqueo de usuario.

## 6. métricas de seguridad

### MTTD — tiempo medio de detección

Representa el tiempo transcurrido desde el primer intento fallido hasta la detección del incidente.

```text
MTTD = fecha de detección - fecha del primer intento
```

### MTTR — tiempo medio de respuesta

Representa el tiempo transcurrido desde la detección del incidente hasta la respuesta aplicada.

```text
MTTR = fecha de respuesta - fecha de detección
```

### cálculo de los promedios

```text
MTTD promedio = suma de los MTTD / cantidad de pruebas

MTTR promedio = suma de los MTTR / cantidad de pruebas
```

## 7. tecnologías utilizadas

- Python
- Flask
- SQLite
- HTML
- Git
- GitHub
- Visual Studio Code
- WSL Ubuntu

## 8. repositorio

Repositorio del proyecto:

https://github.com/Vianix2026/laboratorio-las.git
