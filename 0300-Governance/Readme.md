# 🛡️ PL-900: Seguridad, entornos, administración y ALM en Microsoft Power Platform

> Resumen de estudio sobre seguridad, entornos, administración, privacidad, accesibilidad y Application Lifecycle Management (ALM) en Microsoft Power Platform.

---

## 📚 Contenido

1. [Introducción](#-introducción)
2. [Modelo de seguridad](#-modelo-de-seguridad-de-power-platform)
3. [Microsoft Entra ID](#-autenticación-y-microsoft-entra-id)
4. [RBAC](#-control-de-acceso-basado-en-roles-rbac)
5. [DLP](#-prevención-de-pérdida-de-datos-dlp)
6. [Seguridad de los entornos](#-seguridad-de-los-entornos)
7. [Cifrado](#-cifrado-de-datos)
8. [Gobernanza](#-gobernanza)
9. [Entornos de Power Platform](#-entornos-de-power-platform)
10. [Entornos administrados](#-entornos-administrados)
11. [Centro de administración](#-centro-de-administración-de-power-platform)
12. [Portales de Power Platform](#-portales-de-power-platform)
13. [Privacidad y cumplimiento](#-privacidad-y-cumplimiento)
14. [Accesibilidad](#-accesibilidad)
15. [ALM](#-application-lifecycle-management-alm)
16. [Resumen para el examen](#-resumen-rápido-para-el-examen)

---

# 🚀 Introducción

**Microsoft Power Platform** permite crear aplicaciones, automatizaciones, análisis y soluciones empresariales manteniendo controles de seguridad, administración y cumplimiento.

La plataforma proporciona mecanismos para:

- 🔐 Proteger información confidencial.
- 👤 Gestionar identidades y permisos.
- 🛑 Evitar pérdidas de datos.
- 🌎 Controlar dónde se almacenan los datos.
- 🏢 Separar recursos mediante entornos.
- 📋 ativos.
- Comprender privacidad, cumplimiento y accesibilidad.
- Describir Application Lifecycle Management (ALM).

---

# 🔐 Modelo de seguridad de Power Platform

El modelo de seguridad combina diferentes mecanismos destinados a proteger usuarios, aplicaciones y datos.

Los principales componentes son:

| Componente | Función |
|---|---|
| Microsoft Entra ID | Identidad y autenticación |
| MFA | Verificación adicional de identidad |
| Acceso condicional | Controlar el acceso según determinadas condiciones |
| RBAC | Asignar permisos mediante roles |
| DLP | Controlar el intercambio de datos entre conectores |
| Entornos | Separar aplicaciones, datos y recursos |
| Cifrado | Proteger los datos |
| Gobernanza | Mantener control y cumplimiento |

---

# 👤 Autenticación y Microsoft Entra ID

**Microsoft Entra ID**, anteriormente conocido como Azure Active Directory, proporciona la base de identidad y autenticación de Power Platform.

Permite centralizar la administración de usuarios y controlar quién puede acceder a los recursos.

### Características importantes

- Administración centralizada de identidades.
- Autenticación segura.
- Integración con Microsoft 365 y Azure.
- Compatibilidad con **OAuth 2.0**.
- Autenticación multifactor (**MFA**).
- Directivas de **acceso condicional**.

### 🔑 MFA

La autenticación multifactor solicita más de una prueba para verificar la identidad del usuario.

Ejemplos:

- Contraseña.
- Aplicación móvil.
- Código de seguridad.
- Biometría.

Esto disminuye el riesgo de acceso no autorizado si una contraseña resulta comprometida.

### 🚦 Acceso condicional

Permite establecer reglas dependiendo de factores como:

- Ubicación.
- Usuario.
- Dispositivo.
- Nivel de riesgo.
- Red utilizada.

Por ejemplo, una organización podría impedir el acceso a información confidencial desde una red no confiable.

---

# 👥 Control de acceso basado en roles (RBAC)

**RBAC (Role-Based Access Control)** permite asignar roles de seguridad a los usuarios.

Los roles determinan:

- Qué puede hacer un usuario.
- A qué recursos puede acceder.
- Qué registros puede consultar o modificar.

Un usuario puede tener **varios roles simultáneamente**.

## Niveles de acceso

### 🌐 Entorno

Controla el acceso a recursos dentro de un entorno específico.

Ejemplo:

`Desarrollo → Pruebas → Producción`

### 📱 Aplicación

Determina qué usuarios pueden utilizar determinadas aplicaciones o componentes.

### 📄 Registro

Control detallado sobre registros individuales.

Puede determinar quién puede:

- Leer.
- Crear.
- Modificar.
- Eliminar.

### ⭐ Principio de mínimo privilegio

Los usuarios deberían recibir **únicamente los permisos necesarios para realizar sus tareas**.

Esto reduce:

- Errores accidentales.
- Cambios no autorizados.
- Riesgos de seguridad.

---

# 🛑 Prevención de pérdida de datos (DLP)

Las políticas **Data Loss Prevention (DLP)** controlan cómo pueden intercambiar datos los conectores utilizados en Power Platform.

Su objetivo es evitar que información empresarial termine accidentalmente en servicios no autorizados.

## Clasificación de conectores

### 🏢 Conectores empresariales

Conectores de confianza destinados al manejo de información empresarial.

Ejemplos:

- Microsoft Dataverse.
- SharePoint.
- SQL Server.

### 🌐 Conectores no empresariales

Servicios que pueden no estar autorizados para manejar información confidencial.

Ejemplos:

- Gmail.
- X (Twitter).

Una política DLP puede impedir que una aplicación transfiera información entre un conector empresarial y uno no empresarial.

## Alcance

Las políticas pueden aplicarse a nivel de:

- **Entorno:** afectan a un entorno determinado.
- **Inquilino:** afectan a toda la organización.

> 💡 **Para recordar:** DLP controla principalmente cómo pueden combinarse y utilizarse los conectores para evitar movimientos de datos no deseados.

---

# 🏢 Seguridad de los entornos

Los **entornos** funcionan como contenedores donde se organizan:

- Aplicaciones.
- Flujos.
- Agentes.
- Datos.
- Recursos de Dataverse.

Permiten separar recursos según:

- Proyecto.
- Departamento.
- Región.
- Seguridad.
- Etapa de desarrollo.

Por ejemplo:

```text
Desarrollo → Pruebas → Producción
