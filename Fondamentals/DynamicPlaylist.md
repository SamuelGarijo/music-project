# Dynamic Playlist
Tags: #tecnologia #musica #playlists #analisis #integracion

El concepto de "cola dinámica" consiste en reemplazar o actualizar la lista de reproducción según cambios de sliders (BPM, energía, etc.), sin que el usuario perciba interrupciones notables.

## Lógica básica
1. **Filtrador local**:  
   - Un array o JSON con canciones (ver [[Bases_de_Datos_y_Analisis_Sonoro]]) se filtra cada vez que cambian los parámetros.  
2. **Reemplazo de cola**:  
   - Llamar a `/v1/me/player/play` con la nueva lista filtrada, tal como describe [[SpotifyIntegration]].
3. **Modos de uso**:  
   - "Normal": reproduce un conjunto de canciones según energía/BPM.  
   - "Temático": añade la restricción de artista o género (ej.: "Ciclo The Doors"), relacionado con [[CiclosTematicos]].

## Ajustes dinámicos de atmósfera
- **Sliders**: Volumen, energía, densidad musical, etc.
- **Branding musical**: Ajustar la música a la identidad del local ([[Branding_Musical_y_Segmentacion]]).

## Referencias
- [[TechnicalArchitecture]] para entender dónde se gestiona la lógica de la cola.
- [[PrototypeSteps]] para la implementación paso a paso.