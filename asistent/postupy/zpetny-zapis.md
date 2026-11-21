# Zpětný zápis (deník času)

Cíl: kalendář ukazuje, **co Jakub skutečně dělal**, ne jen co plánoval.

## Z věty od Jakuba
Příklady: „včera jsem byl v práci do 18:30“, „v sobotu 14–16 jsem se učil na právo“, „dneska ráno jsem nebyl na plavání, spal jsem do 7“.

1. Rozpoznej den, čas od–do, činnost, kategorii. Relativní dny počítej od dnešního data.
2. Najdi existující událost v tom čase:
   - plánovaný blok stejné činnosti → **uprav** na skutečný čas, `typ=log`, do popisu `původně: …`
   - neproběhlá událost („nebyl jsem“) → u vlastních bloků asistenta ji smaž nebo přejmenuj na `✗ <název>` (zeptej se jednou, co Jakub preferuje, a zapiš do profilu); u cizích nic neměň
   - nic tam není → **vytvoř** novou událost `typ=log`
3. Překryvy: pokud nový zápis překrývá jiný vlastní log, zkrať ten méně pravděpodobný a řekni to.
4. Nejasný čas („odpoledne“) → zeptej se, nebo použij rozumný odhad a označ v popisu `čas odhadnut`.
5. Potvrď jedním řádkem: `Zapsáno: So 22. 11. 14:00–16:00 Učení – Právo (Škola)`.

Více vět najednou zpracuj hromadně a potvrď seznamem.

## Ze Stravy (automaticky)
- Každou aktivitu převeď na událost: název `<Sport>: <název aktivity>` (např. `Běh: Morning Run 8,0 km`), čas = `start_local` + `elapsed_time`, kategorie Trénink, zdroj `strava:<id>`.
- Do popisu: vzdálenost, moving time, tempo / rychlost, relative effort.
- Pokud existuje plánovaný trénink stejného sportu v okně ±3 h → uprav ho místo vytváření nového.
- Strava `id` už v kalendáři je → přeskoč.
- Jednu fyzickou session rozdělenou do více aktivit (např. dvě plavání 19:49 a 20:06) zapiš jako jednu událost.
