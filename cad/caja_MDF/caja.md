# Caja MDF — Daniela Toríz García

## 1. Medidas de la caja

- Ancho exterior: 80 mm
- Alto exterior: 60 mm
- Fondo exterior: 50 mm
- Espesor real del MDF: 3.12 mm, medido con vernier
- Kerf provisional: 0.20 mm
- Número de dedos por arista: 3
- Separación establecida entre piezas: 3 mm

## 2. Diseño de la caja

El proyecto consiste en una caja abierta de cinco caras, diseñada para fabricarse mediante corte láser en MDF.

La cara frontal contiene una abertura rectangular de 25 × 15 mm y seis perforaciones circulares de 3 mm de diámetro.

Las piezas cuentan con uniones tipo *finger joints* para permitir su ensamblaje.

## 3. Desarrollo del proyecto

Utilicé FreeCAD 1.1.4 para generar las cinco caras de la caja mediante una macro escrita en Python.

La macro permite establecer los valores de ancho, alto, fondo, espesor, kerf y número de dedos, y generar nuevamente las piezas cuando se modifican estos valores en su código.

Los archivos se exportaron en formato DXF para su preparación y posterior corte láser.

## 4. Prueba de kerf

Se preparó una tira de prueba de 100 × 20 mm dividida en diez secciones de 10 × 20 mm.

El kerf inicial establecido es de 0.20 mm. Este valor deberá actualizarse después de realizar la prueba de corte y medir el material.

## 5. Principal dificultad

La parte más complicada fue desarrollar las uniones de dedos y lograr que las cinco caras se generaran respetando las dimensiones y los parámetros establecidos.

El uso de una macro permitió automatizar la construcción de las piezas y reducir el trabajo manual.

## 6. Uso de inteligencia artificial

Utilicé ChatGPT como herramienta de apoyo para desarrollar la macro de FreeCAD, resolver dificultades técnicas durante su ejecución y organizar los archivos de entrega.

## 7. Comprobaciones pendientes

Antes del corte definitivo es necesario verificar la compatibilidad de las uniones, la separación real entre los contornos y el funcionamiento de los parámetros al regenerar el diseño.