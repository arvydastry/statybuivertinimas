# statybuivertinimas.lt — svetainė (statinė versija, Harbor kryptis)

Vienas savarankiškas failas: **`index.html`**. Atidaryti dukart spustelėjus arba `open index.html`.
Ankstesnė tamsi versija (jurkas.lt kryptis) palikta kaip `index-v1.html`.

## Dizaino kryptis — Salient „Harbor“

Perimti konkretūs Harbor elementai, ne tik nuotaika:

| Harbor elementas | Kaip panaudota |
|---|---|
| Bėganti juosta viršuje su ◆ | Terakotos juosta: kaina, tel. nr., nepriklausomumo pažadas |
| Pilno ekrano foto/video + milžiniška antraštė apačioje | Drono video virš statomų namų + „Antra nuomonė.“ per visą plotį |
| Info juosta po hero (miniatiūra · pill mygtukas · „(etiketė)“ · tekstas · ↓) | Tas pats trijų stulpelių išdėstymas |
| Didelis lengvo svorio teiginys (statement) | „Rangovas nori parduoti darbus…“ |
| „(About Us)“ · tekstas · apvalintas portretas | „(Apie konsultantą)“ blokas pirmuoju asmeniu |
| Horizontaliai slenkančios spalvotos panelės su 01/02/03 | 5 situacijos: terakota / gintaras / dangus / juoda / smėlis, su aukštomis nuotraukomis |
| Teiginys virš dangaus foto, žodžiai ryškėja slenkant | „Nerekomenduojame parduotuvių…“ |
| Statistika su pill etiketėmis | 3 skaičiai virš dangaus |
| Foto koliažas + sąrašas | Stogo konstrukcija + mūras, 4 rezultatai, „ką randame sąmatose“ |
| Spalvotos atsiliepimų kortelės su didele raide ir portretu | 3 kortelės, švelniai pasuktos |
| Pill (juodi apvalūs) mygtukai su ↗ apskritimu | Visi CTA |
| Milžiniškas prekės ženklo žodis footer'yje su spalvų švytėjimu | „Statybų įvertinimas“ |

Šriftas — **Inter Tight** (tas pats, kurį naudoja Harbor), svoris 400–500, jokio bold.
Spalvos: `#E4522E` terakota, `#F5A800` gintaras, `#8FC4F0` dangus, `#EFE9DD` smėlis, `#1B1B1B` tekstas.

## Kodėl tai neatrodo „AI“

- Tikros nuotraukos ir du video vietoj ikonų tinklelių ir gradientų: konsultanto portretas — savas (`img/konsultantas.jpg`), likusios — Pexels (sąrašas — `media.md`)
- Asimetriniai išdėstymai: trijų stulpelių „(etiketė) · tekstas · foto“, persidengiantis koliažas, pasuktos kortelės
- Konkretus tekstas: Kauno rajono vietovės (Garliava, Domeikava, Raudondvaris…), realios sąmatų klaidos („tinkavimas įtrauktas du kartus“), atsiliepimai su sumomis ir miesteliais
- Antraštės lengvu svoriu, dideli tarpai, skliaustinės etiketės — redakcinis, ne „SaaS“ tonas
- Jokių švytinčių blob'ų, jokių purpurinių gradientų, jokio „Premium Quality Solutions“

## Logotipas

Ženklas (namas + oranžinė varnelė) atkurtas kaip **inline SVG** pagal originalų logotipą — `currentColor` namui, `--terra` varnelei, todėl ant hero video jis baltas, o pastumdžius puslapį — juodas. Žodinis ženklas — Poppins 700 dviem eilutėmis. Tas pats ženklas naudojamas header'yje, footer'yje ir kaip favicon. Akcentinė spalva `--terra` suvienodinta su logotipo oranžine (`#F04A22`).

## Funkcionalumas (nepakitęs nuo v1)

- **3 skaičiuoklės**: tiksli vizito kaina (150 / 200 €), orientacinis statybos biudžetas, orientacinė žalos sutvarkymo kaina
- **Užklausos forma** 5 žingsniais + santrauka: dideli mygtukai, progreso juosta, „Atgal“, kaina realiu laiku, validacija tik vardui ir LT numeriui, auto-peršokimas tik pelės paspaudimu (ne klaviatūra)
- Tel. nr. **+370 639 65375** — juostoje, header'yje, info juostoje, formoje, CTA, footer'yje ir mobilioje apatinėje juostoje
- `prefers-reduced-motion`: video neautostartuoja, horizontalus slinkimas virsta vertikaliu, animacijos išjungiamos
- Mobiliai (<900 px): panelės sudedamos vertikaliai, hero antraštė lūžta į dvi eilutes, apatinė „Skambinti / Užklausa“ juosta

## Prieš paleidžiant

- Užklausa statinėje versijoje atidaro el. laišką (mailto) su santrauka; WordPress versija siunčia per įskiepį (`../statybuivertinimas-wp`)
- Pexels nuotraukas atsisiųsti ir talpinti savo serveryje (dabar kraunamos iš Pexels CDN)
- Statistikos skaičiai ir atsiliepimai — patikslinti tikrais duomenimis
- Skaičiuoklių koeficientai — patikslinti pagal praktiką
- Privatumo politika, slapukų juosta, jei bus analitika

## Privatumas ir slapukai

- `privatumo-politika.html` — bendrinė BDAR privatumo politika.
- Slapukų pranešimas: „Sutinku su visais“ / „Tik būtini“, pasirinkimas — `localStorage.cookie_consent`; analitika (`loadAnalytics()`) vykdoma tik sutikus su visais.

## WordPress versija

Salient temai skirta versija (Docker, child tema, įskiepis su skaičiuoklėmis, užklausa ir slapukais) — `../statybuivertinimas-wp`.
