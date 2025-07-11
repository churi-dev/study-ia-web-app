
# 🧠 Study IA – Tu asistente académico con IA

**Study IA** es una plataforma inteligente donde los usuarios pueden subir archivos (PDFs), y a partir de ellos, generar:

📚 Resúmenes claros y estructurados  
❓ Quizzes interactivos para practicar  
🗓️ Planes de estudio personalizados  
🎙️ Simulaciones de entrevistas por voz usando IA  

Todo esto integrado con tecnologías como **Gemini (IA textual)** y **ElevenLabs (voz en tiempo real)**.

---

## 🚀 Funcionalidades principales

### 📁 Subida de archivos
- El usuario sube un archivo PDF.
- El sistema lo guarda automáticamente en Google Drive.
- Se extrae el texto completo del archivo y se genera una **descripción general** con IA.

### 🧠 Generación de resúmenes
- Usando **Gemini**, se analizan los textos para generar:
  - Introducción
  - Puntos clave (en lista)
  - Conclusión
- El resumen se guarda en base de datos y puede consultarse luego.

### ❓ Quizzes personalizados
- El usuario puede generar quizzes sobre el archivo.
- Se pueden especificar cuántas preguntas desea.
- Útil para practicar antes de exámenes o reforzar conocimientos.

### 🗓️ Plan de estudio con IA
- Indica una fecha de inicio, fin y horas por día.
- Puedes elegir el **nivel de dificultad** y tipos de tareas:
  - Ejercicios
  - Lecturas
  - Resúmenes
  - Preguntas clave
- El sistema genera un plan de estudio distribuido por días.

### 🎤 Simulación de entrevista por voz
- Basado en la carrera del usuario y el rol del entrevistador (Ej. Técnico, Recursos Humanos, Inglés)
- Se genera una pregunta por IA.
- Usamos **ElevenLabs** para convertirla a voz.
- El usuario responde por voz, y la IA:
  - Transcribe la respuesta
  - Evalúa la respuesta
  - Devuelve un feedback realista.

---

## 🔧 Tecnologías utilizadas

| Tecnología           | Uso                                       |
|---------------------|-------------------------------------------|
| .NET Core Web API   | Backend principal                         |
| Google Drive API    | Almacenamiento de archivos PDF            |
| Gemini (OpenRouter) | IA generativa para resúmenes, preguntas   |
| ElevenLabs API      | Voz (Text-to-Speech y evaluación oral)    |
| SQL Server          | Base de datos relacional                  |
| Swagger / OpenAPI   | Documentación interactiva de la API       |

---

## 📦 Endpoints principales

| Método | Ruta                                | Descripción                                      |
|--------|-------------------------------------|--------------------------------------------------|
| POST   | `/api/archivo/archivo-upload`       | Subir y procesar archivo PDF                     |
| POST   | `/api/archivo/generar-resumen/{id}` | Generar resumen con IA                           |
| POST   | `/api/archivo/generate-quiz/{id}`   | Generar quiz con IA                              |
| POST   | `/api/archivo/generate-plan-studio-ia` | Generar plan de estudio personalizado         |
| GET    | `/api/archivo/listar`               | Listar todos los archivos                        |
| GET    | `/api/archivo/get/{id}`             | Obtener archivo por ID                           |
| GET    | `/api/archivo/resumen-list/{id}`    | Listar resúmenes de un archivo                   |
| POST   | `/api/archivo/generar-pregunta`     | Generar pregunta según carrera                   |
| POST   | `/api/archivo/pregunta-voz`         | Pregunta por voz (audio mp3)                     |
| POST   | `/api/archivo/evaluar-feedback`     | Evaluar respuesta en voz del usuario             |

---

## 🔥 Próximas mejoras

- [ ] Sistema de autenticación y roles (usuarios, administradores, mentores)
- [ ] Historial de estudios por usuario
- [ ] Panel web con React y dashboards de progreso
- [ ] Evaluación automática de desempeño

---
