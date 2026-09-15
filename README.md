# Inventari de filament — Zenkai3D Studio

Aplicació d'una sola pàgina per portar l'inventari de bobines de filament.
No necessita servidor, compte ni connexió a Claude: tot funciona dins del
mateix navegador, allotjada al teu GitHub Pages.

## Fer-la servir

Obre `index.html` en qualsevol navegador, o publica-la a GitHub Pages
(instruccions més avall) per tenir-hi un enllaç fix i poder-la afegir a la
pantalla d'inici del mòbil.

## Publicar-la a GitHub Pages

1. Crea un repositori nou a GitHub (pot ser privat).
2. Puja `index.html` i `.nojekyll` (aquest README és opcional).
3. **Settings → Pages** → "Build and deployment" → *Deploy from a branch* →
   branca `main`, carpeta `/ (root)` → Desa.
4. Al cap d'un minut tindràs un enllaç com
   `https://elteuusuari.github.io/elrepositori/`.
5. Des de l'iPhone: obre'l amb **Safari** → icona de compartir → **Afegeix a
   l'inici**, per tenir-la com una app amb icona pròpia.

## Fes una foto — què fa de veritat i què no

En comptes de dependre de cap servei extern, la lectura funciona tota dins
del teu navegador, amb una llibreria de codi obert (Tesseract.js):

- **Marca, material, acabat i pes nominal**: es llegeixen intentant
  reconèixer el text de l'etiqueta. Funciona bé quan el text és net i de
  cara; amb lletra molt estilitzada, reflexos o fotos de biaix pot fallar
  o no trobar-hi res — per això sempre pots corregir-ho a mà, i els texts
  que hagi trobat surten com a botons per si el que busques hi és però en
  un altre camp.
- **Color**: toca directament el filament a la foto. Això és una mesura de
  píxels, no una suposició — sempre és fiable.
- **Percentatge que queda**: toca 3 punts a la foto (el centre del nucli,
  la vora del filament enrotllat, i la vora de la brida) i es calcula sol
  a partir d'això. És semi-manual a propòsit: cap algorisme automàtic
  endevina això de manera fiable amb una sola foto feta de qualsevol
  manera, així que en comptes de prometre un número que després falla,
  et demana tres tocs que triguen cinc segons.

Res d'això necessita internet un cop carregada la pàgina, excepte la
primera vegada que fas una foto (Tesseract es baixa el seu propi motor de
lectura la primera vegada que l'uses).

## Portar el que ja tenies

Si venies de la versió allotjada a Claude: pestanya **Importa** → **Exporta
JSON** a la versió antiga, i **Importa** → enganxa-ho → **Substitueix-ho
tot** aquí. Cada adreça web té el seu propi magatzem, no es comparteixen sols.

## Limitacions

- Les dades viuen només en aquest navegador i aquest dispositiu. Per
  tenir-ho sincronitzat entre mòbil i ordinador, exporta el JSON de tant en
  tant i importa'l a l'altre banda.
- La lectura de text és un ajut, no una garantia — revisa sempre el que
  trobi abans de desar la bobina.
