# Vefforritun 1, 2026: Verkefni 2, CSS

Útgáfa 0.2.

## Markmið

- Tengja CSS við HTML.
- Aðlaganir á HTML fyrir CSS.
- Notkun á grunn CSS með box model, visual formatting model og letri og litum.
- Nota flexbox.

## Verkefni 1–3

Í verkefnum 1, 2 og 3 munum við vinna áfram með sama verkefni og byggja ofan á það:

- [Verkefni 1](https://github.com/vefforritun/vef1-2026-v1) skilgreinir HTML og síður.
- [Verkefni 2](https://github.com/vefforritun/vef1-2026-v2) setur upp útlit með CSS.
- [Verkefni 3](https://github.com/vefforritun/vef1-2026-v3) gerir útlit skalanlegt (e. responsive) með CSS og setur upp tól til að hjálpa við vinnu og skipulag.

## Lýsing

Verkefnið er framhald af [verkefni 1](https://github.com/vefforritun/vef1-2026-v1), nýtir þær síður, gögn og myndir sem þar voru settar upp og fylgir þeirri verkefnalýsingu áfram en nú bætum við útliti við með CSS.

Sömu fjórar síður og í verkefni 1 skulu fá útlit:

- Forsíða ferðaþjónustufyrirtækis.
- Um ferðaþjónustufyrirtækið.
- Yfirlit yfir ferðir.
- Skráning í ferð.

Notið ykkar eigin lausn úr verkefni 1 sem grunn. Leyfilegt er að nota [sýnilausn að verkefni 1](https://github.com/vefforritun/vef1-2026-v1-synilausn) sem gefin verður út föstudaginn 11. september.

Allt útlitið skal vera í gefinni `./styles.css` og **allar** HTML skrár skulu vísa í nákvæmlega þá skrá.

Bæta þarf við auka elementum við lausn/sýnilausn til að geta náð fram útliti, sjá grunn sem gefinn er fyrir HTML í `index.html`.

Þar sem allt útlit skal útfæra í einni CSS skrá, skal huga að cascade og erfðum, þó er fullkomlega eðlilegt að endurtaka eigindi, en t.d. fyrir málsgreinar (`<p>`) þarf aðeins að taka fram einu sinni hvert margin þeirra er.

## Grunnur

Gefinn er HTML grunnur í `index.html` sem byggir á sýnilausn.

Gefið er `styles.css` skjal með grunn að lausn og athugasemdum.

Almennt skal gilda:

- Nota skal gefið „reset“ og `box-sizing` breytingu (merkt sérstaklega), það má ekki fjarlægja.
- Nota skal leturgerðina [Inter frá Google fonts](https://fonts.google.com/specimen/Inter), variable útgáfu.
  - Sækja skal leturgerðirnar (download) og nota `@font-face` í CSS, _ekki_ skal vísa í Google fonts með `<link>` í HTML.
- Gefin er stærð á letri sem `16px` (sem merkir að `1rem == 16px`), því skal ekki breyta.
- Í lýsingu á útliti er eitt bil skilgreint sem `10px`, tvö bil eru þá `20px` og svo framvegis.
- Gefin er hjálparklasi `.sr-only` sem skal setja á `Beint í efni` tengil og hugsanlega annað efni sem eingöngu er fyrir skjálesara.
- Aðeins skal nota `px` í grunnleturstærð og á `border`, `margin`, `padding` og `gap` skilgreiningar, annars skal nota hlutfallslegar einingar (`em`, `rem`, eða `%`)
- Allt efni (málsgreinar, myndir, form element) skal hafa að minnsta kosti eitt bil fyrir neðan sig.
  - Á fyrirmyndum gæti þetta verið óljóst og þarf ekki að vera nákvæmlega eins og á fyrirmyndum. Í nákvæmri lýsingu á útliti kemur fram ef vikið er frá þessu.
- Litir:
  - Bakgrunnur: `#ffeedd`.
  - Texti: `#000000`.
  - Border: `#000000`.
  - Takkar: bakgrununnur `#996644`, texti `#ffeedd`.
  - Bakgrunnur í fæti: `#996644`.
  - Önnur hver lína í töflu: `#eebb99`.
- CSS skal vera án villna og **viðvarana** þegar keyrt í gegnum [CSS validator](https://jigsaw.w3.org/css-validator/), einnig hægt að keyra gegnum W3C Validator extension.

Allt sem gildir í verkefni 1 gildir áfram í þessu verkefni.

## Útlit

Fyrirmynd að útliti er lýst hér að neðan ásamt skjáskoti úr sýnilausn. Öll skjáskot eru tekin í `1100px` breiðum vafra, ekki þarf að huga að skalanleika (síðan þarf ekki að líta vel út undir þeirri breidd).

### Haus síðu

Haus (`<header>`) skal vera með heiti síðu miðjað, leturstærð `52px` skilgreind í `rem`.

### Valmynd

- Valmynd er undir haus og fylgir þegar skrunað (scroll) er niður síðu, nær yfir alla breidd skjásins.
- Ekkert skal vera sýnilegt „undir“ valmynd þegar skrunað er.
- Leturgerð skal vera Atkinson Hyperlegible, leturstærð `24px` skilgreind í `rem`.
- Efni í valmynd skal miðjað með flexbox, ekki `text-align` eða `inline-block`.
- Þegar tengill í valmynd er valinn með tab (`:focus`) eða sveimað er yfir (`:hover`) skal setja undirstrik undir viðkomandi tengil.
- Núverandi síða er merkt með `<strong>` í stað tengils og skal hafa undirlínu.

### Meginmál

Allt efni á að vera að hámarki `1100px` breitt og miðjað í vafra, auka pláss vinstra og hægra megin skal sjálfkrafa vera útdeilt.

### Fótur

Bakgrunnslitur og border skal ná yfir alla breidd skjásins. Efni í fæti skal vera miðjað og að hámarki `800px` breitt.

Efni í fæti (`Opnunartímar`, `Hafðu samband`, `Samfélagsmiðlar`) skal skipt í þrennt með bili á milli:

- Bakgrunnur skal vera með áherslulit (accent), t.d. `#996644`.
- Bil frá efni skal vera á allar hliðar innan fótar, tvö bil.
- Notið flexbox til að ná þessu fram.

### Takkar

Sama útlit skal vera á „tökkum“ á forsíðu og skráningarsíðu (athugið að þó um takka _útlit_ sé að ræða skal huga að því hvaða element eiga við merkingarfræðilega, t.d. er senditakki í formi `<button>`):

- Bil innan takka (padding) skal vera eitt bil á hliðum og hálft bil fyrir ofan og neðan.
- Takki skal vera með svartan bakgrunn og hvítan texta.
- Takki skal hafa `5px` border radíus.
- Leturstærð skal vera sama og á meginmáli (16px í rem).

### Forsíða

Efni á forsíðu skal setja upp í jafn breið kort (cards) þar sem:

- Fyrst er fyrirsögn, stærð `32px` skilgreint í `rem`, feitletrað, vinstrasett.
- Síðan kemur mynd, fyllir upp í lárétt pláss, hæð `300px`, passið upp á að myndin haldi hlutföllum sínum (aspect ratio), hún skal fylla upp í pláss (`cover`).
  - Ef engin mynd þá kemur textinn í beinu framhaldi.
- Texti kemur síðan undir mynd, vinstrasett.
- Að lokum kemur takki neðst, vinstrasettur.
- Tvö bil á milli alls.

[Skjáskot úr sýnilausn](./fyrirmynd/forsida.png).

### Um síða

- Undir meginfyrirsögnum í texta skulu vera tvö bil.
- Eftir undirfyrirsagnir í texta skal vera eitt bil.
- Eftir málsgreinum skulu vera þrjú bil.
- Mynd skal fylla upp í lárétt pláss.

[Skjáskot úr sýnilausn](./fyrirmynd/um.png) og þegar [búið að skrolla til að sýna valmynd](./fyrirmynd/um-skroll.png).

### Ferðasíða

- Fyrirsagnir í töflu skulu vera feitletraðar, allt efni vinstrijafnað.
- Önnur hver röð í töflunni skal hafa `#eebb99` sem bakgrunnslit.

[Skjáskot úr sýnilausn](./fyrirmynd/ferdir.png).

### Skráningarsíða

- Hvert svæði í formi skal hafa fyrirsögn sem er `24px` skilgreint í `rem`, feitletrað, vinstrasett.
- Svæði skal fylla út í helming af breidd skjásins.
- Milli svæða skal vera þrjú bil.
- Milli reita skal vera tvö bil.

[Skjáskot úr sýnilausn](./fyrirmynd/skraning.png).

## Takmarkanir

Aðeins skal nota eftirfarandi eigindi, og ef tekið fram, viðeigandi gildi:

- `@font-face` til að fella inn leturgerðir
- `background` og nánari skilgreiningar
- `border` og nánari skilgreiningar
- `border-spacing: 0;` (fyrir töflur)
- `box-sizing` (en þó bara það sem gefið er)
- `color`
- `display: flex;`
  - önnur flex eigindi og `gap`
  - ekki ætti að nota önnur gildi fyrir `display`, sjá að neðan
- `font-family`
  - `src` til að vísa í skrár fyrir leturgerðir
- `font-style`
- `font-size`
- `font-weight`
- `list-style: none;`
- `margin-bottom` og `margin-top`
  - _ekki_ ætti að nota `margin-left` og `margin-right` heldur flexbox virkni til að búa til pláss á milli boxa
- `padding` og nánari skilgreiningar
- `width`, `height`, `min-width`, `max-width`, `min-height`
- `position`
- `left`, `right`, `top`, `bottom`
- `text-align`
- `text-decoration`
- Þau eigindi notuð í `.sr-only` og ekki tiltekin hér ætti ekki að nota í annað.

Nota ætti `type` og `class` selectora og í einhverju tilfelli pseudo-selectora. Ekki ætti að nota `id` selectora eða universal selector (`*`) fyrir utan það sem þegar er gefið.

Ekki skal nota önnur `display` gildi en `display: flex;`, `display: block` og `display: inline-block` má þó nota í sértækum tilfellum. Ekki nota `text-align` til að miðja efni. Ekki nota `float`, `clear` eða `vertical-align`.

## Netlify

Setja skal upp verkefni á Netlify með því að hlaða upp skrám með „manual deploy“ _eða_ tengja GitHub repo. Einnig er leyfilegt að nota aðra hýsingu en heyrið í kennara varðandi það.

## Mat

- 20% – Snyrtilega uppsett og gilt CSS.
- 15% – Grunn fyrirmæli og leyfileg eigindi notuð
- 10% – Haus og valmynd
- 10% – Fótur
- 10% – Forsíða
- 10% – Efnissíða
- 10% – Ferðasíða
- 10% – Skráningarsíða
- 5% – Uppsett á netlify

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 31. ágúst 2026.

## Skil

Skila skal í Canvas, seinasta lagi fyrir lok dags fimmtudaginn 17. september 2026.

Skilaboð skulu innihalda bæði:

- zip skrá með öllum skrám og möppum í lausn á verkefni (eða hlekkur á GitHub).
- slóð á verkefni keyrandi á Netlify, sett sem athugasemd við skil á Canvas.

Athugið að það er **ekki nóg** að eingöngu setja athugasemd, skila þarf verkefni sérstaklega. Verkefnum sem ekki er skilað fá ekki einkunn.

Ef skilað er eftir að skilafrestur rennur út mun einkunn vera lækkuð um 10% fyrir hvern dag sem liðinn er frá skilafresti, að hámarki 20% lækkun ef verkefni er skilað á sunnudegi. Eftir það mun verkefnið ekki fá einkunn. Hægt er að fá undanþágu með því að hafa samband við kennara áður en skilafrestur rennur út.

## Aðstoð

Leyfilegt er að ræða, og vinna saman að verkefni en **skrifið ykkar eigin lausn**. Ef tvær eða fleiri lausnir eru mjög líkar þarf að færa rök fyrir því, annars munu allir hlutaðeigandi hugsanlega fá 0 fyrir verkefnið.

Ekki er heimilt að nota stór mállíkön til að vinna verkefni í námskeiðinu, [sjá nánar um notkun](https://github.com/vefforritun/vef1-2026/blob/main/mallikon.md).

## Verkefni og einkunn

Sett verða fyrir fimm minni verkefni sem gilda 3% hvert, samtals 15% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 5%, samtals 10% af lokaeinkunn.

---

Nýjustu útgáfu af verkefni má [nálgast á GitHub](https://github.com/vefforritun/vef1-2026-v2).

## Útgáfusaga

| Útgáfa | Lýsing                                                      |
| ------ | ----------------------------------------------------------- |
| 0.1    | Fyrsta útgáfa                                               |
| 0.2    | Bæta við um lækkun vegna seinna skila; bæta við `AGENTS.md` |
