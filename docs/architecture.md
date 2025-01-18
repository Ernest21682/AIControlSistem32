# Arquitectura del Sistema

El sistema **AIControlSystem32** se compone de dos partes principales: un servidor Flask que maneja la lógica de control y un ESP32 que interactúa con los dispositivos físicos.

## Componentes Principales

1. **Servidor Flask**: 
   - El servidor Flask es responsable de recibir las solicitudes desde la interfaz web, procesarlas y enviar los comandos adecuados al ESP32.
   - El servidor maneja una API REST que permite interactuar con el sistema.
   - Está implementado en Python y utiliza las bibliotecas necesarias para trabajar con el ESP32.

2. **ESP32**:
   - El ESP32 es el microcontrolador que se comunica con el servidor Flask a través de Wi-Fi.
   - Recibe los comandos desde el servidor y controla los dispositivos conectados (por ejemplo, luces, ventiladores, etc.).
   - Está programado en el entorno de desarrollo de Arduino y tiene una conexión a Internet para la comunicación con el servidor Flask.

3. **Interfaz Web**:
   - La interfaz web permite a los usuarios controlar los dispositivos conectados de manera sencilla.
   - La interfaz se conecta al servidor Flask para enviar y recibir información sobre el estado de los dispositivos.
   - Está implementada con tecnologías web como HTML, CSS y JavaScript.

## Flujo del Sistema

1. **Interacción del Usuario**: El usuario interactúa con la interfaz web desde su navegador.
2. **Solicitud al Servidor**: La interfaz web envía solicitudes HTTP al servidor Flask (por ejemplo, encender un dispositivo).
3. **Comunicación entre Flask y ESP32**: El servidor Flask procesa la solicitud y transmite los comandos al ESP32 mediante una conexión de red.
4. **Control de Dispositivos**: El ESP32 recibe los comandos y controla los dispositivos físicos (por ejemplo, encender o apagar una luz).
5. **Retroalimentación al Usuario**: El estado de los dispositivos es devuelto al servidor Flask, que actualiza la interfaz web en tiempo real.

## Diagrama de Flujo

```plaintext
[Interfaz Web] <---> [Servidor Flask] <---> [ESP32] <---> [Dispositivos]
