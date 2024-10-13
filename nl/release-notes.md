---
title: Release notes
description: Versie informatie van het Repower Smart Energy platform
published: true
date: 2024-10-10T14:00:00.000Z
tags: 
editor: markdown
dateCreated: 2024-03-13T13:06:08.526Z
---

_Onderaan de pagina staat welke versie van het platform je nu gebruikt. Loopt deze achter op de nieuwste versie? Vernieuw dan de pagina (Ctrl + Shift + R)._

# 14 oktober: versie 2.23.3

- Debounce is functie toegevoegd aan bepaalde API calls om gelijktijdige verzoeken juist te kunnen verwerken.
- Bij elke relevante call word een UID opgeslagen in de cache. Als er dan een response komt dan word het doorgegeven UID vergeleken met dit opgeslagen UID. Als deze niet overeenkomen dan wordt het verzoek geannuleerd. Dit voorkomt dat de verkeerde data wordt getoond. 

# 3 september: Versie 2.2.0

- Onbalans setpoints en FCR allocaties zijn nu te zien via [Assets > Analyse](/assets/analysis). Beweeg met de muis over de tijdlijn voor gedetailleerde informatie.
- Verschillende kleine updates rondom navigatie.

# 13 augustus: Versie 2.1.36

- Vernieuwde export functionaliteit voor resultaten en meetgegevens: download een Excel bestand met data op kwartierniveau.
- Wijzig je naam, e-mailadres en wachtwoord via [Instellingen](/account/settings).
- Bugfixes en verbeteringen aan de weergave van grafieken.

# 10 juni: Versie 2.1.21

- Responsive design voor telefoons en andere kleine schermen.
- Nieuwe asset pagina's voor algemene info en verwachte omzet.
- Facturen zijn nu inzichtelijk via [Mijn Repowered](/account).
