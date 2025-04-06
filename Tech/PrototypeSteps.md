# Prototype Steps
Tags: #mvp #implementacion #desarrollo #tecnologia #integracion

Guía rápida para construir un **MVP** (Producto Mínimo Viable) que combine los viejos conceptos (base de datos de canciones, branding musical, etc.) y los nuevos (playlists dinámicas, licencias).

1. **Registro en Spotify Developer**  
   - Credenciales (client_id, client_secret).  
   - Configurar redirect URI para autenticación.

2. **Prototipo de base de datos o caché**  
   - Recopilar datos de algunos artistas (3-4) usando Exportify o la API, tal como se describe en [[Bases_de_Datos_y_Analisis_Sonoro]].  
   - Crear un JSON local (o usar Supabase) con BPM, energía, etc.

3. **Diseño del dashboard**  
   - Crear sliders (BPM, energía, etc.) para filtrar canciones.  
   - Integrar conceptos de [[Branding_Musical_y_Segmentacion]] (por ejemplo, "bar retro" = rock 60s con poca energía por la mañana).

4. **Reproductor con Spotify**  
   - Implementar [[SpotifyIntegration]] para reproducir las pistas directamente en el navegador.  
   - Llamar al endpoint `/v1/me/player/play` cuando cambien los sliders (ver también [[DynamicPlaylist]]).

5. **Test con ciclos temáticos**  
   - Añadir modo "Ciclo Temático" (ej.: "Semana de Miles Davis"), tomando ideas de [[Ciclos_Tematicos_y_Experiencias]].  
   - Ver feedback en un entorno pequeño (1-2 locales).

**Otras referencias**:
- [[UserExperience]] para entender a quién va dirigido.
- [[Conexiones_con_Locales_y_Modelo_de_Negocio]] si quieres darle forma comercial.