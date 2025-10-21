# Bluetooth

---
## 1) Resumen

- **Nombre del proyecto:** Bluetooth
- **Equipo / Autor(es):** Aldo Alvarez, Alexandra Groot
- **Curso / Asignatura:** Introduccion a la mecatrónica
- **Fecha:** 12/09/2025  
- **Descripción breve:** Prendido y apagado de un led a través de el uso de la funcion bluetooth de una ESP32.

---

## 2) Objetivos

- **General:** Lograr el encendido y apagado de un led utilizando comandos dados a través de bluetooth con la ayuda de una ESP32.

---

## 3) Alcance y Exclusiones

- **Incluye:** Conectar y programar el circuito de un ESP32 y un LED para el correcto control de este usando el bluetooth.

---

## 4) Requisitos

**Software**
- Arduino
- Aplicación "Serial bluetooth terminal"

**Conocimientos previos**
- _Programación básica en C++
- _Electrónica básica_

---

## 5) Desarrollo

# Electrónica

Primero se instalo la ESP32 en una protoboard y se conecto el LED a un puerto previamente determinando haciendo uso de una resistencia para el correcto funcionamiento del LED.

# Programación
Se utilizo un codigo en C++ a través de la aplicación de Arduino en el cual se activaba la funcion bluetooth de la ESP32 para despues indicar que mensaje recibido iba a encender el Led y cual lo iba a apagar.

El código fué el siguiente:

```#include "BluetoothSerial.h"
BluetoothSerial SerialBT;

#define LED 23

void setup() {
    Serial.begin(115200);
    SerialBT.begin("ESP32");
    pinMode(LED, OUTPUT);
}

void loop() {
    if (SerialBT.available()) {
        String mensaje = SerialBT.readString();
        Serial.println("Recibido: " + mensaje);
        if (mensaje == "ON") {
            digitalWrite(LED, HIGH);
        } else if (mensaje == "OFF") {
            digitalWrite(LED, LOW);
        }
    }
    delay(1000);
}
```

## 6) Resultado y evidencia

Como esperado el Led prendia y apagaba segun la instruccion dada a través del celular

[Video del funcionamiento](https://drive.google.com/file/d/1zrjvqOzj3PhVCXXpGc0IRuPjqYrYylh9/view?usp=sharing)
