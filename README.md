# Tuno Fighter 🥊

Juego de pelea 1 vs 1 con tunos. Un solo archivo (`index.html`), sin instalar nada.

## Subirlo a GitHub Pages
1. Crea un repositorio nuevo en GitHub (por ejemplo `tuno-fighter`).
2. Sube `index.html` (y `luchadores.json` si ya lo tienes). **Add file → Upload files**.
3. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
4. En 1-2 minutos tu juego estará en https://DretcmU.github.io/tuno-fighter/.

## Poner las caras de tus amigos (una sola vez)
1. Abre `index.html` en tu computadora (doble clic).
2. Pulsa **📷 Cargar fotos**, elige todas las fotos del Drive, y por cada una toca el rostro, ajusta el círculo y escribe el nombre.
3. Pulsa **💾 Guardar luchadores**: se descarga `luchadores.json`.
4. Sube `luchadores.json` al repositorio, junto a `index.html`. Al abrir la página se cargarán solos.

## Controles
**J1:** A/D mover · W saltar (2 veces = doble salto) · S agacharse/guardia · F puño · G patada · E dash · H pandereta · R lluvia (40%) · J serenata (100%)
**J2:** ←/→ · ↑ · ↓ · K puño · L patada · I dash · O pandereta · U lluvia · P serenata
**M** = silenciar. Si aparece la chica, ¡salta!

## Jugar en el celular
Abre la página en el celular: aparecen botones táctiles (cruceta a la izquierda y 👊 🦵 💨 🪘 ☔ 🎸 a la derecha). En horizontal los botones se superponen al juego. Toca la pantalla al terminar una ronda para continuar.

## Jugar online
1. Uno pulsa **🌐 Online → Crear sala**: aparece un código de 5 letras y los botones **Copiar enlace** y **Compartir** (WhatsApp, etc.).
2. El otro abre el enlace (o escribe el código y pulsa **Unirme**).
3. Cada uno elige su luchador y empieza la pelea. Cada jugador usa sus propios controles (WASD o flechas en PC, botones en el celular).

La conexión es directa entre los dos jugadores (PeerJS/WebRTC). Necesita internet y la página abierta desde `https://` (GitHub Pages sirve). En algunas redes (ciertos datos móviles o wifis de empresa) puede no conectar.

## Límites del online
- No hay un límite de salas por nuestra parte: cada sala son solo 2 jugadores y el juego va directo entre ellos, sin pasar por ningún servidor tuyo.
- El código se negocia con el servidor gratuito de PeerJS, que es compartido y sin garantía de disponibilidad. Si algún día se satura, pon tu propio PeerServer (gratis en Render/Fly.io) y rellena `PEER_OPTS` al inicio del código.
- Si un jugador cambia de app o pierde señal, el otro ve un aviso y el juego espera hasta 15 segundos antes de cancelar.

## Mapas
Hay 3: Rotonda de San Lázaro, Mirador de Yanahuara y El Inter. Se elige en el menú antes de escoger luchador (en online manda el mapa de quien crea la sala).

## Música
La música de fondo son las canciones de `DretcmU/Reel-tuna-antes-despues` (carpeta `canciones`), en orden aleatorio. La lista se lee de `songs.json` de ese repo, así que si agregas canciones ahí, entran solas. Si no hay internet, suena una melodía de respaldo.

## Saltos
Si uno salta sobre el otro puede cruzar al otro lado y el personaje se voltea; en el suelo siguen chocando.
