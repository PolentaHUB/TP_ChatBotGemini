# Chatbot Gemini – Proyecto

Este proyecto implementa un **chatbot de consola** utilizando la API de **Google Gemini**, siguiendo las prácticas vistas en la clase. El bot cuenta con memoria de conversación, cambio de roles, manejo de errores con reintentos y una estructura modular clara.

---

## 📂 Estructura del proyecto

```
chatbot-gemini/
├─ .env.example         # Variables de entorno de ejemplo
├─ requirements.txt     # Librerías necesarias
├─ README.md            # Documentación del proyecto
├─ config.py            # Configuración centralizada
├─ prompts.py           # Construcción de prompts
├─ memory.py            # Memoria de la conversación
├─ roles.py             # Roles predefinidos (profesor, traductor, etc.)
├─ llm_client.py        # Cliente para la API de Gemini
├─ chat_service.py      # Lógica principal del chatbot
└─ main.py              # Interfaz de consola
```

---

## ⚙️ Instalación

1. **Clonar el repositorio**:

```bash
git clone https://github.com/tu_usuario/chatbot-gemini.git
cd chatbot-gemini
```

2. **Crear y activar un entorno virtual**:

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/macOS
source venv/bin/activate
```

3. **Instalar dependencias**:

```bash
pip install -r requirements.txt
```

4. **Configurar variables de entorno**:

Copiar `.env.example` a `.env` y completar con tu clave de Gemini:

```env
GEMINI_API_KEY=tu_clave
MODEL=gemini-2.5-flash
MAX_RETRIES=3
TIMEOUT_SECONDS=30
MAX_HISTORY=12
SYSTEM_NAME=Chatbot-Gemini-Local
```

---

## ▶️ Uso

Ejecutar el chatbot en consola:

```bash
python main.py
```

Durante la ejecución, se pueden usar comandos:

* `:rol profesor|traductor|programador|asistente` → cambia el rol del bot.
* `:reset` → borra la memoria de la conversación.
* `:salir` → finaliza el programa.

---

## 🎭 Roles disponibles

* **Profesor** → Explica de forma clara y con ejemplos, resume con bullets.
* **Traductor** → Traducción fiel, mantiene formato y tono.
* **Programador** → Responde como desarrollador senior, con buenas prácticas.
* **Asistente** → Ayuda general, respuestas claras y directas.

---


## 🧑‍💻 Autor

Luca Poblete – Proyecto realizado en el marco de la clase Modelado de software .
