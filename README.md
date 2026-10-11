# Meteostanice – webová stránka

Stránka si sama bere data z ThingSpeaku (kanál 3530905) a kreslí karty s aktuálními
hodnotami a grafy za 24 hodin / 7 dní / 30 dní. Jde přidat na plochu mobilu jako aplikace.

## Soubory (všechny nahraj do stejné složky)

- `index.html` – celá stránka
- `manifest.webmanifest`, `sw.js` – aby šla nainstalovat jako aplikace
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` – ikony

## Nahrání na GitHub Pages (zdarma)

1. Na github.com se přihlas (nebo si zdarma založ účet).
2. Vpravo nahoře **+ → New repository**. Název např. `meteostanice`, nastav **Public**, dole **Create repository**.
3. Na stránce nového repozitáře klikni **uploading an existing file**, přetáhni tam **všech 6 souborů** (ne zip, ale soubory) a dole klikni **Commit changes**.
4. **Settings → Pages**. V části *Build and deployment* nastav **Source: Deploy from a branch**, **Branch: main**, složka **/ (root)**, **Save**.
5. Za 1–2 minuty se nahoře na té stránce objeví adresa
   `https://TVOJE-JMENO.github.io/meteostanice/`. To je tvoje stránka.

## Přidání na plochu mobilu

- **iPhone (Safari):** otevři adresu → tlačítko Sdílet → **Přidat na plochu**.
- **Android (Chrome):** otevři adresu → menu ⋮ → **Instalovat aplikaci** / **Přidat na plochu**.

## Změna nastavení

Nahoře v `index.html` je blok `CONFIG` (Channel ID, Read API Key, intervaly).
Názvy a pořadí místností jsou hned pod ním v `ROOMS`.
Po úpravě soubor v GitHubu přepiš (ikona tužky → Commit changes); nová verze je za minutu online.

## Pozor na soukromí

Read API Key je v souboru vidět každému, kdo si stránku otevře a zobrazí zdroj. Klíč umí jen číst
data tohoto kanálu (nic zapsat ani změnit nejde). Kdo zná adresu stránky, uvidí tvoje teploty.
Adresu proto nikam nezveřejňuj. Kdyby ses obával úniku, na ThingSpeaku (API Keys) jde
vygenerovat nový Read key a přepsat ho v `CONFIG`.
