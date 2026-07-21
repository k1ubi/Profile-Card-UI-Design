<div align="center">

```
____________ ___________ _____ _      _____   _____   ___  ____________ 
| ___ \ ___ \  _  |  ___|_   _| |    |  ___| /  __ \ / _ \ | ___ \  _  \
| |_/ / |_/ / | | | |_    | | | |    | |__   | /  \// /_\ \| |_/ / | | |
|  __/|    /| | | |  _|   | | | |    |  __|  | |    |  _  ||    /| | | |
| |   | |\ \\ \_/ / |    _| |_| |____| |___  | \__/\| | | || |\ \| |/ / 
\_|   \_| \_|\___/\_|    \___/\_____/\____/   \____/\_| |_/\_| \_|___/  
```

`[ glassmorphic identity card :: vanilla HTML/CSS/JS :: zero dependencies ]`

![html5](https://img.shields.io/badge/HTML5-ff00c8?style=for-the-badge&logo=html5&logoColor=00fff9&labelColor=0a0014)
![css](https://img.shields.io/badge/CSS-00fff9?style=for-the-badge&logo=css&logoColor=0a0014&labelColor=0a0014)
![sass](https://img.shields.io/badge/SASS-ff00c8?style=for-the-badge&logo=sass&logoColor=00fff9&labelColor=0a0014)
![javascript](https://img.shields.io/badge/JAVASCRIPT-00fff9?style=for-the-badge&logo=javascript&logoColor=0a0014&labelColor=0a0014)

</div>

<br>

```
▓▒░ 0x00 // SITREP ░▒▓
```

A single self-contained glassmorphic profile card — one `<div class="profile-card">`, no framework,
no build step required to run it. Frosted-glass panel over a slowly zooming background image, a
circular avatar, identity block, location tag, social links, and two call-to-action buttons. The demo
data in `index.html` is the card actually used to represent its author — infosec role tags, Rome
location pin, LinkedIn + GitHub links, "Send Email" / "Add me" buttons wired to real `mailto:`/profile
targets.

<br>

```
▓▒░ 0x01 // WHAT'S IN THE CARD ░▒▓
```

- `►` **backdrop blur** — `.profile-card` uses `backdrop-filter: blur(15px)` over a translucent
  border so whatever sits behind the card bleeds through, softened
- `►` **slow zoom background** — `body::before` runs a 20s one-shot `backgroundZoomAnimate`
  keyframe (`scale(1) → scale(1.3)`) on a full-bleed `bg.jpg`
- `►` **circular avatar** — `avatar.webp`, clipped to a 200×200 circle with `object-fit: cover`
- `►` **identity block** — name, role tagline, and a location row with an inline Tabler `map-pin` SVG
- `►` **social row** — Tabler LinkedIn / GitHub icon links, each opening in a new tab
- `►` **action buttons** — `blue` (email) and `purple` (GitHub) variants, wired via inline `onClick`
- `►` **responsive** — card drops to `width: auto` under the `max-width: 768px` media query

<br>

```
▓▒░ 0x02 // FILES ░▒▓
```

| file | role |
|---|---|
| `index.html` | markup + the actual card content/data |
| `reset.css` | baseline reset loaded before the card styles |
| `style.scss` | source styles (Sass) |
| `style.css` / `style.css.map` | compiled output + source map |

<br>

```
▓▒░ 0x03 // RUN IT ░▒▓
```

```console
root@node:~/Profile-Card-UI-Design# open index.html
```

No server, no build tooling required to view it — it's plain HTML/CSS/JS. If you're editing styles,
work in `style.scss` and recompile with Dart Sass:

```console
root@node:~/Profile-Card-UI-Design# sass style.scss style.css
```

<br>

<div align="center">

`.: swap the avatar, the name block, and the social hrefs to make it yours :.`

</div>
