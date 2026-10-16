# ⚖️ LexCore IA — Suite Integral de Operaciones Jurídicas

> **Plataforma LegalTech de alto desempeño para bufetes jurídicos y despachos de litigio.**  
> Arquitectura con *Zero-Data Retention* (Cero Retención Local), Control de Acceso Basado en Roles (RBAC), Rayos X de Expedientes y Bóveda Puente con Google Drive API v3.

---

## 🏛️ Características Principales

### 1. 🔐 Autenticación & Control de Acceso (RBAC)
- **Usuario Semilla Maestro:** `admin` / `admin`.
- Pantalla de inicio de sesión con visualizador interactivo de contraseña (👁️).
- Menú lateral y vistas con visibilidad reactiva según la matriz de permisos de cada usuario.

### 2. 🛡️ Mando Central (Panel de Administrador)
- **A. Seguridad del Administrador:** Cambio de contraseña maestra con validación reactiva en tiempo real.
- **B. Gestión de Usuarios y Permisos:** Alta de abogados y personal con doble confirmación de clave y asignación granular de módulos permitidos.
- **C. Bóveda Cloud (Google Drive API v3):** Conmutador maestro (Modo Efímero vs Modo Puente Drive) con reglas de enrutamiento automatizado por cliente o abogado.

### 3. 📋 Módulo 1: Triaje Jurídico (LegalTriage)
- Calificador de viabilidad procesal con semáforo inteligente (Verde / Amarillo / Rojo).
- Estimación probabilística de éxito basada en carga probatoria, cuantía y urgencia.
- Generación de **Propuesta Formal de Servicios y Ruta Crítica** (Fases I a IV).
- Descarga en PDF membretado en el cliente vía `jsPDF` y purga inmediata de memoria.

### 4. 🔬 Módulo 2: Auditoría de Casos (JurisSearch)
- Ingestión de expedientes y contratos por *Drag & Drop* o texto directo.
- Detección automática de titulares y entidades jurídicas.
- **4 Acciones Rápidas de 1 Clic:**
  1. 🔍 Detectar Contradicciones y Lagunas.
  2. ⚠️ Auditar Cláusulas Abusivas y Riesgos (con redacción protectora sugerida).
  3. 📅 Línea de Tiempo Cronológica Procesal.
  4. ⚖️ Abogado del Diablo (Simular excepciones y estrategia de la contraparte).
- Interrogatorio interactivo efímero con el expediente.

### 5. ✍️ Módulo 3: Redactor Procesal (LexFlow IA)
- Plantillas jurídicas: Juicios Ejecutivos Mercantiles, Demandas de Amparo Indirecto, Contestaciones, Contratos de Servicios y Convenios de Confidencialidad (NDA).
- Selector de tono dialéctico (Litigioso / Conciliador / Institucional).
- Editor en vivo con estructura formal: Proemio, Hechos, Derecho, Puntos Petitorios y Protesto de Ley.

### 6. ⚡ Suite de Herramientas Auxiliares
1. **🎙️ Dictado Jurídico por Voz:** Web Speech API nativa con botón de *"✨ Formalizar a Jerga Jurídica"*.
2. **⏳ Cómputo de Términos Judiciales:** Excluye sábados, domingos y días festivos oficiales de ley.
3. **🗣️ Traductor Legal a Cliente:** Convierte acuerdos judiciales complejos en mensajes claros para WhatsApp.
4. **🛡️ Anonimizador / Testado Automático:** Enmascara RFC, CURP, montos, teléfonos y domicilios.

---

## 🚀 Despliegue e Inicio Rápido

### Requisitos:
- Navegador web moderno (Chrome, Edge, Firefox, Safari).
- Node.js (opcional, para el servidor local).

### Ejecutar Localmente:
```bash
# Iniciar servidor local
node server.js 8080
```
Abrir en el navegador: [http://localhost:8080](http://localhost:8080)

---

## 🔒 Política de Privacidad Efímera
LexCore IA no almacena expedientes, contratos ni consultas en `localStorage` o bases de datos locales. Cada análisis se ejecuta en la memoria volátil de la sesión y se destruye automáticamente al descargar el PDF o reiniciar el módulo.
