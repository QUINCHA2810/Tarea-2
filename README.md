
# Tarea 2 – ASCII y RS232

## 1. Código ASCII

El **código ASCII** (American Standard Code for Information Interchange) fue desarrollado en **1963** por el comité ASA (American Standards Association, hoy ANSI) con el objetivo de unificar la forma en la que los dispositivos representaban caracteres. Antes de ASCII cada fabricante usaba su propio sistema de codificación, lo que dificultaba la comunicación entre equipos distintos.  

ASCII usa **7 bits** para representar un total de **128 caracteres (0–127)**. Entre ellos están:  
- Letras mayúsculas y minúsculas (A–Z, a–z).  
- Dígitos numéricos (0–9).  
- Símbolos de puntuación.  
- Caracteres de control (ejemplo: `ESC`, `CR` para salto de línea, `BEL` para la campana).  

En los años 80 se amplió a **8 bits (ASCII extendido)**, permitiendo 256 códigos (0–255). En este rango adicional se incluyen letras con tildes (á, é, í, ó, ú), símbolos matemáticos y gráficos usados en interfaces antiguas.  

**Importancia:** ASCII fue el primer estándar de codificación de caracteres que permitió la interoperabilidad entre computadoras, impresoras, terminales y más tarde internet (correo electrónico, protocolos de red). Hoy, aunque fue reemplazado en gran parte por **Unicode (UTF-8)**, sigue siendo la base de compatibilidad para representar texto.  

**Fuentes:**  
- [ANSI – The history of ASCII](https://www.ansi.org/news/standards-news/all-news/2013/10/the-history-of-ascii-10)  
- [IBM – What is ASCII?](https://developer.ibm.com/articles/au-ascii/)

---

## 2. Pines de los conectores RS232

El estándar **RS232** define cómo se comunican los dispositivos usando transmisión serie asíncrona. Uno de sus aspectos más importantes son los **conectores físicos** que se utilizan.

### Conector DB9 (9 pines, el más común en PCs)  
1. **DCD (Data Carrier Detect):** indica que el módem detecta señal portadora.  
2. **RXD (Receive Data):** entrada de datos recibidos.  
3. **TXD (Transmit Data):** salida de datos transmitidos.  
4. **DTR (Data Terminal Ready):** señal que indica que el dispositivo está listo.  
5. **GND (Ground):** tierra eléctrica.  
6. **DSR (Data Set Ready):** indica que el dispositivo remoto está listo.  
7. **RTS (Request to Send):** solicitud de permiso para transmitir.  
8. **CTS (Clear to Send):** autorización para transmitir.  
9. **RI (Ring Indicator):** indica llamada entrante (usado en módems antiguos).  

### Conector DB25 (25 pines, estándar original)  
- **Pin 2:** TXD (Transmit Data)  
- **Pin 3:** RXD (Receive Data)  
- **Pin 7:** GND  
- **Pin 4:** RTS, **Pin 5:** CTS, **Pin 6:** DSR, **Pin 8:** DCD, **Pin 20:** DTR  
- Los demás pines corresponden a señales adicionales de control y sincronización.  

**Aplicación práctica:** Estos conectores permitieron conectar PCs con impresoras, módems y otros periféricos en las décadas de 1980 y 1990. Aún hoy se usan en sistemas industriales y equipos de comunicación.  

**Fuentes:**  
- [RS232 DB9 & DB25 Pinouts – TechTarget](https://www.techtarget.com/searchnetworking/definition/RS-232)  
- [AllPinouts – RS232 Pinout](https://allpinouts.org/pinouts/connectors/serial/)

---

## 3. Formato del protocolo RS232  

RS232 es un protocolo de **comunicación serial asíncrona** que transmite un bit a la vez a través de un solo canal de datos (TX y RX).  

**Características principales:**  
- **Velocidad de transmisión:** definida en baudios (ej. 9600, 115200 bps).  
- **Niveles eléctricos:** usan tensiones relativamente altas (−3V a −15V para un “1” lógico y +3V a +15V para un “0”).  
- **Sincronización:** no usa un reloj compartido; por eso necesita bits de inicio y parada.  

**Estructura de una trama RS232:**  
1. **Bit de inicio (Start bit):** siempre en 0 (nivel bajo). Informa al receptor que empieza la transmisión.  
2. **Bits de datos:** puede ser 5, 6, 7 u 8 (los más usados son 7 u 8).  
3. **Bit de paridad (opcional):** sirve para detección de errores (puede ser par, impar o ninguno).  
4. **Bit(s) de parada (Stop bits):** 1, 1.5 o 2 bits en nivel alto (1), marcan el fin de la trama.  

Ejemplo común de configuración:  
- **9600-8N1** = 9600 baudios, 8 bits de datos, No paridad, 1 bit de parada.  

**Ventajas:** simple, confiable y ampliamente soportado.  
**Desventajas:** velocidades limitadas, distancias máximas de ~15 m, y no permite conectar muchos dispositivos a la vez.  

**Fuentes:**  
- [NI – RS232 Protocol](https://www.ni.com/docs/en-US/bundle/serial-bus-overview/page/rs232.html)  
- [SparkFun – RS232 Basics](https://learn.sparkfun.com/tutorials/serial-communication/rs-232)

---

## 4. Repositorio

Este archivo (`README.md`) contiene la documentación solicitada en la **Tarea 2**.  
El repositorio incluye toda la información en un único archivo para que pueda ser revisada fácilmente.  

---
