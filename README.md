# 🧠 Gimnasio Mental

Ejercicios de matemáticas y lógica (límites, integrales, derivadas, álgebra y lógica) generados y verificados con IA, pensados para entrenar la mente todos los días.

## Cómo funciona

- **Groq** genera un ejercicio de opción múltiple sobre el tema y dificultad elegidos.
- **Gemini** resuelve el mismo ejercicio de forma independiente (sin ver la respuesta de Groq) para verificarla. Si ambos modelos no coinciden, la app te lo advierte para que revises el razonamiento con ojo crítico.
- La dificultad puede subir o bajar sola según tu racha de aciertos (modo adaptativo).
- Las llamadas a Groq y Gemini pasan por una **Edge Function de Supabase** que guarda las API keys reales como secretos de servidor — nunca llegan al navegador ni al código de este repositorio.
- Tu progreso (aciertos, racha, mejor racha) y tu clave de acceso personal se guardan solo en el navegador de cada dispositivo (`localStorage`).

## Infraestructura

- **Sitio**: GitHub Pages, sirviendo `index.html` directamente desde `main`.
- **Backend**: proyecto Supabase `MentalGYM` (Edge Function `ai-proxy`) que hace de intermediario hacia Groq y Gemini.
- **Secretos del servidor** (se configuran en el dashboard de Supabase → Edge Functions → Secrets, nunca en este repo):
  - `GROQ_API_KEY`
  - `GEMINI_API_KEY`
  - `APP_SHARED_SECRET` — una clave personal que también debes pegar en la app (⚙️ Configuración → "Clave de acceso"). Sin ella, cualquiera que encuentre esta URL pública podría gastar tu cuota gratuita de IA.

## Usar la app

1. Abre la página publicada en GitHub Pages.
2. Pulsa ⚙️ y pega tu clave de acceso personal (la misma que configuraste como `APP_SHARED_SECRET` en Supabase).
3. Elige tema y dificultad, y pulsa "Nuevo ejercicio".

Cada dispositivo (iPhone, iPad, Mac, PC) necesita esa misma clave de acceso guardada la primera vez que lo abras ahí.

## Desarrollo local

El sitio es una página estática de un solo archivo (`index.html`), sin build ni dependencias. El backend vive aparte en Supabase (`supabase/functions/ai-proxy`, desplegado directamente al proyecto — no hay build local de la función en este repo).

## Aviso

Los ejercicios y sus explicaciones son generados por modelos de IA; pueden contener errores. Úsalo como entrenamiento y repaso, no como fuente única de verdad matemática.
