# AIControlSistem32

IAControlSistem32 es un proyecto diseñado para gestionar dispositivos conectados a un ESP32 a través de Internet utilizando una IA como interfaz principal. Este sistema combina el poder de un microcontrolador flexible como el ESP32 con la inteligencia y versatilidad de los modelos de lenguaje de OpenAI, creando un entorno dinámico y eficiente para la automatización y el control remoto.

## Características principales

- **Control inteligente:** Maneja dispositivos conectados al ESP32 mediante comandos naturales enviados a la IA.
- **Interfaz en tiempo real:** Respuestas inmediatas y personalizadas a través de una API que integra Flask.
- **Conectividad amplia:** Acceso y control desde cualquier dispositivo conectado a Internet.

## Requisitos

- **Hardware:**
  - Un ESP32 con conexión Wi-Fi.
  - Dispositivos o actuadores conectados al ESP32.

- **Software:**
  - Python 3.9 o superior.
  - Librerías necesarias: `flask`, `openai`, `python-dotenv`.
  - Una clave API de OpenAI configurada como variable de entorno.

## Instalación

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone https://github.com/tu-usuario/AIControlSistem32.git
   cd AIControlSistem32
   ```

2. Instala las dependencias necesarias:
   ```bash
   pip install -r requirements.txt
   ```

3. Crea un archivo `.env` en la raíz del proyecto con tu clave API de OpenAI:
   ```env
   OPENAI_API_KEY=tu_clave_api
   ```

4. Ejecuta el servidor Flask:
   ```bash
   python app.py
   ```

5. Accede a la aplicación mediante Postman o cualquier cliente HTTP en la URL:
   ```
   http://127.0.0.1:5000/chat
   ```

## Uso

1. Envía una solicitud POST al endpoint `/chat` con el siguiente formato:
   ```json
   {
       "message": "Enciende la luz del salón"
   }
   ```

2. La IA procesará tu comando y responderá con instrucciones o confirmaciones específicas para el ESP32:
   ```json
   {
       "response": "La luz del salón ha sido encendida."
   }
   ```

3. Configura las tareas específicas del ESP32 para recibir los comandos y actuar en consecuencia.

## Contribuir

Si deseas contribuir a este proyecto, por favor:

1. Haz un fork del repositorio.
2. Crea una rama para tu nueva característica o mejora:
   ```bash
   git checkout -b nueva-caracteristica
   ```
3. Realiza tus cambios y súbelos a tu fork.
4. Abre un Pull Request describiendo tus modificaciones.

## Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE).
