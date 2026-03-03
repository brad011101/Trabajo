# Puerto Priority Manager

Puerto Priority Manager es una aplicación en Java que gestiona el orden de atención de embarcaciones en un puerto utilizando una cola de prioridad.

## 🎯 **Objetivo**

Es tener un sistema de gestión de atraques en un puerto que administra embarcaciones mediante una cola de prioridad, determinando el orden de atención según reglas configurables (tipo de carga, emergencia, contrato premium y tiempo de espera).

### Está diseñado para:

- Administradores portuarios

- Simulaciones académicas de estructuras de datos

- Proyectos educativos en Java (PriorityQueue + Comparator)

## **Flujo Principal del Sistema**
### Entrada
- Registro manual de embarcación desde la interfaz gráfica.
- Carga automática de datos demo.
- Parámetros de prioridad definidos en config.properties.

### Procesamiento

- Validación de datos.
- Cálculo de prioridad usando datos configurables.
- Inserción en PriorityQueue<Embarcacion>.

### Salida

- Visualización ordenada en tabla.

- Atención de embarcación prioritaria.

- Registro visual de eventos en consola integrada.

## **Restricciones y Supuestos**

- Máximo 10 muelles simultáneos.

- Matrícula obligatoria con formato: XX-0000.

- Nivel de emergencia: 1 a 5.

- No se permiten matrículas duplicadas.

- Prioridad calculada dinámicamente desde archivo de configuración.

- No hay persistencia en base de datos (modo memoria).

## **✅ Interfaz**

- Registro de embarcaciones.

- Visualización en tabla ordenada por prioridad.

- Botones: Registrar, Ver siguiente, Atender, Cargar demo, Limpiar cola

![image alt](https://github.com/brad011101/Trabajo/blob/2e3c1794176a61e879413eec94fa44ff9206eede/Imagen1.png)

## **📋  Registro y Administración**

- Registrar embarcación.

- Listar embarcaciones ordenadas.

- Ver siguiente.

- Atender.
