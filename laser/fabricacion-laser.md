# Fabricación con corte láser — Segundo parcial

**Alumna:** Daniela Toríz García  
**Materia:** Proyecto de Ingeniería I · IBERO Puebla  
**Profesor:** Mtro. Rafael Pérez Aguirre  
**Fecha:** 22 de octubre de 2026  

## 1. Diseño y dimensiones

- **Software:** Onshape (panel inicial) y FreeCAD 1.1.4 (caja paramétrica mediante macro Python).
- **Caja de cinco caras:** 80.00 mm de ancho × 60.00 mm de alto × 50.00 mm de fondo.
- **Material:** MDF con espesor medido de **3.12 mm**.
- **Uniones:** tres dedos por arista (*finger joints*).
- **Separación de piezas en el plano:** 3.00 mm.
- **Kerf configurado en FreeCAD actual:** 89.00 µm = **0.089 mm**.
- **Cara frontal de la caja:** abertura rectangular de 25 × 15 mm y seis orificios de Ø3 mm, según `cad/caja_freecad/caja.md`git
- **Diseño 2D previo (Onshape):** placa de 120 × 100 mm, seis perforaciones de Ø5 mm. Es el antecedente y **no** mide lo mismo que la caja final.

**Evolución:** se pasó del panel inicial 2D a la caja tridimensional abierta, con cinco piezas planas y pestañas de ensamblaje; se verificaron los parámetros de espesor, número de dedos y compensación de corte.

## 2. Prueba de kerf

Tira diseñada: **100 × 20 mm**, dividida en diez secciones de 10 × 20 mm.

| Dato registrado | Resultado |
|---|---:|
| Ancho nominal de ranura | **3.00 mm** |
| Ancho real de ranura | **3.15 mm** |
| Diferencia total (3.15 − 3.00) | **0.15 mm** |
| Diferencia por borde (0.15 / 2) | **0.075 mm** |
| Ranura con mejor ajuste reportado | **0.10 mm de compensación** |
| Parámetro de kerf visible en FreeCAD | **0.089 mm (89 µm)** |

La ranura física quedó 0.15 mm más ancha que la nominal, pues el haz elimina material en ambos bordes. Para la compensación dimensional se tomó como referencia **0.075 mm por lado** y se comparó el encaje de las opciones de la tira, cuya compensación de **0.10 mm** produjo el mejor ajuste. El modelo de FreeCAD de la captura tiene configurado **0.089 mm**; es un parámetro del CAD y no debe confundirse con los **0.075 mm por lado** calculados en la medición.

## 3. Parámetros y fabricación

| Parámetro | Valor |
|---|---|
| Material | MDF de 3.12 mm |
| Capa de trabajo de la máquina | Capa 2 |
| Potencia máxima | **75 %** |
| Potencia mínima | **65 %** |
| Velocidad de trabajo | **25 mm/s** |
| Número de pasadas | **1 pasada**, según registro proporcionado |

Las potencias 75 % / 65 % y los 25 mm/s están visibles en la fotografía propia del panel de configuración. La lectura inferior de 100 mm/s y 30 % corresponde a controles separados y **no** a los parámetros de corte de esa capa.

## 4. Problemas, causas y ajustes

| Problema | Causa | Ajuste realizado |
|---|---|---|
| Dificultad para generar las juntas compatibles de las cinco caras | Era necesario conservar dimensiones exteriores, espesor y 3 dedos por arista | Se generaron las piezas mediante una macro paramétrica de Python para FreeCAD y se revisó el despiece. |
| Ranura física mayor que la dibujada | El láser eliminó material a ambos bordes; 3.00 mm nominales frente a 3.15 mm reales | Se calculó 0.075 mm de diferencia por borde y se probaron compensaciones; el ajuste de 0.10 mm fue el que mejor encajó. Se registró en CAD un kerf final de 0.089 mm. |

## 5. Evidencias y archivos del repositorio

Las capturas propias de FreeCAD y de la máquina utilizadas en el reporte fueron proporcionadas por la alumna. Se deben añadir a la carpeta `laser/` las fotos del corte, de la tira y de la caja armada, junto con los DXF finales y este archivo Markdown.

En la última revisión se localizaron: `cad/caja_freecad/caja.dxf`, `cad/caja_freecad/kerf.dxf` y `cad/diseño_carafrontal/pieza-s6.dxf`. **Esta actualización local no equivale a hacer commit y push** de una carpeta `laser/`.

### Organización requerida

```text
laser/
├── caja.dxf
├── kerf.dxf
├── fabricacion-laser.md
└── fotos/
    ├── captura-freecad.png
    ├── parametros-maquina.jpg
    ├── tira-kerf.jpg
    ├── proceso-corte.jpg
    └── caja-armada.jpg
```

## 6. Conclusión

El resultado integró el diseño paramétrico de una caja en MDF con la comprobación física del kerf, importante para garantizar las tolerancias de ensamblaje. La práctica demuestra que una diferencia de 0.15 mm en una ranura obliga a revisar sus juntas antes de fabricar la carcasa del proyecto de llavero inteligente.

## 7. Declaración de uso de IA

Se utilizó ChatGPT para apoyar la macro Python de FreeCAD, revisar los datos de fabricación, estructurar la documentación y generar el Word y Markdown. Se utilizó Gemini previamente como apoyo a la documentación del panel 2D. Se corrigieron los valores preliminares de velocidad al contrastarlos con la fotografía de la máquina, diferenciando las medidas reales y las configuraciones de CAD. Las mediciones y los resultados de ajuste consignados son los datos que proporcionó la alumna.
