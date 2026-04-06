# AARPIA Network

> Arquitectura orientada a contexto para modelar, ejecutar y representar trabajo estructurado sobre una base **event-driven** y **Nostr-first**.

---

## 🧠 Qué es AARPIA

AARPIA es una arquitectura que separa con claridad:

- **Dominio**: define qué existe, qué puede pasar y cómo se deriva el estado
- **Microkernel**: ejecuta capacidades, aplica reglas y publica eventos y snapshots
- **Clientes**: interactúan con el sistema sin convertirse en fuente de verdad
- **Builder**: permite diseñar contextos y configurar clientes complejos
- **Agents**: permite la automatización y ejecución de agentes sobre el ecosistema AARPIA

Su base conceptual gira en torno a tres niveles del dominio:

- **Context**
- **Process**
- **Instance**

---

## ⚙️ Principios de arquitectura

AARPIA se apoya en:

- **Nostr** como capa distribuida de eventos
- **ContextVM** como runtime de capacidades e integración
- **microKernels** como nodos ejecutores
- **Caché local** para acelerar reconstrucción y consulta
- **Blossom** como vía preferente para blobs y assets en la capa de presentación

### 🔒 Regla de frontera

En AARPIA:

- el **dominio** es la verdad del sistema
- el **cliente** es la forma de interacción y representación
- el **Builder** diseña y publica clientes complejos
- el **Agents** permite la automatización y ejecución de agentes sobre el ecosistema AARPIA

Esto implica que:

- el cliente no define reglas canónicas de validación
- el cliente no define reglas canónicas de transducción
- el cliente no decide estados del dominio
- el cliente no sustituye la **StateMachine** ni el **microkernel**

---

## 🗂️ Repositorios principales

### ⚙️ `aarpia-microkernel`
Núcleo operativo del sistema.

Responsabilidades principales:

- ejecución de capacidades de dominio
- procesamiento de eventos
- evaluación de estado
- publicación de snapshots
- integración con Nostr y caché local

### 🧩 `aarpia-builder`
Sistema unificado para clientes complejos y modelado de contextos.

Responsabilidades principales:

- diseño de contextos, procesos e instancias
- configuración de clientes
- navegación, vistas, permisos y dashboards
- bootstrap y resolución de presentación
- composición dinámica sobre runtime común

### 🤖 `aarpia-agents`
Capa orientada a integraciones, automatización y flujos de agente.

Responsabilidades principales:

- ejecución o integración de agentes sobre el ecosistema AARPIA
- automatización sobre capacidades publicadas
- consumo y operación sobre eventos, snapshots y contexto activo

---

## 🚀 Contribución

Usamos una disciplina simple y obligatoria de trabajo:

- **Jira** define el trabajo
- **GitHub** contiene el código
- **Git** gestiona los cambios

### Reglas base

- las ramas de trabajo salen desde `development`
- las pull requests se abren contra `development`
- `main` queda reservada para la línea estable
- ramas, commits y PRs deben incluir el identificador de la issue de Jira
- no se trabaja directamente sobre `main`
- no se trabaja directamente sobre `development`

Consulta la guía completa de contribución en `CONTRIBUTING.md`.

---

## ✅ Estado del proyecto

AARPIA se encuentra en fase activa de evolución arquitectónica y desarrollo de MVP.

Líneas actuales de trabajo:

- consolidación del MicroKernel
- cierre del contrato mínimo de los Agents
- definición del sistema de clientes
- alineación estricta con el mapping Nostr canónico
- construcción progresiva del ecosistema Builder + Agents

---

## 🧱 Idea central

AARPIA no busca generar clientes aislados ni lógica dispersa en frontend.

Busca construir un sistema donde:

- dominio
- ejecución
- eventos
- representación

permanezcan alineados desde el principio.

> Si una pieza rompe esa frontera, no está extendiendo AARPIA. Está degradándolo.