# Imágenes de BLACKOUT

Dos retratos y tres escenas ficticias generados con la herramienta integrada `image_gen`, sin usar la API/CLI. Las escenas ilustran situaciones posibles; no son fotografías documentales de eventos reales de BLACKOUT ni de Black Hat.

- `atacante.png`: operador situado a la izquierda, mirando a la derecha.
- `defensor.png`: operadora situada a la derecha, mirando a la izquierda.
- `evento.png`: bienvenida a una conferencia de ciberseguridad, para `ProximoEvento`.
- `academia.png`: aprendizaje colaborativo en un taller, para `Aprende`.
- `comunidad.png`: equipos resolviendo retos en un torneo presencial, para `Nosotros`.

`Duelo.astro` consume versiones WebP de 320, 480 y 720 px mediante `srcset`, con carga diferida y dimensiones explícitas. Se generaron con ImageMagick a calidad 80; no requieren dependencias adicionales. Los PNG conservan las imágenes originales. Los textos y el color de acento pertenecen al componente, para responder a ambos temas y al tamaño de pantalla.

`Escena.astro` sirve las tres escenas en WebP de 360, 720 y 1280 px. La imagen del evento carga inmediatamente porque se encuentra en la portada; las imágenes de academia y comunidad cargan de forma diferida.

## Integración

Los componentes definitivos son `Hero`, `ProximoEvento`, `Nosotros`, `Aprende`, `Compite`, `Duelo` y `Escena`. Las imágenes se almacenan en `src/assets/blackout/`. El ajuste de posición del retrato de la defensora se realiza con CSS en `Duelo.astro`; los archivos de imagen no se modifican.

Las fichas de los personajes usan los alias y equipos de ejemplo del ranking: `root.404` / `NULL POINTERS` y `n0cturnal` / `GH0ST DIVISION`.

## Prompts utilizados

Los prompts de las tres nuevas escenas están en [PROMPTS-ESCENAS.md](./PROMPTS-ESCENAS.md).

### Atacante

Use case: ads-marketing. Asset type: left competitor portrait in a reversible experimental VS tournament module on BLACKOUT, an ethical hacking community website. Create one original fictional adult male cybersecurity competitor, short dark textured hair, dark unbranded technical jacket, face unobscured, focused calm expression, chest-up portrait, three-quarter pose looking toward the RIGHT edge to face an opponent in a two-portrait web layout. Subject centered, whole head visible with generous space above, shoulders fade into absolute black. Vertical 4:5 composition. Premium monochrome editorial photography fused with gritty photocopy zine art, fine halftone screen print, restrained dithering and film grain. Sharp recognizable facial structure and eyes, dramatic side lighting, ink-black background with extremely faint scan lines, off-white highlights. Entirely grayscale, no color, no glow. Quiet confidence and intelligent competitive tension, underground computer tournament art direction. Only a single person. No hood, mask, weapons, logos, text, letters, numbers, watermark, UI, borders, laptop, extra props or scenery. This is an image asset only, not a web page mockup.

### Defensor

Use case: ads-marketing. Asset type: right competitor portrait in a reversible experimental VS tournament module on BLACKOUT, an ethical hacking community website. Create one original fictional adult female cybersecurity competitor, dark hair tied back, dark unbranded technical jacket, face unobscured, focused calm expression, chest-up portrait, three-quarter pose looking toward the LEFT edge to face an opponent in a two-portrait web layout. Subject centered, whole head visible with generous space above, shoulders fade into absolute black. Vertical 4:5 composition. Premium monochrome editorial photography fused with gritty photocopy zine art, fine halftone screen print, restrained dithering and film grain. Sharp recognizable facial structure and eyes, dramatic side lighting, ink-black background with extremely faint scan lines, off-white highlights. Entirely grayscale, no color, no glow. Quiet confidence and intelligent competitive tension, underground computer tournament art direction. Only a single person. No hood, mask, weapons, logos, text, letters, numbers, watermark, UI, borders, laptop, extra props or scenery. This is an image asset only, not a web page mockup.
