# Plan van Aanpak

Klik hierboven door naar de verschillende hoofdstuk uit het 'Plan van Aanpak' document:

![Plan van Aanpak](pva-op-github.png)

## PDF

Je kunt ook de [`.pdf` variant](Plan-van-Aanpak.pdf) bekijken die in een build pipeline automatisch build bij aanpassen van een van de markdown bestanden in de `plan-van-aanpak` folder (*.md). De pipeline built deze met [pandoc](https://pandoc.org). Grote tabellen lopen in de .pdf hierbij helaas wel door elkaar en deeplinks werken niet (deze krijg je niet werkend in zowel pdf als online op GitHub en dat laatste krijgt de voorkeur).

### Lokaal PVA als .pdf genereren/testen

Eerst moet je [pandoc installeren](https://pandoc.org/installing.html).Als het goed is werkt onderstaande commando.

Deze gebruikt het `pva-pdf.yaml` config bestand die ook de Pipeline variant gebruikt. NB: Deze pipeline config heeft 'garantie tot de deur'. De best practice van specifieke versies pinnen is gebruikt (i.p.v. `:latest`/impliciete tags). Maar nog steeds kunnen andere vormen van 'software erosion' (Wiggins, 2011) ervoor zorgen dat je zelf config weer werkend moet krijgen. Dit is onderdeel van 'Build process' (Continuous Documentation als onderdeel van Continuous Delivery).

```bash
cd procesproducten/plan-van-aanpak

pandoc --defaults=pva-pdf.yaml $(cat include.txt)
```

</details>

## Bronnen

- Wiggins A. (28-6-2011) *The New Heroku (Part 4 of 4): Erosion-resistance & Explicit Contracts*. blog.heroku.com. Geraadpleegd april 2025 op [http://blog.heroku.com/the_new_heroku_4_erosion_resistance_explicit_contracts](http://blog.heroku.com/the_new_heroku_4_erosion_resistance_explicit_contracts)
