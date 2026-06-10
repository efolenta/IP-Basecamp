# IP Basecamp 🏔️
 
> **Your digital coordinates.**
 
A clean, modern tool for looking up your public IP address — no ads, no clutter, no tracking. Just your IP, front and center, wrapped in an outdoors-inspired experience.
 
**[Live Demo →](https://ip.ericfolenta.com)**
 
---
 
## Inspiration
 
IP Basecamp was born out of a love of hiking and the outdoors. Every time I needed to look up my IP address, I was met with the same cluttered, ad-filled websites that felt more like a billboard than a tool. I wanted to build something that felt calm, intentional, and a little bit like stepping outside.
 
The name comes from the idea of a basecamp — your starting point before a climb. In the same way, your IP address is your starting point on the internet: your digital coordinates in a vast network.
 
---
 
## Features
 
### The Essentials
- Displays your **public IPv4 address** instantly on load
- Displays your **public IPv6 address** if your network supports it
- One-click **copy to clipboard** for each address
- Clean error handling — if IPv6 isn't available, it says so gracefully
### The Fun Stuff
 
**A living mountain scene**
The background is a hand-painted canvas scene — a Firewatch-inspired landscape with three layers of mountain silhouettes, a treeline of spruce trees, and a sky that actually changes.
 
**Day and night mode**
Switch between light and dark mode using the toggle in the top-right corner. Choose from Dark, Light, or System (follows your OS setting automatically). The transition is the best part — watch the sun slowly descend toward the mountains as a warm sunset glow blooms on the horizon, then see the moon rise from behind the peaks as the sky deepens into night. Switch back and the process reverses.
 
**Twinkling stars**
In dark mode, the night sky fills with stars. 25% of them are brighter and twinkle more noticeably with a soft glow — the rest breathe gently in the background. All cycles are slow and organic, nothing harsh.
 
**Real moon phases**
The moon you see in dark mode reflects the actual current phase of the moon. Waxing crescent tonight? That's what you'll see. Full moon? It'll be there in full. No API required — the phase is calculated entirely in the browser using a known lunar reference date and the 29.53-day cycle.
 
---
 
## Tech
 
IP Basecamp is intentionally minimal:
 
- **Vanilla HTML, CSS, and JavaScript** — no frameworks, no build tools
- **Single file** — the entire app is one `index.html`
- **No backend** — everything runs in your browser
- **No tracking** — your IP is fetched for display only, never sent anywhere
---
 
## Credits
 
### IP Lookup — [ipify](https://www.ipify.org)
 
IP addresses are fetched using the ipify API — a free, purpose-built, CORS-friendly service for browser-side IP lookup. Two endpoints are used:
 
- `https://api.ipify.org?format=json` — forces an IPv4 response
- `https://api64.ipify.org?format=json` — returns IPv6 if available, falls back to IPv4
ipify requires no API key and has no tracking or data collection. It's exactly what this project needed.
 
### Moon Phase Calculation
 
No external API is used for moon data. The current phase is calculated entirely in JavaScript using a simple but accurate method:
 
A known new moon date (January 6, 2000) serves as the reference point. The number of days elapsed since that date is divided by the lunar cycle length (29.53059 days) to get a value between 0 and 1 representing the current position in the cycle. That value maps to one of eight standard phases — new, waxing crescent, first quarter, waxing gibbous, full, waning gibbous, third quarter, and waning crescent — and the moon shape is drawn accordingly on an offscreen canvas. Accuracy is within roughly one day, which is plenty for a visual flourish.
 
---
 
## Hosting
 
IP Basecamp is designed to live on GitHub Pages — free, fast, and zero configuration.
 
1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set the source to your `main` branch
4. Visit `yourusername.github.io/repo-name`
To use a custom domain, add a `CNAME` file with your domain and update your DNS settings. GitHub provides free SSL automatically via Let's Encrypt.
 
---
 
## Built With

IP Basecamp was built in collaboration with [Claude](https://claude.ai) by Anthropic. The outdoors and hiking theme was Eric's idea — Claude helped bring it to life through the feature design, canvas rendering, moon phase math, and day/night transition logic.

---

## License
 
MIT — do whatever you like with it.
