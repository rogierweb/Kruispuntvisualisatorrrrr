# Kruispuntvisualisatorrrrrr

Maak een kruispuntdiagram van verkeersstromen tussen kruispunttakken. Geef elke tak een naam en een hoek en vul de intensiteiten in een herkomst-bestemmingsmatrix (HB-matrix) in. De pijlen veranderen direct mee met je invoer. Elke herkomsttak heeft een eigen kleur en de lijndikte geeft de relatieve intensiteit van de verkeersstroom weer.

Check het hier: https://rogierweb.github.io/Kruispuntvisualisatorrrrr/

## Openen

Open het HTML-bestand in je browser. De kruispuntvisualisatorrrrr werkt offline. HTML, CSS en JavaScript zitten in hetzelfde bestand. Je hebt geen installatie, server of buildstap nodig.

## Een kruispunt invoeren

1. Gebruik het voorbeeld met vier takken of pas het aan naar je eigen kruispunt. Je kunt twee tot tien kruispunttakken invoeren.
2. Geef elke tak een naam en een hoek. De hoek loopt met de klok mee. Oost is 0°, zuid 90°, west 180° en noord 270°.
3. Vul in de **HB-matrix** het aantal voertuigen per verkeersbeweging in. De rij is de herkomsttak en de kolom is de bestemmingstak. De diagonaal is niet bewerkbaar.
4. Sla het resultaat op met de knoppen onder **Kruispunttakken**.

| Invoer in de HB-matrix | Betekenis |
| --- | --- |
| Positief getal | Intensiteit van herkomst naar bestemming |
| `0` | Nulintensiteit |
| `-1` of een leeg invoerveld | Geen gegevens |

Gebruik binnen één diagram dezelfde eenheid voor alle intensiteiten, bijvoorbeeld voertuigen per uur.

## Opslaan en opnieuw openen

- **PNG exporteren** downloadt het diagram als afbeelding. De uitsnede volgt automatisch de pijlen en labels.
- **JSON exporteren** downloadt de namen, hoeken en HB-matrix, zodat je het kruispunt later kunt bewerken.
- **JSON importeren** laadt een eerder geëxporteerd kruispunt en vervangt de huidige invoer.
- **Voorbeeld herstellen** vervangt de huidige invoer door het voorbeeld met vier takken.

## Implementatie

De tekenlogica is gebaseerd op `renderKruispunt()` uit de VMA Viewer. Het diagram wordt in de browser getekend met de Canvas 2D API. Het JSON-formaat gebruikt de velden `takken`, `hoeken` en `pin`. Het veld `pin` bevat de HB-matrix, in dezelfde volgorde als de kruispunttakken.

## Licentie

De broncode valt onder de [GNU Affero General Public License, versie 3](./LICENSE) (SPDX: `AGPL-3.0-only`).

Verspreid je een gewijzigde versie, dan gelden dezelfde licentievoorwaarden voor die versie en moet je de bijbehorende broncode beschikbaar stellen volgens de licentie. Bied je een gewijzigde versie via een netwerk aan, dan moeten gebruikers die ermee werken de bijbehorende broncode kosteloos via het netwerk kunnen verkrijgen.
