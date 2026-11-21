# Plaud → úkoly a follow-upy

1. Načti nahrávky od posledního zpracování (poznámka v popisu poslední události `zdroj=plaud:` nebo posledních 48 h).
2. Z poznámky / přepisu vytáhni:
   - konkrétní úkoly Jakuba („musím…“, „domluvili jsme se, že…“, „připomenout…“)
   - termíny a schůzky
   - informace do profilu (nové závazky, preference)
3. Každý úkol → událost `typ=ukol` ve vhodném slotu (krátké úkoly 15 min, připomínka 0 min), popis: kontext + `zdroj=plaud:<file_id>`.
4. Nejisté interpretace (kdo, kdy) → do briefu jako otázka, nevytvářej naslepo.
5. Plaud ID už v kalendáři je → přeskoč (prohledej popisy přes `fullText`).
