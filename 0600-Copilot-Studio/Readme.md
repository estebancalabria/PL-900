# 🤖 Microsoft Copilot Studio | PL-900

> Resumen de estudio sobre Microsoft Copilot Studio: agentes, datos, RAG, herramientas, MCP, flujos, análisis, evaluaciones y ciclo de desarrollo.

---

## 📌 ¿Qué es Microsoft Copilot Studio?

**Microsoft Copilot Studio** es una plataforma SaaS de bajo código que permite crear, implementar y administrar **agentes inteligentes** sin necesitar conocimientos avanzados de programación.

Un agente puede:

- 💬 Mantener conversaciones en lenguaje natural.
- 📚 Consultar fuentes de conocimiento.
- ⚙️ Ejecutar acciones mediante herramientas y conectores.
- 🔄 Automatizar procesos empresariales.
- 🔌 Integrarse con sistemas externos.
- 📊 Medir su uso mediante análisis integrados.
- 🔐 Respetar las políticas de seguridad y acceso de la organización.

---

# 1. Tipos de agentes

Un **agente** es una aplicación basada en IA capaz de conversar, acceder a conocimiento y realizar acciones.

Copilot Studio admite principalmente dos categorías:

| Tipo | Funcionamiento | Ideal para |
|---|---|---|
| 💬 **Conversacional** | Responde a solicitudes iniciadas por usuarios | Soporte, consultas y autoservicio |
| 🤖 **Autónomo** | Actúa proactivamente ante eventos, reglas o programaciones | Automatización y procesos repetitivos |

---

## 💬 Agentes conversacionales

Interactúan con los usuarios mediante lenguaje natural.

### Casos de uso

- **RR. HH.**
  - Vacaciones
  - Beneficios
  - Políticas
  - Incorporación

- **Soporte de TI**
  - Restablecimiento de contraseñas
  - Configuración de VPN
  - Solicitudes de software

- **Atención al cliente**
  - Preguntas frecuentes
  - Estado de pedidos
  - Devoluciones

- **Ventas**
  - Precios
  - Productos
  - Información competitiva
  - Contratos

- **Gestión del conocimiento**
  - SharePoint
  - Documentos internos
  - Wikis
  - Bases de conocimiento

---

## 🤖 Agentes autónomos

Realizan acciones sin necesitar que una persona inicie cada paso.

Pueden ejecutarse:

- Según una programación.
- Ante un evento desencadenador.
- Como parte de un proceso de varios pasos.

### Casos de uso

- 🎯 Calificación de clientes potenciales.
- 📄 Procesamiento de contratos.
- 💰 Procesamiento de facturas y gastos.
- 📦 Supervisión de la cadena de suministro.
- 🛡️ Cumplimiento y auditoría.

> **Idea clave:**  
> Conversacional = el usuario pregunta y el agente responde.  
> Autónomo = ocurre algo y el agente puede actuar.

---

# 2. Cómo Copilot Studio usa los datos

Copilot Studio está diseñado teniendo en cuenta la **protección de los datos empresariales**.

## ☁️ Datos dentro de la nube de Microsoft

Copilot Studio utiliza servicios de Microsoft y Azure.

Los datos empresariales conectados a los agentes se utilizan para generar respuestas y trabajar con ellos dentro del contexto de la organización.

Según el contenido del módulo:

- Las indicaciones y respuestas no se utilizan para entrenar los modelos fundamentales.
- Los datos de la organización no se comparten con otras organizaciones.
- Se aplican controles de seguridad empresariales.

---

# 3. RAG: Retrieval-Augmented Generation

Copilot Studio utiliza **RAG** para generar respuestas fundamentadas en el conocimiento disponible.

RAG funciona en tres etapas:

### 1️⃣ Recuperación

Busca información relevante en fuentes como:

- SharePoint
- Sitios web
- Dataverse
- Archivos
- Otras fuentes conectadas

### 2️⃣ Aumento

Combina:

```text
Pregunta del usuario
        +
Contenido recuperado
        ↓
Contexto para el modelo
```

### 3️⃣ Generación

El modelo utiliza ese contexto para producir una respuesta fundamentada.

> **RAG = Recuperar → Aumentar → Generar**

---

# 4. Seguridad y acceso

Copilot Studio utiliza el modelo de seguridad de **Power Platform**.

## 👤 Acceso a nivel de usuario

Los agentes respetan los permisos del usuario autenticado.

Si un usuario no puede acceder a determinado contenido protegido, el agente tampoco debería utilizarlo en nombre de ese usuario.

## 🛡️ DLP

Las políticas **Data Loss Prevention (DLP)** de Power Platform se aplican a Copilot Studio.

Si un conector está bloqueado por una política DLP, el agente no puede utilizarlo.

## 🔒 Customer Lockbox

Copilot Studio admite mecanismos de seguridad que pueden requerir autorización antes de que personal de soporte de Microsoft acceda a determinados datos del cliente.

## 🧠 IA responsable

Se aplican filtros de seguridad y moderación de contenido.

Los creadores también pueden añadir:

- Instrucciones.
- Restricciones de ámbito.
- Guardrails.
- Escalación hacia personas.

---

# 5. Flujo de datos de Copilot Studio

El flujo simplificado de una conversación es:

```text
Usuario
  ↓
Mensaje
  ↓
Orquestación
  ↓
Conocimiento / Herramientas
  ↓
Modelo de IA
  ↓
Filtros de seguridad
  ↓
Respuesta
  ↓
Registro y analítica
```

## Paso 1: mensaje

El usuario envía una solicitud desde un canal publicado.

## Paso 2: orquestación

Copilot Studio determina cómo responder.

Puede utilizar:

### Orquestación basada en temas

Relaciona el mensaje con frases de activación y ejecuta un flujo definido.

### Orquestación generativa

La IA decide dinámicamente si debe:

- Consultar conocimiento.
- Ejecutar una herramienta.
- Invocar un tema.
- Solicitar información adicional.

## Paso 3: conocimiento

Si necesita información, recupera contenido relevante de las fuentes configuradas.

## Paso 4: herramientas

Si necesita realizar una acción, ejecuta una herramienta.

Por ejemplo:

```text
Usuario: "¿Cuántos días de vacaciones tengo?"

Agente
  ├─ Consulta política en SharePoint
  └─ Consulta saldo mediante Dataverse
        ↓
Combina resultados
        ↓
Respuesta
```

## Paso 5: generación

La IA combina:

- Mensaje del usuario.
- Conocimiento recuperado.
- Resultados de herramientas.
- Instrucciones del agente.

## Paso 6: respuesta y registro

La respuesta se entrega al usuario y determinados datos de la interacción pueden alimentar la analítica del agente.

---

# 6. Canales de publicación

Un agente puede publicarse en diferentes canales:

- 💬 Microsoft Teams
- 🧠 Microsoft 365 Copilot
- 🌐 Sitios web
- 📚 SharePoint
- 🔌 Aplicaciones personalizadas mediante Direct Line

---

# 7. Conocimiento vs. herramientas

Esta diferencia es fundamental.

> 📚 **Conocimiento = lo que el agente puede consultar y razonar.**  
> 🛠️ **Herramientas = lo que el agente puede hacer.**

---

## 📚 Fuentes de conocimiento

Copilot Studio puede utilizar distintas fuentes:

### SharePoint

- Sitios
- Bibliotecas
- Documentos

### Sitios web públicos

Útiles para:

- Documentación pública
- Productos
- Marketing
- Soporte

### Archivos

Por ejemplo:

- PDF
- Word
- Hojas de cálculo

### Dataverse

Permite utilizar registros empresariales estructurados.

Ejemplos:

- Clientes
- Productos
- Casos
- Cuentas

### Conectores personalizados

Pueden proporcionar acceso a sistemas empresariales externos.

---

# 8. Herramientas

Las herramientas permiten que el agente **realice acciones**.

Entre las categorías estudiadas se encuentran:

1. 🔌 Conectores de Power Platform
2. 🔄 Flujos de agente
3. 🧩 Servidores MCP
4. ✍️ Prompts personalizados
5. 🖥️ Computer-Using Agents (CUA)
6. 🤖 Agentes secundarios

---

# 9. Model Context Protocol (MCP)

**MCP, Model Context Protocol**, es un estándar abierto para conectar agentes y modelos de IA con herramientas, datos y servicios externos.

Un **servidor MCP** expone capacidades que el agente puede descubrir y utilizar.

```text
Agente
   ↓
Servidor MCP
   ├── Datos
   ├── Consultas
   ├── Acciones
   └── Operaciones
```

El servidor describe:

- Qué operaciones existen.
- Qué parámetros necesitan.
- Qué datos devuelven.

La IA puede decidir durante la ejecución qué operaciones utilizar.

---

## 🗃️ MCP de Dataverse

El servidor MCP de Dataverse permite interactuar con información estructurada.

Entre sus operaciones se incluyen:

| Operación | Función |
|---|---|
| List tables | Descubrir tablas |
| Describe table | Consultar el esquema |
| Read data | Leer registros |
| Create record | Crear registros |
| Update record | Actualizar registros |
| List prompts | Enumerar prompts |
| Execute prompt | Ejecutar un prompt |
| List knowledge sources | Descubrir fuentes |
| Retrieve knowledge | Recuperar conocimiento |

Ejemplo:

```text
Pregunta del usuario
      ↓
List tables
      ↓
Describe table
      ↓
Read data
      ↓
Respuesta
```

---

## 🔌 MCP de terceros

Copilot Studio puede conectarse con servidores MCP personalizados o de terceros para integrar sistemas empresariales.

Ejemplos estudiados:

- GitHub
- Jira
- Confluence
- SAP
- ServiceNow
- Salesforce

Las conexiones MCP también están sujetas a la **gobernanza DLP de Power Platform**.

---

# 10. Supervisión y análisis

Publicar un agente no termina el proyecto.

El ciclo real es:

```text
Crear → Publicar → Medir → Mejorar → Evaluar → Repetir
```

Copilot Studio proporciona análisis para comprender cómo se utiliza un agente.

---

## 📊 Métricas principales

### Total de sesiones

Cantidad de sesiones atendidas.

### Tasa de participación

Sesiones en las que el usuario interactúa realmente con el agente.

### Tasa de resolución

Porcentaje de sesiones resueltas sin escalación.

### Tasa de escalación

Sesiones transferidas hacia asistencia humana u otro proceso definido.

### Tasa de abandono

Usuarios que dejan la conversación antes de resolver su necesidad.

---

## 📚 Análisis de temas

Permite identificar:

- Temas frecuentes.
- Temas con alto abandono.
- Temas con alta escalación.
- Áreas donde falta conocimiento.

---

## ⭐ CSAT

**Customer Satisfaction Score** permite analizar la satisfacción de los usuarios cuando existe una encuesta configurada.

---

## 👥 Usuarios activos

Puede realizar seguimiento de:

- **DAU:** Daily Active Users.
- **MAU:** Monthly Active Users.

Estas métricas ayudan a determinar si la adopción:

- 📈 Crece.
- ➡️ Se mantiene.
- 📉 Disminuye.

---

## 📐 Métricas personalizadas

Los creadores pueden definir métricas relacionadas con resultados empresariales específicos.

Por ejemplo:

> "¿Con qué frecuencia los usuarios solicitan hablar con un especialista?"

---

# 11. Flujos de agente

Los **flujos de agente** son automatizaciones deterministas que un agente puede utilizar como herramientas.

A diferencia de una respuesta generativa, siguen pasos definidos.

> **IA generativa = flexible**  
> **Flujo de agente = predecible y determinista**

---

## ¿Cuándo utilizar un flujo?

### ✅ Utilizar flujo

- Calcular comisiones mediante reglas fijas.
- Registrar solicitudes de vacaciones.
- Crear registros.
- Ejecutar procesos con aprobaciones.
- Reordenar inventario bajo cierto umbral.

### ❌ Preferir comportamiento generativo

- Responder preguntas abiertas.
- Consultar políticas.
- Resumir documentos.
- Explicar información.
- Responder preguntas generales de incorporación.

---

## Capacidades

Los flujos pueden utilizar:

- 🔌 Conectores de Power Platform.
- 🧮 Power Fx.
- ✅ Aprobaciones.
- 🧱 Condiciones.
- 📥 Parámetros de entrada.
- 📤 Variables de salida.
- 🔔 Notificaciones.
- 🗃️ Sistemas externos.

Ejemplo:

```text
Empleado solicita vacaciones
        ↓
Agente recopila información
        ↓
Invoca flujo
        ↓
Valida fechas
        ↓
Comprueba saldo
        ↓
Registra solicitud
        ↓
Envía confirmación
        ↓
Devuelve resultado al agente
```

---

# 12. Proceso de desarrollo de un agente

Microsoft propone un proceso estructurado en **5 fases**:

```text
1. Visión y diseño
       ↓
2. Compilación
       ↓
3. Evaluación
       ↓
4. Implementación
       ↓
5. Supervisión y mejora
       ↺
```

---

## 1️⃣ Visión y diseño

Responder cuatro preguntas:

### ¿Cuál es el caso de uso?

Definir:

- Problema.
- Usuarios.
- Objetivo.

### ¿Qué datos necesita?

Identificar:

- SharePoint.
- Dataverse.
- Sistemas externos.
- Documentos.

### ¿Qué acciones realizará?

Determinar:

- Automatizaciones.
- Herramientas.
- Aprobaciones humanas.

### ¿Cómo mediremos el éxito?

Ejemplos:

- Tasa de resolución.
- CSAT.
- Reducción de tickets.
- Tiempo ahorrado.
- Tasa de escalación.

---

## 2️⃣ Compilación

Proceso típico:

1. Crear el agente.
2. Definir propósito.
3. Configurar instrucciones.
4. Agregar conocimiento.
5. Configurar herramientas.
6. Crear temas.
7. Probar iterativamente.

---

## 3️⃣ Evaluación

Antes de publicar, es importante medir formalmente la calidad del agente.

### Conjuntos de pruebas

Un **test set** contiene casos de prueba.

Cada caso puede tener:

```text
Entrada del usuario
        ↓
Respuesta del agente
        ↓
Respuesta esperada
        ↓
Evaluación
```

Un conjunto puede contener **hasta 100 casos de prueba**, según el contenido del módulo.

### Creación de pruebas

Pueden crearse mediante:

- ✏️ Creación manual.
- 🤖 Generación mediante IA.
- 📄 Importación CSV.

---

## Tipos de evaluación

### Respuesta única

Evalúa una pregunta y una respuesta.

Ideal para:

- FAQs.
- Recuperación de conocimiento.
- Exactitud.

### Conversaciones multiturno

Evalúan conversaciones completas.

Ideal para:

- Mantener contexto.
- Seguimientos.
- Procesos de varios pasos.

---

## Métodos de evaluación

| Método | Comprueba |
|---|---|
| **Calidad** | Precisión, relevancia y completitud |
| **Similitud** | Cercanía semántica con la respuesta esperada |
| **Coincidencia de texto** | Presencia de contenido específico |
| **Uso de herramientas** | Si se ejecutó la herramienta o tema correcto |

La evaluación de **Calidad** puede devolver una puntuación de:

```text
0 ─────────────────── 1
Mala               Excelente
```

El creador puede establecer un umbral de aprobación.

Ejemplo:

```text
Umbral = 0.7

0.85 → ✅ Aprobado
0.72 → ✅ Aprobado
0.61 → ❌ Revisar
```

---

# 13. Implementación

Una vez alcanzado el nivel de calidad requerido, el agente puede desplegarse.

Un enfoque recomendado es:

1. Realizar pruebas.
2. Ejecutar evaluaciones.
3. Implementar mediante procesos gobernados.
4. Comenzar con un grupo piloto.
5. Recoger feedback.
6. Corregir problemas.
7. Ampliar el despliegue.

En el ejemplo estudiado se utiliza un piloto de aproximadamente **20 a 50 usuarios**.

---

# 14. Supervisión y mejora continua

Después de publicar:

### Alto abandono

Puede indicar:

- Respuestas poco útiles.
- Falta de conocimiento.
- Problemas de conversación.

### Alta escalación

Puede indicar:

- Limitaciones del agente.
- Procesos que todavía requieren intervención humana.

### Transcripciones

Permiten descubrir cómo preguntan realmente los usuarios.

Esto puede ayudar a:

- Mejorar instrucciones.
- Agregar conocimiento.
- Corregir temas.
- Agregar herramientas.
- Crear nuevos casos de prueba.

---

# 15. Construcción práctica de un agente

Un proceso práctico puede ser:

## Paso 1: describir el agente

Ejemplo:

> Crear un agente de soporte de TI para empleados que responda preguntas sobre VPN, contraseñas y acceso a software, y pueda crear tickets cuando sea necesaria la intervención del equipo de TI.

## Paso 2: configurar instrucciones

Definir:

- Rol.
- Ámbito.
- Tono.
- Restricciones.
- Comportamiento cuando no conoce la respuesta.

Ejemplo:

```text
Rol: asistente de soporte de TI.

Tono: profesional, amable y conciso.

Ámbito:
- VPN
- Contraseñas
- Software corporativo

Si no puedes resolver el problema:
- Ofrece crear un ticket.

No respondas preguntas fuera del ámbito de soporte de TI.
```

---

## Paso 3: agregar conocimiento

Ejemplo:

```text
SharePoint
   ├── VPN
   ├── Contraseñas
   ├── Software
   └── Políticas de TI
```

---

## Paso 4: configurar herramientas

Ejemplo:

Una herramienta de Dataverse para crear un ticket.

Parámetros:

```text
Nombre
Descripción del problema
Prioridad
```

---

## Paso 5: probar

Casos de prueba:

```text
"¿Cómo puedo conectarme a la VPN?"
```

Esperado:

> Consulta el conocimiento y devuelve instrucciones.

```text
"Mi contraseña expiró."
```

Esperado:

> Recupera el procedimiento correspondiente.

```text
"Necesito hablar con alguien de TI."
```

Esperado:

> Ofrece crear un ticket y solicita la información necesaria.

---

## Paso 6: evaluar

Ejemplo de evaluación:

```text
10 casos de prueba
      ↓
Evaluador de calidad
      ↓
Umbral: 0.7
      ↓
Analizar errores
      ↓
Corregir
      ↓
Volver a evaluar
```

---

## Paso 7: publicar

Puede publicarse, por ejemplo, en **Microsoft Teams** para que los empleados interactúen directamente con él.

Después:

```text
Publicar
   ↓
Analizar
   ↓
Encontrar problemas
   ↓
Mejorar
   ↓
Evaluar nuevamente
```

---

# 🧠 Conceptos clave para recordar

| Concepto | Idea principal |
|---|---|
| **Copilot Studio** | Plataforma low-code para crear agentes |
| **Agente conversacional** | Responde a interacciones iniciadas por usuarios |
| **Agente autónomo** | Actúa ante eventos o procesos |
| **RAG** | Recupera conocimiento y lo utiliza para generar respuestas |
| **Knowledge** | Lo que el agente sabe/consulta |
| **Tools** | Lo que el agente puede hacer |
| **MCP** | Estándar para conectar agentes con herramientas y datos |
| **Agent Flow** | Automatización determinista |
| **Generative orchestration** | La IA decide dinámicamente cómo responder |
| **DLP** | Controla qué conectores y datos pueden combinarse/utilizarse |
| **CSAT** | Satisfacción del usuario |
| **DAU / MAU** | Usuarios activos diarios/mensuales |
| **Test Set** | Colección de casos de prueba |
| **Evaluation** | Medición formal del comportamiento del agente |

---

# ⚡ Chuleta rápida PL-900

```text
CONOCIMIENTO
"El agente necesita saber algo"
        ↓
SharePoint / Web / Files / Dataverse

HERRAMIENTA
"El agente necesita hacer algo"
        ↓
Connector / Flow / MCP / Agent

RAG
Pregunta
   ↓
Retrieve
   ↓
Augment
   ↓
Generate

AGENTE CONVERSACIONAL
Usuario → Agente → Respuesta

AGENTE AUTÓNOMO
Evento → Agente → Acción

FLUJO
Proceso exacto y predecible
        ↓
Agent Flow

ORQUESTACIÓN GENERATIVA
Decisión dinámica
        ↓
IA

DESARROLLO
Diseñar
  ↓
Construir
  ↓
Evaluar
  ↓
Implementar
  ↓
Supervisar
  ↺
```

---

# 🎯 Puntos que conviene memorizar

1. **Conocimiento y herramientas no son lo mismo.**
   - Conocimiento → consultar información.
   - Herramientas → ejecutar acciones.

2. **RAG tiene tres fases.**
   - Retrieval.
   - Augmentation.
   - Generation.

3. **Conversacional y autónomo tienen propósitos distintos.**
   - Conversacional → responde.
   - Autónomo → actúa proactivamente.

4. **Los flujos son deterministas.**
   - Son preferibles cuando las reglas deben ejecutarse siempre de la misma manera.

5. **La orquestación generativa es dinámica.**
   - Puede decidir qué conocimiento, herramienta o tema utilizar.

6. **MCP conecta agentes con capacidades externas.**
   - El agente puede descubrir las operaciones disponibles y decidir cuáles utilizar.

7. **DLP también afecta a los agentes.**
   - La gobernanza de Power Platform sigue siendo relevante.

8. **Un agente no termina al publicarse.**
   - La analítica y las evaluaciones permiten mejorarlo continuamente.

9. **Las evaluaciones evitan regresiones.**
   - Conviene evaluar antes y después de introducir cambios importantes.

10. **El ciclo completo es:**

   **Diseñar → Construir → Evaluar → Implementar → Supervisar → Mejorar**

---

## 📚 PL-900

Este documento forma parte de mis apuntes personales de preparación para **Microsoft Power Platform Fundamentals (PL-900)**.

> 💡 **Tip de estudio:** más que memorizar cada característica de Copilot Studio, intenta distinguir qué componente utilizarías ante un escenario: **conocimiento, herramienta, flujo, MCP, agente conversacional o agente autónomo**.
