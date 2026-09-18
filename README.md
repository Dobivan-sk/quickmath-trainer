# QuickMath Trainer

Rýchla vanilla JS/HTML/CSS hra na tréning malej aj veľkej násobilky a delenia. 10 úrovní, 3 životy, streak bonusy, highscore v `localStorage`, slovenská a anglická lokalizácia, a funguje ako instalovateľná PWA na macOS, iOS aj Androide.

**Živá verzia:** https://dobivan-sk.github.io/quickmath-trainer/

## Ako to spustiť lokálne

Žiadny build, žiadne závislosti — stačí otvoriť `Quick-Math.html` v prehliadači, alebo pre plnú funkčnosť PWA (manifest + service worker) spustiť lokálny server:

```bash
python3 -m http.server 8000
```

a otvoriť `http://localhost:8000/Quick-Math.html`.

## Štruktúra súborov

| Súbor | Účel |
|---|---|
| `Quick-Math.html` | celá hra — HTML, CSS aj JS v jednom súbore |
| `index.html` | presmerovanie z koreňovej URL na `Quick-Math.html` |
| `manifest.json` | PWA manifest (názov, ikonky, farby, `start_url`) |
| `sw.js` | service worker — cachuje appku pre offline chod |
| `icon-new.svg`, `icon-*.png` | ikonka appky (favicon, apple-touch-icon, PWA icons) |

## Funkcie

- 10 úrovní obtiažnosti, automaticky podľa dosiahnutého skóre
- Malá aj veľká násobilka a delenie, časový limit na odpoveď
- Streak: 5 správnych v rade = +1 život, pauza hry = -1 život
- Vlastná číselná klávesnica (funguje aj bez natívnej mobilnej klávesnice)
- Highscore rebríček uložený v prehliadači
- Slovenčina / English prepínač
- Instalovateľná ako appka (Add to Home Screen) na iOS a Androide

## Nasadenie

Hostované na GitHub Pages z branchu `main`. Zmena súboru + `git push` sa prejaví na živom linku do minúty.

---
Vytvorené s [Claude Code](https://claude.com/claude-code).
