# Hoe het wél makkelijker kan

Interactieve simulatie van één burgeromgeving, geordend naar levensgebied. Dit is het alternatief voor *nóg een identiteitsapp* — geen MyCheck, geen itsme, geen NL Wallet, geen nieuwe DigiD-variant.

Voorheen heette dit prototype **Mijn Omgevingen**. De naam is bewust scherper gemaakt: het punt is niet een extra loket, maar dat de burger altijd en direct toestemming geeft of intrekt.

## Openen

Open `index.html` in een browser. Er zijn geen afhankelijkheden, geen buildstap en geen server nodig. De staat wordt in `localStorage` bewaard (sleutel `hoe-het-wel-makkelijker-kan-v2`). Met **Simulatie resetten** (onder Instellingen) keer je terug naar de beginsituatie, inclusief de voorbeeldtijdlijn.

Dit is een lokale demo. Er gaan geen gegevens naar een echte organisatie.

Live (GitHub Pages): https://ahsumoken.github.io/hoe-het-wel-makkelijker-kan/

## Kernprincipes (zichtbaar én werkend)

1. **Geen losse ID-apps, wel categorieën.** Eén omgeving met Nutsvoorzieningen, Overheid, Social Media, Banken, Zorg, plus Werk en Onderwijs.
2. **Toestemming altijd en direct.** Eén tik om te geven of in te trekken. Geen “weet u het zeker?”, geen opslaan-knop, geen wachtlijn. Elke actie krijgt een tijdstempel in de tijdlijn. Dat geldt ook in het overzicht *Waar heb ik voor getekend?*, en bij het blokkeren van een verdere doorgifte.
3. **Communicatievoorkeuren** per organisatie: e-mail, telefoon, app of geen contact. Ook dit is meteen van kracht.
4. **Openstaande aanvragen.** Via de knoppen “Simuleer: je belde je zorgverzekeraar” (en vergelijkbare scenario’s) verschijnt een verzoek in het portaal. Je kiest welke velden je deelt, of je weigert.
5. **Per veld bepalen wat wel of niet gedeeld mag worden**, met de labels *mag wel* / *mag niet*.
6. **Sector-specifieke identifier** (bijvoorbeeld een Zorg-ID). BSN staat standaard uit. Waar de wet het kan eisen, kun je het zelf aanzetten — en meteen weer uitzetten. Waar het niet thuishoort (nuts, social media) blijft het op “nooit delen”.
7. **Waar heb ik voor getekend?** Met één druk op de knop — per organisatie of via *Alles in één overzicht* — zie je in gewone taal wat je hebt afgesproken: welke data je deelt, welke derden wél of geen data krijgen, wat er in de voorwaarden staat, de tien belangrijkste voordelen en nadelen, mogelijke gevaren, en een checklist.

## Keten, wet en reputatie

Onder *Wél gedeeld* (en ook bij voorbeeldovertredingen) is elke partij aanklikbaar. Je ziet aan wie die partij de data vervolgens doorgeeft — dezelfde kaartgegevens (doel, bewaartermijn, locatie, verkoop, profilering, en welke data doorstroomt), twee tot drie lagen diep. Sommige takken eindigen op “deelt niet verder”.

Boven de kaarten staat een kruimelpad (`Organisatie › Partij A › Partij B`), een terugknop, en een compacte boom: bijvoorbeeld “Je data zit bij 9 partijen in 3 lagen”. Waar dat past, blokkeer je een verdere doorgifte met één tik. Dat is meteen van kracht en komt in de tijdlijn. Een enkele schakel die bij de uitvoering van de wet of van de betaling hoort, is in de simulatie niet te blokkeren; dat staat erbij.

Waar in de voorbeelddata **zonder akkoord** is gedeeld, staan de artikelcodes van de wet die dan in het geding is, in gewone taal, met een link naar de officiële bron. Gebruikt zijn, na controle van de officiële tekst:

- Verordening (EU) 2016/679 (AVG / GDPR), via EUR-Lex: art. 5 lid 1 onder a en b, art. 6 lid 1, art. 7, art. 9, art. 13 en 14, art. 28, art. 44 tot en met 49; als mogelijk gevolg art. 82 (schadevergoeding) en art. 83 (boetes); voor de reactietermijn art. 12 lid 3; voor de klacht en de rechter art. 77 en 79.
- Uitvoeringswet AVG art. 46 (wettelijk identificatienummer / BSN), via wetten.overheid.nl, geldend vanaf 1 september 2026.
- Telecommunicatiewet art. 11.7 lid 1 (ongevraagde communicatie) en art. 11.7a lid 1 (cookies en vergelijkbare techniek), via wetten.overheid.nl.

Bij zo’n markering staat ook **waar je je kunt melden** en wat je kunt verwachten: eerst de organisatie zelf (in beginsel binnen een maand reactie, verlenging met twee maanden mogelijk), daarna de Autoriteit Persoonsgegevens (gemiddeld zes maanden voordat een klacht in behandeling kan, bericht binnen drie maanden), en zo nodig de rechter. Je kunt het bewijs uit de tijdlijn downloaden.

Per partij, op elk niveau, is er een **reputatiecheck** (score, datalekken, boetes, berichten, lopende collectieve acties). Dat is voorbeelddata. Onder *Hoe dit in het echt getoetst wordt* staan geverifieerde bronnen: het Centraal register voor collectieve vorderingen, de AP (boetes, actueel, klacht), het EDPB-register van één-loketbesluiten, en de Consumentenbond. De uitleg over WAMCA (opt-out voor wie in Nederland woont of verblijft, opt-in voor wie dat niet doet) volgt art. 3:305a BW en art. 1018f Rv.

## Tijdlijn

Onder **Tijdlijn** (voorheen het toestemmingenlogboek) staat de hele geschiedenis, tot tien jaar terug, gegroepeerd per jaar en maand. De oude jaren zijn voorbeelddata en staan standaard dicht; het huidige jaar is open. Filters op type en organisatie, een sprong naar een jaar, en nieuwe acties bovenaan. Een reputatiecheck of het (simulatie-)aansluiten bij een collectieve actie wordt ook gelogd.

## Indeling

- **Desktop (vanaf 901 px):** drie kolommen, in de trant van het eerdere ontwerp. Links sectoren, midden organisaties (badge Actief / Niet gekoppeld, “Toestemmingen bekijken”), rechts de velden, het sector-ID en de communicatievoorkeur. In de kop: Aanvragen, Tijdlijn, *Waar heb ik voor getekend?*, Instellingen.
- **Mobiel:** kaarten per sector (“x koppelingen actief”) en een onderbalk Home / Toestemmingen / Getekend / Instellingen. In het detailscherm dezelfde schakelaars, inclusief BSN “nooit delen”.

De stijl is rustig blauw-wit en gebruikt alleen systeemfonts. Er zijn geen logo’s of nabootsingen van bestaande ID-apps; die namen komen alleen in de tekst voor, als contrast.

## Bestanden

- `index.html` — de hele simulatie (HTML, CSS en JavaScript in één bestand)
- `README.md` — deze toelichting
