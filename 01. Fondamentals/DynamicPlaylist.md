# Dynamic Playlist
Tags: #tecnologia #musica #playlists #analisis #integracion

El concepto de "cola dinámica" consiste en reemplazar o actualizar la lista de reproducción según cambios de sliders (BPM, energía, etc.), sin que el usuario perciba interrupciones notables.

## Lógica básica
1. **Filtrador local**:  
   - Un array o JSON con canciones (ver [[Bases_de_Datos_y_Analisis_Sonoro]]) se filtra cada vez que cambian los parámetros.  
   - Se respeta el [[ADN_Sonoro]] definido para mantener la coherencia musical.
2. **Reemplazo de cola**:  
   - Llamar a `/v1/me/player/play` con la nueva lista filtrada, tal como describe [[SpotifyIntegration]].
3. **Modos de uso**:  
   - "Normal": reproduce un conjunto de canciones según energía/BPM.  
   - "Temático": añade la restricción de artista o género (ej.: "Ciclo The Doors"), relacionado con [[CiclosTematicos]].

## Ajustes dinámicos de atmósfera
- **Sliders**: Volumen, energía, densidad musical, etc. (ver [[ControladoresDinamicos]] para detalles sobre estos mecanismos interactivos).
- **Branding musical**: Ajustar la música a la identidad del local ([[Branding_Musical_y_Segmentacion]]).

## Referencias
- [[TechnicalArchitecture]] para entender dónde se gestiona la lógica de la cola.
- [[PrototypeSteps]] para la implementación paso a paso.
- [[ADN_Sonoro]] para comprender el núcleo que define la coherencia musical.
- [[TunelesMusicales]] para entender el concepto de experiencias musicales dinámicas que esta tecnología permite crear.
- [[ControladoresDinamicos]] para detalles sobre los mecanismos interactivos que permiten ajustar las playlists.