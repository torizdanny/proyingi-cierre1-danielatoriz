# Investigación: ¿esto ya existe? ¿quién lo dice?

**Autor:** Daniela Toríz García  
**Fecha:** 17/09/2026  
**Ideas analizadas:** ver [[ideas-proyecto]] o [ideas-proyecto.md](ideas-proyecto.md)  

---

## Parte 1. Un ejemplo que ya existe, por cada idea

### Idea 1: Llavero inteligente en forma de amplificador de guitarra

- **Qué encontré:** Llavero con diseño de amplificador de guitarra que, al conectar las llaves mediante un conector de audio (Jack), enciende un LED para controlar quién está en casa y evitar perder las llaves.
- **Enlace:** https://youtube.com/shorts/CLz6DKQUc_g?si=MGvAD4u95HqF_nrp
- **Qué hace:** Conecta cada llavero como un botón pulsador a una placa ESP8266 o ESP32, detectando la presencia física de las llaves al insertar la clavija.
- **Por qué no resuelve mi caso:** Porque es un sistema pasivo que solo registra la presencia de las llaves; mi propuesta busca emitir una alarma sonora/luminosa activa programada según mis horarios de salida para evitar descuidos.

### Idea 2: Alarma interactiva con objetivo de tiro

- **Qué encontré:** Reloj despertador interactivo con un blanco de tiro y una pistola de infrarrojos o dardos.
- **Enlace:** https://blog.bricogeek.com/noticias/arduino/como-hacer-el-despertador-led-definitivo-con-arduino-requiere-punteria/
- **Qué hace:** Activa una alarma sonora que solo se apaga cuando el usuario apunta y acierta al centro del tablero con la pistola.
- **Por qué no resuelve mi caso:** Requiere mecanismos mecánicos y accesorios complejos, mientras que mi propuesta busca resolver la misma necesidad de forma más sencilla, directa y accesible.

### Idea 3: Monitor de calidad de aire

- **Qué encontré:** Medidor y alerta de calidad de aire con sensor MQ-135 y Arduino.
- **Enlace:** https://www.instructables.com/Calidad-De-Air-Sensor-Mq-135/
- **Qué hace:** Mide la presencia de gases en el ambiente y muestra los valores numéricos continuamente en una pantalla LCD.
- **Por qué no resuelve mi caso:** Funciona como un instrumento de medición pasivo que requiere revisar la pantalla constantemente; mi propuesta analiza los datos e integra una alarma preventiva directa.

---

## Parte 2. Fuentes de la idea que elegí

### Fuente 1

| Campo | Contenido |
|---|---|
| Autor u organización | Home Assistant y Domótica Fácil |
| Título | Llavero Inteligente ¡Nunca Más Pierdas Tus Llaves! |
| Año | 2025 |
| Enlace | https://youtube.com/shorts/CLz6DKQUc_g?si=MGvAD4u95HqF_nrp |
| Tipo | Video / Demostración de prototipo |
| Por qué le creo | Muestra una prueba funcional y visual del prototipo en tiempo real. |
| Qué dato me dio | La idea de utilizar conectores tipo Jack para combinar un diseño estético con detección eléctrica. |

### Fuente 2

| Campo | Contenido |
|---|---|
| Autor u organización | Brico Geek (Oscar González) |
| Título | Cómo hacer el despertador LED definitivo con Arduino (requiere puntería!) |
| Año | 2017 |
| Enlace | https://blog.bricogeek.com/noticias/arduino/como-hacer-el-despertador-led-definitivo-con-arduino-requiere-punteria/ |
| Tipo | Blog / Documentación técnica en español |
| Por qué le creo | Es un portal de divulgación tecnológica reconocido con código fuente y demostración del ensamblaje. |
| Qué dato me dio | La lógica de lectura de fotodetectores e interrupciones para desactivar la alarma sonora. |

### Fuente 3 (opcional)

| Campo | Contenido |
|---|---|
| Autor u organización | Instructables |
| Título | Calidad del aire del Air Sensor MQ-135 |
| Año | 2018 |
| Enlace | https://www.instructables.com/Calidad-De-Air-Sensor-Mq-135/ |
| Tipo | Documentación y tutorial |
| Por qué le creo | Es una comunidad abierta de proyectos con tutoriales y documentación técnica verificada paso a paso. |
| Qué dato me dio | Cómo conectar el sensor MQ-135 a un microcontrolador y desplegar lecturas en una pantalla LCD. |

---

## Parte 3. Qué haría distinto

A diferencia de los proyectos encontrados, los cuales funcionan de manera pasiva o como simples instrumentos de medición, mi propuesta integra un sistema de alertas activas programadas con base en horarios específicos de salida diario. El dispositivo no solo registra si la llave está puesta, sino que avisa de forma sonora y luminosa si el usuario intenta salir sin ellas.

---

## Parte 4. Qué me falta averiguar

- [ ] ¿Cómo programar el microcontrolador o módulo correspondiente para gestionar y configurar los horarios de la alarma?
- [ ] Medir el consumo exacto de energía de la batería cuando el dispositivo permanece en modo de espera (standby).
- [ ] Probar la durabilidad física del mecanismo de detección y de los conectores con el uso diario de las llaves.

---

## Declaración de uso de IA

- **Herramienta utilizada:** Gemini (septiembre 2026).
- **Qué le pedí:** Revisión de la redacción, verificación de los enlaces de las fuentes y apoyo en la explicación de términos técnicos de las propuestas.
- **Qué modifiqué o rechacé de su respuesta:** Descarté las sugerencias de proyectos alternativos que no coincidían con mis búsquedas y corregí los enlaces para asegurarme de que abrieran de forma directa.