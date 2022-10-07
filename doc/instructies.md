# DevOps project/Operations - instructies

## Broncode

De directory `src/` zal alle broncode bevatten voor het opzetten van de opstelling.

- Je mag gebruik maken van werk dat tijdens het semester gerealiseerd is door het team.
- Als je code uit de Github-repo van het team overbrengt naar deze repo, geef dat dan duidelijk aan in de commit-boodschap (bv. "overnemen code 1zit").
- Probeer niet om code die je niet zelf geschreven hebt voor te stellen als je eigen werk. Vermeld altijd de auteurs als je code overneemt.
- Je mag gebruik maken van startcode uit bv. [ansible-skeleton](https://github.com/bertvv/ansible-skeleton) of [vagrant-shell-skeleton](https://github.com/bertvv/vagrant-shell-skeleton). Vergeet niet om de `.gitignore` en `.gitattributes` te verplaatsen naar de root van je eigen repository!

## Documentatie

De directory `doc/` bevat alle documentatie. Het bestand [procedure.md](procedure.md) bevat de procedurehandleidingen voor het reproduceren en gebruiken van de gerealiseerde opstelling.

- Als je vindt dat het bestand te groot en onoverzichtelijk wordt, kan je het opsplitsen in meerdere bestanden (bv. één per server).
- Zorg in de [README](../README.md) van dit project voor een duidelijk overzicht/inhoudstafel met aanklikbare links. Deze links moeten werken op Github!
- Maak zelf nieuwe bestanden aan voor aanvullende technische documentatie (bv. samenvattingen opzoekwerk, cheat sheets van vaak gebruikte commando's, enz.).
- Zorg voor een nette en overzichtelijke directorystructuur met zinvolle directory- en bestandsnamen.

Beschrijf in de procedurehandleidingen altijd:

- Welke voorwaarden moeten voldaan zijn om te kunnen beginnen aan de procedure (*prerequisites*, bv. geïnstalleerde software)?
- Welke stappen moet je doorlopen om de opstelling te reproduceren? Gebruik fenced code blocks voor interacties met de terminal of desgevallend screenshots voor interacties met een GUI of webinterface. Hou screenshots bij in een subdirectory binnen deze repo.
- Hoe kunnen we controleren dat het eindresultaat correct is, dat de procedure met succes is doorlopen?
