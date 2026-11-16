# Hoe het wél makkelijker kan

Interactieve simulatie van één burgeromgeving, geordend naar levensgebied. Dit is het alternatief voor *nóg een identiteitsapp* — geen MyCheck, geen itsme, geen NL Wallet, geen nieuwe DigiD-variant.

Voorheen heette dit prototype **Mijn Omgevingen**. De naam is bewust scherper gemaakt: het punt is niet een extra loket, maar dat de burger altijd en direct toestemming geeft of intrekt.

## Openen

Open `index.html` in een browser. Er zijn geen afhankelijkheden, geen buildstap en geen server nodig. De staat wordt in `localStorage` bewaard (sleutel `hoe-het-wel-makkelijker-kan-v1`). Met **Simulatie resetten** (onder Instellingen) keer je terug naar de beginsituatie.

Dit is een lokale demo. Er gaan geen gegevens naar een echte organisatie.

Live (GitHub Pages): https://ahsumoken.github.io/hoe-het-wel-makkelijker-kan/

## Kernprincipes (zichtbaar én werkend)

1. **Geen losse ID-apps, wel categorieën.** Eén omgeving met Nutsvoorzieningen, Overheid, Social Media, Banken, Zorg, plus Werk en Onderwijs.
2. **Toestemming altijd en direct.** Eén tik om te geven of in te trekken. Geen “weet u het zeker?”, geen opslaan-knop, geen wachtlijn. Elke actie krijgt een tijdstempel in het logboek. Dat geldt ook in het overzicht *Waar heb ik voor getekend?*.
3. **Communicatievoorkeuren** per organisatie: e-mail, telefoon, app of geen contact. Ook dit is meteen van kracht.
4. **Openstaande aanvragen.** Via de knoppen “Simuleer: je belde je zorgverzekeraar” (en vergelijkbare scenario’s) verschijnt een verzoek in het portaal. Je kiest welke velden je deelt, of je weigert.
5. **Per veld bepalen wat wel of niet gedeeld mag worden**, met de labels *mag wel* / *mag niet*.
6. **Sector-specifieke identifier** (bijvoorbeeld een Zorg-ID). BSN staat standaard uit. Waar de wet het kan eisen, kun je het zelf aanzetten — en meteen weer uitzetten. Waar het niet thuishoort (nuts, social media) blijft het op “nooit delen”.
7. **Waar heb ik voor getekend?** Met één druk op de knop — per organisatie of via *Alles in één overzicht* — zie je in gewone taal wat je hebt afgesproken: welke data je deelt, welke derden wél of geen data krijgen (inclusief een kort privacybeleid: doel, bewaartermijn, locatie, verkoop en profilering), wat er in de voorwaarden staat over data en toestemming, de tien belangrijkste voordelen en nadelen, mogelijke gevaren, en een checklist waar je op moet letten. Organisaties, derden en voorwaarden in dit onderdeel zijn **voorbeelddata**; de risicocategorieën (datalek, profilering, doorverkoop, function creep, koppeling van datasets, enzovoort) zijn algemeen en herkenbaar.

## Indeling

- **Desktop (vanaf 901 px):** drie kolommen, in de trant van het eerdere ontwerp. Links sectoren, midden organisaties (badge Actief / Niet gekoppeld, “Toestemmingen bekijken”), rechts de velden, het sector-ID en de communicatievoorkeur. In de kop: Aanvragen, Logboek, *Waar heb ik voor getekend?*, Instellingen.
- **Mobiel:** kaarten per sector (“x koppelingen actief”) en een onderbalk Home / Toestemmingen / Getekend / Instellingen. In het detailscherm dezelfde schakelaars, inclusief BSN “nooit delen”.

De stijl is rustig blauw-wit en gebruikt alleen systeemfonts. Er zijn geen logo’s of nabootsingen van bestaande ID-apps; die namen komen alleen in de tekst voor, als contrast.

## Bestanden

- `index.html` — de hele simulatie (HTML, CSS en JavaScript in één bestand)
- `README.md` — deze toelichting
