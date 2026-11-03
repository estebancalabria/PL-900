# Microsoft Power Platform - Fundamentos y valor empresarial

Microsoft Power Platform es una plataforma **low-code** que permite crear aplicaciones, automatizar procesos, desarrollar portales, organizar datos empresariales y construir agentes con inteligencia artificial.

Su objetivo es acercar el desarrollo de soluciones a las personas que conocen los procesos de negocio, reduciendo tiempos de desarrollo y la dependencia exclusiva de equipos de desarrollo profesional.

## Componentes principales

- **Power Apps** → creación de aplicaciones.
- **Power Automate** → automatización de procesos.
- **Power Pages** → creación de sitios web y portales externos.
- **Dataverse** → almacenamiento y administración de datos empresariales.
- **Copilot Studio** → creación de agentes de IA.
- **Copilot y AI Builder** → incorporación de IA generativa e inteligencia artificial.
- **Conectores** → integración con servicios y sistemas externos.
- **Plan Designer** → diseño asistido por IA de soluciones completas de Power Platform.

---

# Power Apps

Microsoft Power Apps es una plataforma **low-code para crear aplicaciones empresariales personalizadas**.

Permite reemplazar procesos basados en hojas de cálculo, formularios, correos electrónicos o papel por aplicaciones adaptadas al proceso real de una organización.

## Valor empresarial

Power Apps acerca el desarrollo de aplicaciones a las personas que conocen los procesos.

Los usuarios empresariales pueden:

- Crear prototipos rápidamente.
- Participar directamente en el diseño.
- Validar soluciones con usuarios reales.
- Iterar antes de realizar grandes inversiones.
- Reducir la dependencia de desarrollos tradicionales.

El objetivo no es reemplazar a TI o a los desarrolladores profesionales, sino favorecer un modelo colaborativo:

**Usuarios de negocio:** conocimiento del proceso y necesidades.

**TI:** seguridad, gobernanza, arquitectura, datos e integraciones complejas.

## Tipos de aplicaciones

### Canvas Apps

Ofrecen gran libertad sobre la interfaz y la experiencia del usuario.

Son apropiadas cuando se necesita una experiencia altamente personalizada.

Ejemplos:

- Inspecciones de campo.
- Solicitudes de empleados.
- Gestión de inventario.
- Registro de eventos.

### Model-driven Apps

Se construyen principalmente sobre **Microsoft Dataverse**.

La interfaz se genera a partir del modelo de datos, por lo que son apropiadas para procesos empresariales estructurados y centrados en datos.

Ejemplos:

- Gestión de casos.
- Gestión de activos.
- Pipeline de ventas.
- Gestión de proyectos.

## Copilot en Power Apps

Copilot permite describir una aplicación utilizando lenguaje natural.

Por ejemplo:

> Crear una aplicación para gestionar solicitudes de servicio de empleados incluyendo solicitante, departamento, categoría, descripción, prioridad, propietario, fecha de vencimiento y estado.

Copilot puede ayudar a generar:

- Tablas de Dataverse.
- Columnas.
- Relaciones.
- Pantallas.
- Formularios.
- Una primera versión funcional de la aplicación.

Esto permite pasar rápidamente de una **idea a un prototipo funcional**.

---

# Power Automate

Microsoft Power Automate es un servicio de automatización que permite crear **flujos de trabajo** que conectan aplicaciones, servicios, datos y personas.

El objetivo es automatizar procesos repetitivos y reducir tareas manuales.

## Valor empresarial

Power Automate permite transformar procesos con múltiples pasos manuales en flujos coordinados.

Por ejemplo:

**Solicitud → validación → aprobación → actualización de datos → notificación → seguimiento**

Beneficios:

- Menos tareas manuales.
- Menos errores.
- Procesos más rápidos.
- Mayor trazabilidad.
- Mayor consistencia.
- Mejor integración entre sistemas.

## Tipos de flujos

### Cloud Flows

Se ejecutan en la nube y pueden iniciarse:

- Automáticamente mediante eventos.
- Según una programación.
- Manualmente.

Ejemplos:

- Aprobación de compras.
- Incorporación de empleados.
- Escalación de casos de clientes.
- Procesamiento de facturas.

### Desktop Flows

Utilizan **Robotic Process Automation (RPA)** para automatizar tareas realizadas sobre interfaces de escritorio.

Son útiles cuando existen aplicaciones antiguas o sistemas sin API.

Ejemplos:

- Carga de datos en un ERP heredado.
- Consolidación de hojas de cálculo.
- Actualización de portales web.
- Organización automática de archivos.

### Process Mining

Permite analizar procesos utilizando datos reales para descubrir:

- Ineficiencias.
- Cuellos de botella.
- Variaciones del proceso.
- Oportunidades de automatización.

## Copilot en Power Automate

Copilot permite crear automatizaciones describiendo el proceso en lenguaje natural.

Ejemplo:

> Cuando se cree una incidencia de soporte técnico de alta prioridad en Dataverse, enviar una notificación de Teams al administrador.

Copilot puede proponer:

- Trigger.
- Acciones.
- Conectores.
- Condiciones.
- Lógica del flujo.

Las capacidades generativas también permiten analizar contenido no estructurado y tomar decisiones durante la ejecución del flujo.

---

# Power Pages

Microsoft Power Pages es una plataforma **low-code SaaS** para crear sitios web empresariales orientados principalmente a usuarios externos.

Permite crear portales conectados directamente con **Microsoft Dataverse**.

## Valor empresarial

Power Pages permite extender procesos empresariales fuera de la organización.

Los usuarios externos pueden:

- Registrarse.
- Completar formularios.
- Consultar información.
- Subir documentos.
- Consultar el estado de solicitudes.
- Acceder a servicios de autoservicio.

Los permisos y roles permiten controlar qué información puede consultar o modificar cada usuario.

## Casos de uso

- Portal de servicio al cliente.
- Portal de proveedores.
- Incorporación de partners.
- Registro de estudiantes o ciudadanos.
- Portales de servicio de campo.
- Portales públicos.
- Portales de conocimiento.

## Copilot en Power Pages

Copilot puede generar a partir de lenguaje natural:

- Estructura del sitio.
- Páginas.
- Formularios.
- Contenido.
- Tablas de Dataverse.

De esta forma puede acelerarse considerablemente la creación de portales empresariales.

---

# Microsoft Dataverse

Microsoft Dataverse es la **plataforma de datos de Power Platform**.

Permite almacenar, organizar, relacionar y proteger los datos utilizados por aplicaciones, automatizaciones, portales, informes y agentes.

Puede considerarse el **tejido conectivo de Power Platform**.

```text
Power Apps
     │
Power Automate
     │
Power Pages
     │
Copilot Studio
     │
Power BI
     │
     ▼
 Dataverse
```

## Características

Dataverse organiza los datos mediante:

- Tablas.
- Filas.
- Columnas.
- Relaciones.

Además incorpora:

- Seguridad basada en roles.
- Seguridad a nivel de campo.
- Auditoría.
- Reglas de negocio.
- Validaciones.
- Campos calculados.
- Integración con servicios Microsoft.
- Administración del ciclo de vida de las aplicaciones.

## Valor empresarial

Dataverse permite que múltiples soluciones utilicen la misma información.

Por ejemplo:

```text
Power Apps
    │
    ▼
Dataverse
    │
    ├── Power Automate
    ├── Power Pages
    ├── Power BI
    └── Copilot Studio
```

Esto evita crear silos de información separados para cada aplicación.

Dataverse **no es solamente una base de datos**. Es una plataforma de datos empresariales que incorpora seguridad, relaciones, lógica empresarial, auditoría e integración.

---

# Copilot Studio

Microsoft Copilot Studio es una plataforma **low-code para crear agentes de inteligencia artificial**.

Estos agentes pueden comprender lenguaje natural, acceder a conocimiento empresarial, consultar datos y ejecutar acciones.

## Qué puede hacer un agente

Un agente puede:

- Responder preguntas.
- Consultar documentos.
- Consultar Dataverse.
- Utilizar conocimiento de SharePoint.
- Ejecutar acciones.
- Activar Power Automate.
- Mantener conversaciones de varios turnos.
- Escalar situaciones a personas.
- Operar autónomamente.

## Patrón fundamental

Un agente puede combinar:

```text
Conocimiento
     +
Datos empresariales
     +
Acciones
     │
     ▼
Agente
```

El usuario simplemente expresa qué necesita en lenguaje natural.

## Ejemplos

### Agente de RR. HH.

Responde preguntas sobre:

- Beneficios.
- Vacaciones.
- Políticas.
- Gastos.
- Incorporación.

### Agente de soporte TI

Puede:

- Consultar documentación.
- Guiar al usuario.
- Resolver problemas comunes.
- Crear tickets.
- Escalar incidentes.

### Agente de atención al cliente

Puede:

- Consultar pedidos.
- Consultar garantías.
- Gestionar devoluciones.
- Crear casos.
- Consultar Dataverse.

### Agente comercial

Puede proporcionar:

- Resúmenes de cuentas.
- Información de productos.
- Información competitiva.
- Próximas acciones recomendadas.

## Agentes autónomos

Copilot Studio también permite crear agentes capaces de actuar sin esperar una conversación iniciada por una persona.

Por ejemplo:

```text
Nuevo registro en Dataverse
          │
          ▼
      Agente detecta
          │
          ▼
     Analiza situación
          │
          ▼
       Decide acción
          │
          ▼
Actualiza / Notifica / Escala
```

Esto permite incorporar agentes directamente dentro de procesos empresariales.

---

# IA generativa en Power Platform

La IA generativa permite crear contenido o estructuras nuevas a partir de instrucciones expresadas en lenguaje natural.

El patrón básico es:

```text
Descripción en lenguaje natural
              │
              ▼
             IA
              │
              ▼
     Primera solución
              │
              ▼
      Revisión humana
              │
              ▼
        Refinamiento
```

Copilot está integrado en distintos componentes de Power Platform.

### Power Apps

Puede generar aplicaciones, tablas y pantallas.

### Power Automate

Puede generar flujos, acciones y lógica.

### Power Pages

Puede generar páginas, formularios y contenido.

### Power BI

Puede ayudar a generar visualizaciones y analizar información utilizando lenguaje natural.

### Dataverse

Puede ayudar a diseñar tablas, columnas y relaciones.

---

# AI Builder

AI Builder permite incorporar modelos de inteligencia artificial dentro de Power Apps y Power Automate sin necesidad de desarrollar modelos desde cero.

Algunos escenarios:

- Procesamiento de documentos.
- Extracción de información.
- Detección de objetos.
- Clasificación de texto.
- Predicciones.

Ejemplo:

```text
Factura PDF
    │
    ▼
AI Builder
    │
    ├── Proveedor
    ├── Número de factura
    ├── Fecha
    └── Importe
    │
    ▼
Power Automate
    │
    ▼
Dataverse / ERP
```

---

# Inteligencia artificial responsable

Las capacidades de IA deben utilizarse siguiendo principios de IA responsable.

Entre los principios promovidos por Microsoft se encuentran:

- Equidad.
- Confiabilidad y seguridad.
- Privacidad.
- Inclusión.
- Transparencia.
- Responsabilidad.

Las respuestas generadas por IA deben considerarse **resultados que requieren supervisión humana**, especialmente en escenarios sensibles o de alto impacto.

---

# Conectores

Los conectores permiten integrar Power Platform con servicios externos.

Funcionan como interfaces predefinidas que permiten a Power Apps, Power Automate y otros componentes comunicarse con otros sistemas.

Ejemplos:

- SharePoint.
- Outlook.
- Teams.
- Dynamics 365.
- Salesforce.
- SAP.
- ServiceNow.
- Dropbox.

## Acciones y triggers

Los conectores normalmente proporcionan:

### Acciones

Operaciones que Power Platform puede ejecutar.

Por ejemplo:

> Enviar un correo electrónico.

### Triggers

Eventos que pueden iniciar una automatización.

Por ejemplo:

> Cuando se crea un nuevo elemento en una lista de SharePoint.

## Conectores estándar y Premium

Los conectores pueden clasificarse principalmente como:

- **Standard Connectors**
- **Premium Connectors**

Los conectores Premium suelen utilizarse para servicios empresariales especializados.

## Custom Connectors

Cuando no existe un conector estándar puede desarrollarse un **Custom Connector**.

Los conectores personalizados permiten integrar Power Platform con APIs propias o servicios externos mediante interfaces como OpenAPI.

---

# Plan Designer

Plan Designer es una experiencia de Power Apps asistida por inteligencia artificial que permite transformar la descripción de un problema empresarial en un **plan completo de solución de Power Platform**.

En lugar de decidir manualmente qué aplicación, flujo, tabla o agente crear, se comienza describiendo el problema.

```text
Problema empresarial
        │
        ▼
   Plan Designer
        │
        ▼
Plan de solución
        │
        ├── Power Apps
        ├── Power Automate
        ├── Dataverse
        ├── Copilot Studio
        ├── Power Pages
        └── Power BI
```

## Agentes especializados

Plan Designer utiliza distintos agentes especializados.

### Solution Agent

Analiza la solución completa y coordina sus componentes.

### Process Agent

Identifica los procesos y automatizaciones necesarias.

### Data Agent

Diseña el modelo de datos:

- Tablas.
- Columnas.
- Relaciones.

### Experience Agent

Propone las experiencias necesarias:

- Canvas Apps.
- Model-driven Apps.
- Power Pages.
- Power BI.

## Qué puede generar

A partir del plan se pueden obtener puntos de partida para:

- Canvas Apps.
- Model-driven Apps.
- Flujos de Power Automate.
- Agentes de Copilot Studio.
- Sitios de Power Pages.
- Informes de Power BI.
- Tablas de Dataverse.

## Flujo conceptual

```text
1. Describir el problema
        │
        ▼
2. Analizar procesos
        │
        ▼
3. Diseñar datos
        │
        ▼
4. Diseñar experiencias
        │
        ▼
5. Definir automatizaciones
        │
        ▼
6. Incorporar agentes
        │
        ▼
7. Revisar y refinar
        │
        ▼
8. Generar la solución
```

El proceso es **iterativo**. Los usuarios de negocio pueden validar el diseño mientras TI revisa aspectos como:

- Seguridad.
- Gobernanza.
- Acceso a datos.
- Conectores.
- Arquitectura.
- Estrategia de entornos.

---

# Cómo encajan todos los componentes

Power Platform genera su mayor valor cuando sus componentes trabajan juntos.

```text
                 ┌─────────────────┐
                 │     Usuarios    │
                 └────────┬────────┘
                          │
            ┌─────────────┼─────────────┐
            ▼             ▼             ▼
       Power Apps    Power Pages   Copilot Studio
            │             │             │
            └─────────────┼─────────────┘
                          ▼
                      Dataverse
                          │
              ┌───────────┼───────────┐
              ▼           ▼           ▼
       Power Automate  Power BI   AI Builder
              │
              ▼
          Conectores
              │
              ▼
      Sistemas externos
```

De esta manera:

- **Power Apps** proporciona las aplicaciones.
- **Power Automate** automatiza los procesos.
- **Power Pages** extiende las soluciones hacia usuarios externos.
- **Dataverse** proporciona la capa de datos.
- **Copilot Studio** proporciona agentes.
- **Power BI** proporciona análisis y visualización.
- **AI Builder** incorpora modelos de inteligencia artificial.
- **Conectores** integran sistemas y servicios.
- **Plan Designer** ayuda a diseñar la solución completa.

---

# Idea principal

Power Platform no debe entenderse como un conjunto de herramientas independientes.

Su verdadero valor aparece cuando los componentes trabajan juntos para transformar un proceso empresarial:

```text
Problema empresarial
        │
        ▼
Datos centralizados
  (Dataverse)
        │
        ├── Apps
        ├── Automatización
        ├── Portales
        ├── Agentes
        ├── IA
        └── Analytics
        │
        ▼
Solución empresarial integrada
```

El objetivo final es permitir que las organizaciones pasen más rápidamente de **problemas empresariales a soluciones digitales**, combinando **low-code, automatización, datos, integración e inteligencia artificial**.
