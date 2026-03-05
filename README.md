# **Puerto Priority Manager**

Puerto Priority Manager es una aplicación en Java que gestiona el orden de atención de embarcaciones en un puerto utilizando una cola de prioridad.

## 🎯**Objetivo**

Es tener un sistema de gestión de atraques en un puerto que administra embarcaciones mediante una cola de prioridad, determinando el orden de atención según reglas configurables (tipo de carga, emergencia, contrato premium y tiempo de espera).

### Está diseñado para:

- Administradores portuarios

- Simulaciones académicas de estructuras de datos

- Proyectos educativos en Java (PriorityQueue + Comparator)

## **🚀Ejecución del Proyecto**
1️⃣ Abrir la carpeta del proyecto.

2️⃣Ir a la carpeta scripts.

3️⃣hacer doble clic en run_windows o run_linux si ultiliza este sistema.

## **🔁Flujo Principal del Sistema**
####  Entrada
- Registro manual de embarcación desde la interfaz gráfica.
- Carga automática de datos demo.
- Parámetros de prioridad definidos en config.properties.

####  Procesamiento

- Validación de datos.
- Cálculo de prioridad usando datos configurables.
- Inserción en PriorityQueue<Embarcacion>.

####  Salida

- Visualización ordenada en tabla.

- Atención de embarcación prioritaria.

- Registro visual de eventos en consola integrada.

###  **Restricciones y Supuestos**

- Máximo 10 muelles simultáneos.

- Matrícula obligatoria con formato: XX-0000.

- Nivel de emergencia: 1 a 5.

- No se permiten matrículas duplicadas.

- Prioridad calculada dinámicamente desde archivo de configuración.

- No hay persistencia en base de datos (modo memoria).

##  **Funcionalidades implementadas**
###  **🎛️Interfaz**

- Registro de embarcaciones.

- Visualización en tabla ordenada por prioridad.

- Botones: Registrar, Ver siguiente, Atender, Cargar demo, Limpiar cola

### **📋Registro, Administración y Operaciones principales**

- Registrar embarcación.

- Listar embarcaciones ordenadas.

- Ver siguiente.

- Atender.

- Limpiar todos los muelles (Limpiar cola)

- Cargar Demo



###  **⚙️Procesamiento con Estructura de Datos**

- Uso de PriorityQueue<Embarcacion>

- Implementación de Comparable

#### Desempate por:

- Mayor prioridad

- Más horas esperando

-  Orden FIFO


###  **📠Cálculo de Prioridad**

Se basa en config.properties:

priority.peligrosa=10

priority.perecible=7

priority.normal=3

priority.emergenciaFactor=2

priority.premium=5

priority.esperaFactor=2

Fórmula:

#### Prioridad = pesoTipoCarga
- (nivelEmergencia * emergenciaFactor)
- premiumWeight
- (horasEsperando / esperaFactor)  

## **🚨Manejo de Errores y Validaciones**
- Matrícula inválida
- Matrícula duplicada
- Límite de muelles alcanzado

## **📑Reportes y Métricas**

- Orden completo de atención.

- Muelles disponibles dinámicos.

- Registro visual de eventos.

- Prioridad calculada visible en tabla.
# **📚Librerías Utilizadas**

### **Librerías estándar de Java**

java.util → PriorityQueue, List

java.nio.file → Configuración y verificación

java.io → Lectura de archivos

javax.swing → Interfaz gráfica

java.time → Logs

### *No se uso  librerías adicionales*

### **☕Versión recomendada de Java**

JDK 17 o superior

## **♻️Cambios realizados (bitácora técnica)**
### *Lista de cambios*
Se rediseñó el sistema de log para mostrar mensajes en distintos colores según el tipo de evento:

🟢 Verde: Acciones realizadas correctamente.

🔴 Rojo: Errores o validaciones fallidas.

⚫ Negro: Información general del sistema.

🔵 Azul: Confirmación del inicio correcto del programa.

Se implementó el cálculo dinámico de prioridad de las embarcaciones considerando:

Nivel de emergencia.

Tipo de carga.

Estado premium.

Horas de espera.

Parámetros configurables desde config.properties.

Se desarrolló la función de atención automática de embarcaciones utilizando una PriorityQueue, garantizando que siempre se atienda primero la de mayor prioridad.

Se añadió la funcionalidad para registrar nuevas embarcaciones desde la interfaz gráfica con validaciones incluidas.

### *Mejoras realizadas*
Se implementó validación de matrícula única, evitando el registro de embarcaciones duplicadas.

Se estableció un límite máximo de 10 muelles, impidiendo registrar más embarcaciones cuando la capacidad está completa.

Se mejoró el sistema de log visual con texto multicolor para facilitar la identificación rápida de errores y acciones exitosas.

Se agregó un indicador dinámico que muestra en tiempo real la cantidad de muelles disponibles.

Se corrigió la interfaz gráfica deshabilitando la entrada manual por teclado en los campos de:

Nivel de emergencia.

Horas de espera.
Esto evita errores de formato y mejora la validación de datos.

## **🧾Evidencias**
- Evidencia 1 Capturas de ejecución (terminal o consola)

  <img width="718" height="387" alt="image" src="https://github.com/user-attachments/assets/795537ca-ba79-44a1-a3d9-9a1c5f4dcc12" />

- Evidencia 2  Cargar demo

  <img width="644" height="478" alt="image" src="https://github.com/user-attachments/assets/ee303ccb-89d5-4202-9f9d-f22e1b56d70e" />

- Evidencia 3 Errores.

<img width="738" height="552" alt="image" src="https://github.com/user-attachments/assets/079c6980-707e-4b98-9084-8350866f796a" />

<img width="700" height="511" alt="image" src="https://github.com/user-attachments/assets/0654e87e-5067-45f3-845d-f2604e66fe9e" />

- Evidencia 4 Registro, Administración y Operaciones principales

![image alt](https://github.com/brad011101/Trabajo/blob/161df88fe93529017551ffc2df81536c8d0aeeb6/u.png)

![image alt](https://github.com/brad011101/Trabajo/blob/292eca94261ce4bd99f61f7fef7ca7d88bb76029/R.png)

![image alt](https://github.com/brad011101/Trabajo/blob/292eca94261ce4bd99f61f7fef7ca7d88bb76029/O.png)

![image alt](https://github.com/brad011101/Trabajo/blob/292eca94261ce4bd99f61f7fef7ca7d88bb76029/j.png)

![image alt](https://github.com/brad011101/Trabajo/blob/19da32ca140f5b2e6edb14392db878b16fa3b98b/y.png)

-Evidencia 5 Procesamiento con Estructura de Datos

<img width="685" height="523" alt="image" src="https://github.com/user-attachments/assets/4b355e58-9129-4ac6-a93c-190df85b3ac1" />

## **🏗️Árbol del proyecto**
PuertoPriorityManager_Starter/
│
├── .vs/           → Configuración del entorno de desarrollo
├── build/         → Archivos compilados
├── checksums/     → Verificación de integridad
├── config/        → Archivo config.properties
├── scripts/       → Script de ejecución (run_windows.bat)
├── src/           → Código fuente Java
└── README.md      → Documentación del proyecto

## **🧩Convenciones y Organización del Código**
### 📌Modelo

- Embarcacion.java

- Representa la entidad principal del sistema.

- Implementa Comparable para permitir el ordenamiento por prioridad.

### ⚙️Lógica de Negocio

- PuertoManager.java

- Gestiona la PriorityQueue.

- Controla registro, atención y validaciones.

- Aplica reglas de prioridad.

### 🖥️Interfaz (UI)

- Main.java

- Contiene la interfaz gráfica desarrollada con Swing.

- Maneja eventos de botones y muestra los resultados en tabla y log.

### 🛠️Utilidades

- Lectura de config.properties para parámetros dinámicos.

- Validaciones de formato de matrícula.

- Sistema de log con colores según tipo de mensaje.
