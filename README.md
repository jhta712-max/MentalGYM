# 🧠 Gimnasio Mental

Ejercicios de matemáticas y lógica (límites, integrales, derivadas, álgebra y lógica) generados y verificados con IA, pensados para entrenar la mente todos los días.

## Cómo funciona

- **Groq** genera un ejercicio de opción múltiple sobre el tema y dificultad elegidos.
- **Gemini** resuelve el mismo ejercicio de forma independiente (sin ver la respuesta de Groq) para verificarla. Si ambos modelos no coinciden, la app te lo advierte para que revises el razonamiento con ojo crítico.
- La dificultad puede subir o bajar sola según tu racha de aciertos (modo adaptativo).
- Tu progreso (aciertos, racha, mejor racha) y, si lo activas, tus API keys se guardan solo en el navegador de cada dispositivo (`localStorage`) — nunca se envían a ningún servidor propio.

## Usar la app

1. Abre la página publicada en GitHub Pages.
2. Pulsa ⚙️ y pega tu API key gratuita de Groq (console.groq.com/keys) y de Gemini (aistudio.google.com/apikey).
3. Elige tema y dificultad, y pulsa "Nuevo ejercicio".

Cada dispositivo (iPhone, iPad, Mac, PC) necesita su propia API key guardada la primera vez que lo abras ahí, ya que las keys viven en el navegador de cada dispositivo, no en un servidor compartido.

## Desarrollo local

Es una página estática de un solo archivo (`index.html`), sin build ni dependencias — ábrelo directamente en cualquier navegador.

## Aviso

Los ejercicios y sus explicaciones son generados por modelos de IA; pueden contener errores. Úsalo como entrenamiento y repaso, no como fuente única de verdad matemática.
