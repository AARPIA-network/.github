# Contribuir en AARPIA

Gracias por contribuir. Aquí no venimos a improvisar ramas raras ni a dejar PRs arqueológicos.  
La idea es simple: **orden, trazabilidad y merges limpios**.

---

## 🧾 Regla de oro

- **Jira** = qué hacer
- **GitHub** = código
- **Git** = cambios

---

## 🌳 Estructura de ramas

### Principales
- `main`
- `development`

### Trabajo
- `feature/AAR-123-nombre-corto`

---

## 🏷️ Convenciones obligatorias

### 🌿 Rama
```bash
feature/AAR-123-nombre-corto
```

## 💬 Commit

`AAR-123: descripción breve`

## 🔀 Pull Request

`[AAR-123] Descripción breve`

## 🔁 Flujo de trabajo

### 1. El PM crea la tarea en Jira

- se crea la issue
- se asigna responsable
- estado inicial: `To Do`

### 2. El dev toma la tarea

- cambia la issue a `In Progress`

### 3. Preparar entorno

```bash
git checkout development
git pull origin development
```

### 4. Crear rama

```bash
git checkout -b feature/AAR-123-mi-rama
git push -u origin feature/AAR-123-mi-rama
```

### 5. Desarrollar

```bash
git add .
git commit -m "AAR-123: mi cambio"
git push
```

### 6. Actualizar rama antes del PR

```bash
git fetch origin
git checkout feature/AAR-123-mi-rama
git merge origin/development
git push
```

### 7. Crear PR

- Base: `development`
- Compare: `feature/...`

Incluye:

- qué hace
- qué toca
- cómo probar

### 8. Review

- se revisa el PR
- si hay cambios, se corrigen en la misma rama

### 9. Merge

- merge hacia `development`
- método recomendado: **Squash and merge**

### 10. Cierre

- Jira → `Done`
- borrar rama remota

### 11. Limpieza local

```bash
git checkout development
git pull origin development
git branch -d feature/AAR-123-mi-rama
```

## 🚫 Prohibido

- trabajar directamente en `main`
- trabajar directamente en `development`
- crear ramas sin ID de Jira
- abrir PRs sin actualizar la rama antes
- hacer commits sin ID de Jira
- usar GitHub Issues en paralelo
- inventar nombres creativos “porque se entiende”

## ✅ Resumen corto

1. Jira define la tarea
2. rama desde development
3. desarrollo en `feature/...`
4. PR contra development
5. review
6. squash merge
7. cerrar Jira
8. limpiar rama