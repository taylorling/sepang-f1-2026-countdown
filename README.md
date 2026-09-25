# Sepang F1 2026 countdown

A live pixel-art countdown to the **Formula 1 Gulf Air Bahrain Grand Prix in Malaysia** at Sepang International Circuit. Lights out is Sunday 4 October 2026 at 3:00 pm Malaysia time (07:00 UTC).

**Live site:** https://sepang-f1-2026-countdown.vercel.app

## What you'll see

- The Sepang main grandstand with the Hibiscus Tower, its globe, and a waving Malaysian flag, plus Bahrain and Malaysia flags around the circuit.
- F1 cars lapping the main straight, a crowd that cheers as they pass, fans waving flags, a marshal, a KLIA jet taking off, and a timing pylon.
- A full day-to-night cycle every 60 seconds: sunset, floodlights, camera flashes in the stands and fireworks at night.
- A countdown drawn in pixels, with the start time converted to the visitor's own time zone and city (for example "SUN 4 OCT 08:00 LONDON TIME").
- Automatic race-day states: "LIGHTS OUT! RACE IS LIVE" with a lap counter from 3:00 pm, then "CHEQUERED FLAG" once the race is over.

## How it works

Everything lives in a single self-contained `index.html` with no dependencies, fonts or external requests.

- The static scenery (sky layers, grandstand, track, crowd bank) is baked into the file as small images.
- A small JavaScript renderer draws every frame live on a tiny canvas, around 480 × 270 pixels, then scales it up by a whole number so the pixels stay crisp.
- It composites the layers, moves the sprites, tints the scene for the time of day, adds a separate layer of lights and glows at night, and draws the countdown text pixel by pixel.
- The layout adapts to any screen. Wide screens get the landscape scene with extra track and crowd filled in at the sides. Tall screens get a portrait layout with more sky and grass.

## Run it locally

Open `index.html` in a browser. That's it.

## Make your own

Fork the repo and deploy it anywhere that serves static files, such as Vercel, Netlify, Cloudflare Pages or GitHub Pages. To point it at a different race, change the `RACE` constant near the top of the script (a UTC timestamp) and the end-of-race messages in `countdownLines`.

## Credits

Inspired by DDChen's pixel-art "living diorama" post ([x.com/chen79639ddc](https://x.com/chen79639ddc/status/2103020737623965885)). Made by [Taylor Ling](https://github.com/taylorling) with Claude.

This is an unofficial fan project. It is not affiliated with or endorsed by Formula 1, the FIA, Sepang International Circuit or any team. Car liveries are invented. Formula 1 and related marks belong to their respective owners.

## License

MIT. Copy it, remix it, make one for your own circuit.
