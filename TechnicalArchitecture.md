# Technical Architecture

Este documento describe la arquitectura tecnológica básica que soporta el proyecto. Integra ideas anteriores sobre bases de datos y análisis sonoro con la nueva lógica de **playlists dinámicas**.

1. **Extracción de datos**:  
   - Usar la **API de Spotify** o herramientas tipo Exportify (mencionadas en [[Bases_de_Datos_y_Analisis_Sonoro]]) para obtener BPM, energía, danceability, etc.

2. **Almacenamiento**:  
   - Opción de llamar a la API en tiempo real (prototipo inicial).
   - Opción de **cachear** datos en un archivo JSON o en una BD (ej. Supabase), de acuerdo a la escala.

3. **Generador de playlists**:  
   - Sistema que filtra canciones según criterios de branding musical (ver [[Branding_Musical_y_Segmentacion]]) y eventos especiales (ver [[Ciclos_Tematicos_y_Experiencias]]).
   - Ajustable mediante sliders de energía, BPM y más (ver [[DynamicPlaylist]]).

4. **Interfaz y reproductor**:  
   - Emplear un **dashboard** para el dueño, con sliders y configuración.  
   - Integrar el **Spotify Web Playback SDK** (ver [[SpotifyIntegration]]) para reproducir en el navegador.

**Contenidos relacionados**:
- [[Bases_de_Datos_y_Analisis_Sonoro]]
- [[DynamicPlaylist]]
- [[SpotifyIntegration]]
- [[PrototypeSteps]] (nuevo) para los pasos de un MVP.