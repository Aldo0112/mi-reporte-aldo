# Control servomotor

---

## 1) Resumen

- **Nombre del proyecto:** Control servomotor  
- **Equipo / Autor(es):** Aldo Alvarez, Alexandra Groot
- **Curso / Asignatura:** Introducción a la mecatrónica
- **Fecha:** 26/09/25  
- **Descripción breve:** Controlar el movimiento de un servomotor para que vaya girando en un mayor ángulo cada vez.

---

## 2) Objetivos

- **General:** Lograr que un servomotor vaya aumentando el tamaño de su giro de 10 en 10 grados empezando en 10 y terminando en 180 para después volver a empezar el programa con la ayuda de una ESP32 y programado en Arduino

---

## 3) Alcance y Exclusiones

- **Incluye:** Un servomotor el cual vaya girando cada vez más progresivamente
---

## 4) Requisitos

**Software**
- _Arduino_

**Hardware (si aplica)**
- _Fuente de poder_
- _Multimetro_

**Conocimientos previos**
- _Programación básica en C++_
- _Electrónica básica_

---

## 5) Dearrollo

# Electrónica 

Primero se conecto a una protoboard una placa ESP32 la cual estaba alimentada con la conexion a la computadora, después se conecto el servomotor tanto a un pwm en la placa para controlar su movimiento como a una fuente de poder la cual alimentaba a este.

# Programación

La programación estaba hecha con el objetivo de que mientras los grados de rotación del servomotor fueran menores a 180 este iba a aumentar su giro en 10 grados cada vez hasta llegar a 180 y cuando esto sucedia el programa volvia a empezar desde el principio.

[Imagen de la programación utilizada](https://drive.google.com/file/d/1puDJ0viPpVL3oPNEVQroXuWTOXrvlg3E/view?usp=sharing)

---

## 6) Resultado y evidencia

El resultado fué el esperado ya que el servomotor empezaba con un giro de 10 grados girando coda vez mas hasta llegar a los 180 grados y volvía a repetir el ciclo.

[Video del funcionamiento del servomotor](https://drive.google.com/file/d/1tfvKkWcTvmlawQ5-rqkEjaDrcSRBzs5e/view?usp=sharing)
