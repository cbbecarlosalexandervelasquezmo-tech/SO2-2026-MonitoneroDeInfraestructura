# Plataforma de Monitoreo y Observabilidad de Infraestructura TI

Proyecto semestral de **Sistemas Operativos (P2)** · Carrera de Ingeniería de Sistemas · Universidad Privada Franz Tamayo (UNIFRANZ) · Cochabamba, Bolivia · Gestión 2026

**Docente:** Diego Patrick Cardenas Sejas

---

## 1. Problema

El laboratorio de la universidad no cuenta con una supervisión centralizada de su infraestructura TI. Problemas como saturación de CPU, falta de espacio en disco o caídas de conectividad se detectan solo después de afectar a los usuarios, y la revisión manual equipo por equipo dificulta la detección preventiva.

## 2. Propósito y objetivo

Implementar una plataforma de monitoreo y observabilidad que permita supervisar en tiempo real equipos y recursos tecnológicos, visualizar métricas de rendimiento y generar alertas para detectar incidentes de forma temprana.

**Objetivos específicos**
- Levantar un servidor central de monitoreo virtualizado con PRTG Network Monitor (Free Edition).
- Configurar sensores en al menos 3 equipos del laboratorio (Windows y Linux) para CPU, memoria, almacenamiento, red y disponibilidad.
- Diseñar al menos 2 dashboards y 1 mapa de red.
- Configurar y probar al menos 3 reglas de notificación (CPU, memoria y almacenamiento).
- Elaborar un Manual Técnico y un Manual de Usuario.

## 3. Usuarios

- Administradores y personal técnico del laboratorio de la universidad.
- Docente evaluador del proyecto.

## 4. Descripción general de la solución

Un servidor PRTG, ejecutado en una máquina virtual (VMware Workstation + Windows 11), recopila métricas mediante sensores y las presenta en dashboards, un mapa de red y alertas.

```
Equipos Windows / Ubuntu / dispositivos de red
        ↓
Sensores PRTG y protocolos (WMI, SNMP, SSH)
        ↓
PRTG-SERVER (VMware + Windows 11 + PRTG)
        ↓
Dashboards + Mapa de red + Alertas
        ↓
Administrador / Equipo técnico
```

**Tecnologías:** PRTG Network Monitor Free Edition · VMware Workstation · Windows 11 · Ubuntu (próxima integración) · WMI / SNMP / SSH.

## 5. Estado actual

| Componente | Estado |
|---|---|
| Servidor PRTG-SERVER (VMware + Windows 11 + PRTG) | Implementado |
| Sensores: Ping, CPU, RAM, Disco, Red | Implementado |
| Alertas (CPU, memoria, almacenamiento) | ⚙️ Configuradas (prueba de notificaciones pendiente) |
| 2 dashboards y 1 mapa de red | Implementado |
| Integración de PC Windows y Ubuntu de compañeros | Pendiente |
| Tercer dispositivo | Pendiente |
| Router / Switch (SNMP) | Pendiente |
| Servicios y aplicaciones | Pendiente |
| Manual Técnico y Manual de Usuario | Pendiente |

> Actualmente solo se monitorea el propio PRTG-SERVER. El objetivo de supervisar al menos 3 dispositivos aún no está cumplido.

## 6. Equipo

| Integrante | Responsabilidad principal |
|---|---|
| Leandro Sebastián Gonzales Mur | Líder de proyecto; coordinación, configuración del servidor y apoyo en PRTG |
| Evelyn Torrico Guevara | Administración de PRTG y documentación técnica; sensores, dashboards y alertas |
| Carlos Alexander Velasquez | Pruebas y manual de usuario; validación de sensores, notificaciones, mapas y evidencias |

Fichas individuales en la carpeta [`Grupo/`](Grupo/).

## 7. Estructura del repositorio

```
├── README.md
├── Documentacion/
│   ├── Proyecto_Diagrama_Gantt_v2.pdf       → Planificación (Gantt)
│   ├── SOP (2).pdf                          → Documento actualizado del proyecto
│   └── White_Modern_Geometric_Thesis_Defense_Presentation.pdf → Presentación (2da)
└── Grupo/                                   → Fichas de los integrantes
```

## 8. Documentación

- [Documento del proyecto (versión actualizada)](Documentacion/SOP%20(2).pdf)
- [Diagrama de Gantt](Documentacion/Proyecto_Diagrama_Gantt_v2.pdf)
- [Presentación (2da presentación, 07/10/2026)](Documentacion/White_Modern_Geometric_Thesis_Defense_Presentation.pdf)

## 9. Planificación

El Gantt cubre de agosto a diciembre de 2026: selección de herramienta y diseño (agosto–septiembre), implementación (septiembre–octubre), integración de dispositivos y pruebas (octubre–noviembre), manuales y evidencias (noviembre–diciembre) y entrega final (diciembre). Detalle en el PDF del Gantt.

## 10. Trabajo en curso

El trabajo pendiente se gestiona mediante **Issues** de este repositorio.
