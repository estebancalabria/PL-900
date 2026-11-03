# 📘 PL-900 | Microsoft Dataverse

## 📌 Introducción

**Microsoft Dataverse** es la plataforma de datos en la nube de Microsoft Power Platform.

Permite almacenar, organizar y administrar datos empresariales de forma segura y estructurada, además de integrarlos con herramientas como:

- Power Apps
- Power Automate
- Power BI
- Dynamics 365
- Azure

Dataverse está especialmente diseñado para escenarios **low-code / no-code**, reduciendo la necesidad de desarrollar y mantener una base de datos tradicional desde cero.

### 🎯 ¿Qué problemas ayuda a resolver?

Dataverse permite:

- 📦 Organizar y centralizar datos.
- ⚙️ Automatizar procesos empresariales.
- 🔗 Integrarse con otras aplicaciones y servicios.
- 🔐 Aplicar seguridad sobre los datos.
- 📈 Crear soluciones escalables.
- 🧩 Construir aplicaciones sobre un modelo de datos común.

---

# 🆚 Dataverse vs. bases de datos tradicionales

Aunque Dataverse utiliza conceptos tradicionales como tablas, filas y columnas, incorpora muchas capacidades adicionales.

| Característica | Base de datos tradicional | Dataverse |
|---|---|---|
| Estructura | Tablas, filas y columnas | Tablas, filas y columnas + metadatos |
| Relaciones | Configuración manual | Integradas en la plataforma |
| Seguridad | Normalmente requiere configuración | Seguridad avanzada integrada |
| Desarrollo | Habitualmente requiere programación | Low-code / no-code |
| Lógica empresarial | Debe desarrollarse | Reglas de negocio, Power Fx y Power Automate |
| Integración | Depende de APIs/desarrollo | Integración con Power Platform, Dynamics 365, Azure y conectores |
| Escalabilidad | Depende de la arquitectura | Diseñado para escenarios empresariales |

## 🔐 Seguridad

Dataverse proporciona características como:

- Seguridad basada en roles.
- Control de acceso sobre filas.
- Seguridad sobre columnas.
- Cifrado.
- Control de acceso a los datos.

Esto permite controlar **quién puede acceder a qué información**.

---

# 🧩 Common Data Model (CDM)

El **Common Data Model (CDM)** proporciona esquemas estandarizados para representar conceptos empresariales comunes.

Ejemplos:

- Accounts
- Contacts
- Transactions

Estos esquemas contienen:

- Tablas
- Atributos
- Relaciones

### ¿Por qué es importante?

El CDM permite que diferentes aplicaciones utilicen estructuras de datos consistentes.

Esto facilita la interoperabilidad entre:

- Dataverse
- Dynamics 365
- Power Apps
- Azure
- Sistemas externos mediante conectores y APIs

> 💡 **Idea clave para PL-900:**  
> Dataverse proporciona almacenamiento estructurado, mientras que el Common Data Model ayuda a estandarizar cómo se representan los datos empresariales.

---

# 🗃️ Estructura de datos en Dataverse

Las **tablas** son el elemento principal para almacenar información.

Una tabla contiene:

- **Filas:** registros individuales.
- **Columnas:** propiedades o atributos del registro.

### Ejemplo

Una tabla `Pets` podría contener:

| Name | Species | Breed |
|---|---|---|
| Toby | Dog | Labrador |
| Luna | Cat | Siamese |

Cada mascota es una **fila**, mientras que `Name`, `Species` y `Breed` son **columnas**.

---

## 🆔 Clave principal

Cada fila de Dataverse dispone de un identificador único.

Dataverse utiliza un:

**GUID (Globally Unique Identifier)**

Esto permite identificar de forma única cada registro.

---

# 🔗 Relaciones entre tablas

Las relaciones permiten conectar información almacenada en diferentes tablas.

## 1️⃣ Uno a varios (1:N)

Un registro puede relacionarse con múltiples registros de otra tabla.

Ejemplos:

```text
Profesor 1 ──── N Clases
Cliente  1 ──── N Pedidos
Contact  1 ──── N Donations
