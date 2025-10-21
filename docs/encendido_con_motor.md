# Encendido con botón
---

## 1) Resumen

- **Nombre del proyecto:** Encendido con botón
- **Equipo / Autor(es):** Aldo Alvarez, Alexandra Groot  
- **Curso / Asignatura:** Introducción a la mecatrónica
- **Fecha:** 12/09/25
- **Descripción breve:** Encendido de un Led con ayuda de un botón y una ESP32

---

## 2) Objetivos

- **General:** Con la ayuda de una ESP32 se planea lograr el encendido de un LED al mantener un botón presionado y al dejarlo de presionar que este se apague.

---
## 3) Alcance y Exclusiones

- **Incluye:** Un LED el cual al presionar el botón se prenda

---

## 4) Requisitos

**Software**
- Arduino

**Hardware (si aplica)**
- Botón
-Multimetro

**Conocimientos previos**
- _Programación básica en C++_
- _Electrónica básica_

---

## 5) Desarrollo

# Electrónica

Primero se conecto una placa ESP32 a una protoboard, después se instalo un botón y a este se conecto un LED tomando el puerto especificado y utilizando resistencias para el correcto funcionamiento de este

# Programación

El programa que se hizo en C++ tiene el objetivo de que al recibir la señal de que el botón esta presionado encienda el LED, de lo contrario el LED permanece apagado

El codigo utilizado fué el suiguiente:

```
#define LED 23
#define BUTTON 33

void setup() {
    pinMode(LED, OUTPUT);
    pinMode(BUTTON, INPUT);
}

void loop() {
    if (digitalRead(BUTTON) == HIGH) {
        digitalWrite(LED, HIGH);
    } else {
        digitalWrite(LED, LOW);
    }
}
```

---
## 6) Resultado y evidencia

El resultado fué el esperado logrando de que el LED prendiera exclusivamente cuando el boton estuviera precionado y apagada en el caso contrario

[Video del funcionamiento](https://drive.google.com/file/d/1y4MCiTSNBavNAfkrnyJipjh7j5Zh8KXm/view?usp=sharing)
