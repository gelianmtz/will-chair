# will-chair

## Descripción general

**Will-Chair** es una **silla de ruedas modular inteligente** desarrollada con una **NVIDIA Jetson Nano** como unidad de procesamiento principal.  
El sistema está diseñado para **adaptarse a las necesidades específicas de cada usuario** mediante la conexión e integración de diferentes **módulos de control**, como:

- Control por **joystick**
- Control por **sensores electromiográficos (EMG)**
- Control por **seguimiento ocular**

El software implementa **redes neuronales** (TensorFlow) para calibrar automáticamente los umbrales de control, permitiendo una **personalización precisa, segura y accesible**.

---

## Objetivos del proyecto

- Diseñar una silla de ruedas **modular y adaptable**.
- Permitir la **conexión e intercambio de módulos funcionales** sin configuración manual.
- Integrar distintos **métodos de control** (joystick, EMG, visión ocular).
- Implementar **redes neuronales** para calibración y personalización automática.
- Mantener un enfoque en **seguridad, accesibilidad y bajo costo**.

---

## Tecnologías utilizadas

### Hardware principal
- **NVIDIA Jetson Nano** – Unidad de procesamiento principal  
- **Batería Li-ion 24V / 20Ah** – Fuente de alimentación autónoma  
- **Sensores y módulos periféricos** – Comunicación I²C / UART estandarizada

### Software
- **Lenguaje:** Python 3  
- **Bibliotecas principales:**
  - `TensorFlow` – Implementación de redes neuronales
  - `OpenCV` – Procesamiento de visión para el módulo ocular
  - `Tkinter` – Interfaz gráfica táctil (GUI)
  - `Jetson.GPIO` – Control de pines GPIO
  - `pySerial`, `smbus2` – Comunicación con módulos externos

---

## Arquitectura modular

Will-Chair utiliza un **puerto universal de conexión** que combina:
- **Alimentación eléctrica**
- **Comunicación serial (UART)**
- **Protocolo I²C**

Cada módulo tiene una **identificación electrónica I²C**, lo que permite:
- Detección automática del tipo de módulo
- Activación dinámica del modo de control correspondiente

### Módulos disponibles
| Módulo | Descripción |
|--------|--------------|
| Joystick | Control direccional analógico con retroalimentación háptica |
| Sensores EMG | Interpretación de señales musculares |
| Seguimiento ocular | Control mediante rastreo de la mirada (cámara IR) |

---

## Interfaz de usuario

Una **pantalla táctil integrada** (basada en Tkinter) permite:
- Conectar/desconectar módulos
- Calibrar sensores
- Visualizar estado del sistema
- Monitorear energía y conexión

---

## Resultados esperados

- Implementación exitosa de arquitectura **modular universal**  
- Integración fluida de múltiples métodos de control  
- Calibración inteligente mediante **redes neuronales**  
- Sistema **seguro, estable y accesible** con componentes de bajo costo  

---
