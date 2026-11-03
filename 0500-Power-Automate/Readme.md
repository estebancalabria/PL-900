# ⚡ PL-900 | Microsoft Power Automate

> Resumen de estudio sobre Power Automate para Microsoft Power Platform Fundamentals (PL-900).

---

## 📌 ¿Qué es Power Automate?

**Microsoft Power Automate** es una plataforma de automatización basada en la nube que permite crear procesos automáticos entre aplicaciones y servicios.

Su objetivo es reducir:

- Tareas manuales y repetitivas.
- Errores humanos.
- Copia manual de información entre sistemas.
- Seguimiento manual de aprobaciones.
- Procesos administrativos repetitivos.

Ejemplos:

- Guardar automáticamente archivos adjuntos recibidos por correo.
- Enviar notificaciones en Teams.
- Procesar formularios.
- Solicitar aprobaciones.
- Actualizar SharePoint o Dataverse.
- Ejecutar procesos todos los lunes.
- Automatizar aplicaciones de escritorio antiguas.

---

# ☁️ Flujos de nube vs. 🖥️ flujos de escritorio

Power Automate ofrece dos grandes tipos de automatización.

| Flujo | Uso principal |
|---|---|
| ☁️ **Cloud flow** | Automatizar aplicaciones y servicios conectados |
| 🖥️ **Desktop flow** | Automatizar aplicaciones de escritorio mediante RPA |

---

## ☁️ Flujos de nube

Los **flujos de nube** conectan servicios y aplicaciones para ejecutar acciones automáticamente.

Ejemplos:

```text
Llega un correo
      ↓
Guardar adjunto en SharePoint
      ↓
Solicitar aprobación
      ↓
Notificar resultado en Teams
