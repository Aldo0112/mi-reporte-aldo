# Control de un motor

---

## 1) Resumen

- **Nombre del proyecto:** Control de un motor 
- **Equipo / Autor(es):** Aldo Alvarez, Alexandra Groot
- **Curso / Asignatura:** Introducción a la mecatrónica
- **Fecha:** 19/19/25
- **Descripción breve:** Lograr que un motor gire por un tiempo determinado

---

## 2) Objetivos

- **General:** Con la ayuda de una ESP32 y un puente H lograr el movimiento de un motor por un tiempo determinado en la programación hecha en Arduino con lenguaje C++.

---
## 3) Alcance y Exclusiones

- **Incluye:** EL movimiento de un motor por el tiempo predeterminado en la programación y que después gire al lado contrario.

---

## 4) Requisitos

**Software**
- _Arduino_

**Hardware**
- _Fuente de poder_
- _Multimetro_

**Conocimientos previos**
- _Programación básica en C++_
- _Electrónica básica_

---

## 5) Desarrollo

# Electrónica

Primero se instalo la placa ESP32 a un arduino la cual era alimentada a través de la conexión a la computadora, después se conectaron los puertos que ibamos a usar de la ESP32 al puente H, luego conectamos el motor a el puente H según corresponde y finalmente se alimento el puente H con la ayuda de una fuente de poder.

# Programación

La programación esta hecha para que el motor gire durante un tiempo determinado hacia una dirección, después se detenga, gire a la dirección opuesta durante un tiempo determinado, se detenga y continue el ciclo.

El codigo utilizado fué el siguiente:

```
#define in1 27
#define in2 14

void setup() {
  /*Declarar Pines Como salida*/
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
}

void loop() {
  /*ADELANTE*/
  digitalWrite(in1, 0);
  digitalWrite(in2, 1);
  delay(1000);
  /*ALTO*/
  digitalWrite(in1, 0);
  digitalWrite(in2, 0);
  delay(1000);
  /*ATRAS*/
  digitalWrite(in1, 1);
  digitalWrite(in2, 0);
  delay(1000);
  /*ALTO*/
  digitalWrite(in1, 0);
  digitalWrite(in2, 0);
  delay(1000);
}
```

---
## 6) Resultado y evidencias

El resultado fué el esperado logrando que el motor suguiera las instrucciones en la programación

[Foto de las conexiones](https://drive.google.com/file/d/1ZfiblPK5CeDVj72NPW2BG-Izp5TSbGYC/view?usp=sharing)

[Video del funcionamiento](https://drive.google.com/file/d/1uku9kFjUkLhdnCgV8f6ZGa-J4uivBzcc/view?usp=sharing)
