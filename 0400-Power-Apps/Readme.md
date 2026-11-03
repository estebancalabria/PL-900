# 📱 Microsoft Power Apps | Resumen PL-900

## 1. ¿Qué es Power Apps?

**Microsoft Power Apps** es una plataforma **low-code / no-code** que permite crear aplicaciones empresariales personalizadas para:

- Digitalizar procesos manuales.
- Reemplazar formularios y procesos en papel.
- Modernizar flujos de trabajo.
- Conectar información procedente de diferentes sistemas.
- Automatizar tareas empresariales.
- Consultar y modificar información desde aplicaciones web y móviles.

Power Apps puede utilizarse tanto para soluciones sencillas, como formularios de inspección, como para soluciones empresariales más complejas relacionadas con ventas, inventario, atención al cliente o gestión de activos.

---

## 2. Power Apps y los datos

Una de las principales ventajas de Power Apps es su capacidad de trabajar con información almacenada en diferentes servicios.

Entre los orígenes de datos habituales encontramos:

- **Microsoft Dataverse**
- **SharePoint**
- **Dynamics 365**
- **SQL Server**
- **Azure SQL**
- **Microsoft 365 / Office 365**

Una aplicación no está limitada a un único origen de datos. Puede combinar información procedente de múltiples servicios.

> 💡 **Idea clave para PL-900:** Power Apps permite crear una única aplicación que interactúe con datos procedentes de diferentes sistemas.

---

# 3. Tipos principales de aplicaciones

Power Apps dispone de dos tipos principales de aplicaciones:

1. **Aplicaciones de lienzo (Canvas Apps)**
2. **Aplicaciones basadas en modelo (Model-driven Apps)**

La elección depende principalmente de:

- El origen de los datos.
- El nivel de personalización de la interfaz.
- El proceso empresarial que queremos resolver.

---

# 🎨 4. Aplicaciones de lienzo | Canvas Apps

Las **Canvas Apps** ofrecen al creador un gran control sobre la interfaz y el comportamiento de la aplicación.

El desarrollo comienza principalmente desde la **experiencia de usuario y las tareas que debe realizar el usuario**.

## Características principales

- Interfaz altamente personalizable.
- Diseño mediante controles de arrastrar y colocar.
- Uso de **Power Fx** para implementar lógica.
- Power Fx utiliza expresiones similares a las fórmulas de Excel.
- Permiten conectarse a múltiples orígenes de datos.
- Pueden ejecutarse desde navegador o dispositivos móviles.
- Pueden aprovechar características del dispositivo, como la cámara.
- Pueden incorporarse en otros servicios.

Por ejemplo:

- SharePoint
- Power BI
- Microsoft Teams
- Aplicaciones basadas en modelo

## Creación de aplicaciones

Las Canvas Apps se pueden construir utilizando datos existentes procedentes, por ejemplo, de Excel o SharePoint.

También se puede utilizar **Copilot** para describir mediante lenguaje natural la aplicación que queremos crear y generar una aplicación inicial.

Power Apps también permite trabajar con diseños procedentes de **Figma**.

📚 [Diseñar una aplicación de lienzo mediante Figma](https://learn.microsoft.com/es-es/training/modules/design-canvas-app-figma/)

## ¿Cuándo utilizar una Canvas App?

Son especialmente apropiadas para aplicaciones:

- Orientadas a una tarea concreta.
- Utilizadas sobre el terreno.
- Que necesitan una interfaz muy personalizada.
- Que necesitan utilizar capacidades del dispositivo.
- Que necesitan combinar múltiples fuentes de datos.

### Ejemplo

Un agente inmobiliario podría utilizar una Canvas App para:

1. Buscar propiedades disponibles.
2. Consultar información sobre ellas.
3. Registrar nuevas propiedades.
4. Tomar fotografías desde el teléfono.
5. Programar jornadas de puertas abiertas.

> 🧠 **Regla mental:**  
> `Canvas App = tarea específica + interfaz personalizada + múltiples fuentes de datos`

---

# 🏢 5. Aplicaciones basadas en modelo | Model-driven Apps

Las **Model-driven Apps** siguen un enfoque centrado principalmente en los **datos y procesos empresariales**.

A diferencia de las Canvas Apps:

> ⚠️ Las aplicaciones basadas en modelo utilizan **Microsoft Dataverse** como plataforma de datos.

La aplicación se construye a partir de la estructura existente en Dataverse.

## Elementos habituales

Una Model-driven App integra componentes como:

- Tablas
- Formularios
- Vistas
- Gráficos
- Paneles
- Relaciones
- Reglas de negocio
- Procesos empresariales

Su interfaz es dinámica y adaptable, por lo que puede utilizarse desde:

- Navegador
- Tablet
- Teléfono móvil

## Casos de uso

Son especialmente apropiadas para aplicaciones de:

- Gestión
- Administración
- CRM
- Seguimiento de solicitudes
- Gestión de activos
- Gestión de ventas
- Gestión del servicio al cliente
- Procesos empresariales complejos

### Ejemplo

Una organización puede recibir incidencias de soporte mediante una Canvas App.

Los responsables podrían utilizar posteriormente una **Model-driven App** para:

- Consultar las incidencias.
- Asignarlas a técnicos.
- Gestionar su resolución.
- Analizar resultados.
- Consultar gráficos y paneles.
- Supervisar el rendimiento general.

---

# 🧱 6. Estructura de una Model-driven App

Una aplicación basada en modelo se organiza principalmente mediante:

## Aplicaciones

Colecciones de funcionalidades destinadas a determinadas actividades.

Ejemplos:

- Aplicación de ventas.
- Aplicación de servicio al cliente.
- Aplicación de gestión de activos.

## Áreas

Subdivisiones de una aplicación dedicadas a un conjunto concreto de actividades.

Ejemplo:

```text
Aplicación
├── Ventas
│   ├── Productos
│   ├── Oportunidades
│   └── Pedidos
│
└── Configuración
    └── Opciones administrativas
