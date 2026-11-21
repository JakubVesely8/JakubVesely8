# Pravidla kalendáře

## Kategorie a barvy
Každá událost, kterou asistent vytvoří nebo zapíše, má kategorii = barvu (`colorId` v Google Calendar API).

| Kategorie | colorId | Barva | Příklady |
|---|---|---|---|
| Práce | 9 | Blueberry | pracovní blok 9–17, přesčas |
| Škola | 3 | Grape | VŠEM výuka, zkoušky, učení |
| Trénink | 10 | Basil | plavání, kolo, běh, gym, coach |
| Angličtina | 7 | Peacock | lekce se Stevem, příprava na test |
| Osobní / vyřizování | 5 | Banana | doktor, nákupy, úřady, servis kola |
| Sociální / rodina | 4 | Flamingo | kamarádi, rodina, večeře, rezervace |
| Cesty | 8 | Graphite | přesuny, lety, dojíždění |
| Odpočinek | 2 | Sage | volno, regenerace, spánek navíc |
| Focus / hluboká práce | 6 | Tangerine | vlastní projekty, učení v klidu |
| Důležité / deadline | 11 | Tomato | termíny, které nesmí utéct |

Existující události bez barvy asistent **nepřebarvuje**, pokud nejsou jeho (`#asistent`). Ve statistikách je zařadí podle názvu.

## Značení událostí asistenta
Poslední řádek popisu každé události, kterou asistent vytvoří:

```
#asistent kat=<Kategorie> typ=<plan|log|ukol> zdroj=<rucne|strava:<id>|gmail:<threadId>|plaud:<id>>
```

- `typ=plan` – plán do budoucna
- `typ=log` – zpětný zápis skutečnosti
- `typ=ukol` – úkol s vyhrazeným časem

Díky tomu jde poznat, co je asistentovo, a nevznikají duplicity (např. stejná `strava:<id>` se nezapíše dvakrát).

## Plán vs. skutečnost
- Když plánovaný blok (`typ=plan`) proběhl jinak, **uprav ho na skutečný čas** a změň na `typ=log`. Do popisu připiš `původně: HH:MM–HH:MM`.
- Když neproběhl vůbec, nemaž ho mlčky: v briefu se zeptej, jestli ho přesunout, nebo smazat.

## Připomínky
- Výchozí připomínky kalendáře (30 min) ponech.
- Trénink brzy ráno: připomínka večer předem není třeba, stačí brief.
- Deadliny (Tomato): připomínky 1 den a 1 h předem.

## Ochrana času
- Spánek a ranní rutina jsou nedotknutelné (časy v profilu).
- Po tréninku nech 15–30 min rezervu.
- Mezi dvěma místy v Praze počítej ~30 min přesun (u Holešovic/VŠEM podle mapy).
- Víkendy s výukou VŠEM: trénink plánuj mimo bloky výuky (ráno nebo v obědové pauze 12–14).
