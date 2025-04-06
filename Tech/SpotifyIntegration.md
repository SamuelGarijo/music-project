# Spotify Integration
Tags: #api #integracion #tecnologia #desarrollo #playlists

Este archivo detalla cómo incorporar la reproducción y autenticación de Spotify en nuestro proyecto, aprovechando la estrategia descrita en [[Bases_de_Datos_y_Analisis_Sonoro]] para obtener metadatos.

## 1. Autenticación OAuth
- Registrar una app en [Spotify Developer](https://developer.spotify.com/dashboard).
- Obtener `access_token` y `refresh_token` del usuario.
- Referencia: si en [[Colaboradores_y_Expansión]] planeas incluir un desarrollador experto, esto es parte de sus tareas.

## 2. Web Playback SDK
- Incluir `<script src="https://sdk.scdn.co/spotify-player.js"></script>`.
- Crear un objeto `Spotify.Player` con `client_id`.
- Permite reproducir playlists generadas en tiempo real (ver [[DynamicPlaylist]]).

## 3. Endpoints de la API
- `/v1/me/player/play`: Inicia reproducción en el "device" del SDK.
- `/v1/audio-features`: Obtiene BPM, energy, danceability, etc. (parte esencial de [[Bases_de_Datos_y_Analisis_Sonoro]]).

## Referencias adicionales
- [[PrototypeSteps]] para implementar el MVP.
- [[TechnicalArchitecture]] para ver la arquitectura de integración.
- [[UserExperience]] para entender cómo se mostrará todo al dueño y al usuario final.