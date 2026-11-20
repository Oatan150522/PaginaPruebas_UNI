
# Testing Web - Entorno de Pruebas

## 1. Descripción del proyecto

Desarrollar una página web de pruebas que permita validar el funcionamiento de un agente automatizado de consultas web.

Esta página funcionará como un entorno controlado para realizar consultas, simular búsquedas, procesar información y visualizar los resultados obtenidos por el sistema.

El objetivo es disponer de una interfaz independiente para probar las funcionalidades del futuro agente antes de realizar su implementación en el entorno empresarial.

## 2. Objetivos

- Crear una página web independiente para realizar pruebas.
- Permitir ingresar consultas manualmente.
- Simular búsquedas y consultas de información.
- Mostrar los resultados obtenidos por el sistema.
- Validar la estructura y consistencia de las respuestas.
- Registrar los resultados de las pruebas.
- Preparar la estructura para futuras integraciones empresariales.

## 3. Alcance

La primera versión será exclusivamente de pruebas (MVP).

No tendrá conexión directa con bases de datos productivas ni modificará información de los sistemas empresariales.

Se implementarán funcionalidades básicas que permitan comprobar el flujo de trabajo del futuro agente automatizado.

## 4. Tecnologías propuestas

| Tecnología | Utilización |
|---|---|
| HTML5 | Estructura de la página |
| CSS3 | Diseño y estilos |
| JavaScript | Interactividad |
| Python | Backend y procesamiento |
| Flask | Comunicación entre frontend y backend |
| Git | Control de versiones |

## 5. Funcionalidades principales

### 5.1. Panel principal

- Visualizar el estado del sistema.
- Ingresar consultas.
- Ejecutar pruebas.
- Visualizar resultados.
- Consultar el historial de pruebas.

### 5.2. Módulo de consultas

Implementar un campo de texto que permita ingresar consultas manualmente.

Ejemplo:

> Consultar información sobre los festivos de Colombia para el año 2027.

El sistema deberá procesar la solicitud y mostrar el resultado correspondiente.

### 5.3. Visualización de resultados

Mostrar la siguiente información:

- Consulta realizada.
- Fecha y hora de ejecución.
- Estado de la consulta.
- Resultado obtenido.
- Mensajes de error, cuando corresponda.

### 5.4. Historial de pruebas

Implementar una sección que permita consultar las pruebas realizadas anteriormente y verificar sus resultados.

## 6. Arquitectura del proyecto

La aplicación estará organizada en dos componentes principales:

**Frontend:**
- Interfaz gráfica.
- Formulario de consultas.
- Visualización de resultados.
- Historial de ejecuciones.

**Backend:**
- Recepción de solicitudes.
- Procesamiento de consultas.
- Comunicación con servicios externos.
- Gestión de respuestas.
- Manejo de errores.

### Flujo de funcionamiento

```text
Usuario
   |
   v
Página Web (Frontend)
   |
   v
Backend Python (Flask)
   |
   v
Motor de consultas
   |
   v
Procesamiento de información
   |
   v
Resultado
   |
   v
Visualización en la página web
```

## 7. Estructura inicial del proyecto

```text
testing-web/
│
├── frontend/
│   ├── index.html
│   ├── css/
│   │   └── styles.css
│   └── js/
│       └── app.js
│
├── backend/
│   ├── app.py
│   ├── routes/
│   │   └── queries.py
│   └── services/
│       └── query_service.py
│
├── tests/
│   └── test_queries.py
│
├── requirements.txt
├── .gitignore
└── README.md
```

## 8. Escenarios de prueba

| Prueba | Resultado esperado |
|---|---|
| Consulta válida | Mostrar respuesta |
| Campo vacío | Mostrar validación |
| Consulta sin resultados | Informar que no existen resultados |
| Error de conexión | Mostrar mensaje de error |
| Consulta repetida | Procesar correctamente |
| Servicio no disponible | Informar el estado del servicio |

## 9. Instalación y ejecución

### 9.1. Crear entorno virtual

```bash
python -m venv venv
```

### 9.2. Activar entorno virtual

**Windows:**

```bash
venv\Scripts\activate
```

**Linux:**

```bash
source venv/bin/activate
```

### 9.3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 9.4. Ejecutar el backend

```bash
python backend/app.py
```

### 9.5. Acceder a la aplicación

```text
http://127.0.0.1:5000
```

## 10. Consideraciones para la integración empresarial

La aplicación deberá desarrollarse pensando en futuras integraciones con los sistemas utilizados por la empresa.

Se deberán considerar:

- Integración con Zoho.
- Servicios de correo electrónico mediante Gmail.
- Consultas a diferentes fuentes de información web.
- Posible integración con MAIA, pendiente de identificar los mecanismos de acceso disponibles.
- Autenticación y control de acceso.
- Registro de consultas y auditoría.
- Manejo seguro de credenciales y variables de entorno.
- Separación de ambientes de desarrollo, pruebas y producción.

## 11. Fases de desarrollo

1. **Diseño:** Crear la estructura visual de la página.
2. **Frontend:** Implementar formularios y visualización de resultados.
3. **Backend:** Implementar el procesamiento de solicitudes.
4. **Pruebas:** Validar los escenarios de funcionamiento.
5. **Integraciones:** Evaluar conexiones con servicios externos.
6. **Preparación empresarial:** Documentar los ajustes necesarios para producción.

## 12. Resultado esperado

Obtener una aplicación web funcional que permita realizar pruebas controladas sobre el flujo de consultas automatizadas.

Este entorno servirá como base para desarrollar, evaluar y mejorar el agente antes de conectarlo con los servicios y sistemas reales de la empresa.

---

**Nota:** Esta primera versión corresponde a un prototipo de pruebas (MVP) y no debe utilizarse como herramienta de operación en producción.
