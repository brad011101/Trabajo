# **Puerto Priority Manager**

Puerto Priority Manager es una aplicación en Java que gestiona el orden de atención de embarcaciones en un puerto utilizando una cola de prioridad.

## 🎯 **Objetivo**

Es tener un sistema de gestión de atraques en un puerto que administra embarcaciones mediante una cola de prioridad, determinando el orden de atención según reglas configurables (tipo de carga, emergencia, contrato premium y tiempo de espera).

### Está diseñado para:

- Administradores portuarios

- Simulaciones académicas de estructuras de datos

- Proyectos educativos en Java (PriorityQueue + Comparator)

## **🔁 Flujo Principal del Sistema**
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
###  **🎛️ Interfaz**

- Registro de embarcaciones.

- Visualización en tabla ordenada por prioridad.

- Botones: Registrar, Ver siguiente, Atender, Cargar demo, Limpiar cola

![image alt](https://github.com/brad011101/Trabajo/blob/2e3c1794176a61e879413eec94fa44ff9206eede/Imagen1.png)

### **📋  Registro, Administración y Operaciones principales**

- Registrar embarcación.

![image alt](https://github.com/brad011101/Trabajo/blob/161df88fe93529017551ffc2df81536c8d0aeeb6/u.png)

- Listar embarcaciones ordenadas.

![image alt](https://github.com/brad011101/Trabajo/blob/292eca94261ce4bd99f61f7fef7ca7d88bb76029/R.png)

- Ver siguiente.

![image alt](https://github.com/brad011101/Trabajo/blob/292eca94261ce4bd99f61f7fef7ca7d88bb76029/O.png)

- Atender.

![image alt](https://github.com/brad011101/Trabajo/blob/292eca94261ce4bd99f61f7fef7ca7d88bb76029/j.png)

- Limpiar todos los muelles (Limpiar cola)

![image alt](https://github.com/brad011101/Trabajo/blob/19da32ca140f5b2e6edb14392db878b16fa3b98b/y.png)

- Cargar Demo

<img width="843" height="626" alt="image" src="https://github.com/user-attachments/assets/c9ac2f98-cc0f-4498-a175-99ef9f26c230" />

###  **⚙️ Procesamiento con Estructura de Datos**

- Uso de PriorityQueue<Embarcacion>

- Implementación de Comparable

#### Desempate por:

- Mayor prioridad

- Más horas esperando

-  Orden FIFO

<img width="906" height="692" alt="image" src="https://github.com/user-attachments/assets/cf25641f-9907-490b-abb9-90fc4399550e" />

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

<img width="738" height="552" alt="image" src="https://github.com/user-attachments/assets/079c6980-707e-4b98-9084-8350866f796a" />

- Límite de muelles alcanzado

<img width="700" height="511" alt="image" src="https://github.com/user-attachments/assets/0654e87e-5067-45f3-845d-f2604e66fe9e" />

