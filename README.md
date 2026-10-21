# Dienpinigių skaičiuoklė: prototipas

Mokesčių SUFLERIO dienpinigių skaičiuoklės prototipas. Tikslas: išspręsti problemą, kai žmogus įveda šalį (pvz. „Vokietija“), bet nepasirenka jos iš pasiūlymų sąrašo, ir skaičiuoklė tyliai rodo 0,00 €.

**Peržiūra:** https://richkus.github.io/dienpinigiu-skaiciuokle/

## Kaip veikia šalies laukas

Šalies laukas yra mygtukas, į jį rašyti negalima. Paspaudus atsidaro skydelis su paieškos laukeliu ir šalių sąrašu. Taip lauke niekada nelieka parašyto teksto, kuris atrodo kaip pasirinkta šalis, bet ja nėra.

- Atidarius be pasirinkimo nieko nepažymėta. Pradėjus rašyti pažymimas pirmas atitikmuo, Enter jį pasirenka. Pasirinkta šalis sąraše pažymėta varnele.
- Paieška nekreipia dėmesio į lietuviškas raides ir ieško bet kurio žodžio pradžios („karalyst“ randa Jungtinę Karalystę).
- Jei tikslaus atitikmens nėra, nukerpamos 1-2 paskutinės raidės ir rodoma „Gal ieškote:“ („Vokietija“ → „Vokietijos Federacinė Respublika“).
- Kol šalis nepasirinkta, dienų laukas išjungtas (numatyta reikšmė 0). Pasirinkus šalį jis įsijungia ir kursorius pereina į jį.
- Kol šalis nepasirinkta, Norma ir Suma rodo „–“, ne 0,00 €. Uždarius skydelį nepasirinkus šalies, laukas paraudonuoja ir rodoma „Pasirinkite šalį iš sąrašo.“
- Galima pridėti kelias šalis, skaičiuojama bendra suma.

Normos yra **pavyzdinės**, ne tikri duomenys. Sąraše 28 šalys.

## Stilius

- Puslapis ir skaičiuoklė: Figma „Dienpinigių skaičiuoklė“ (node 4177:11106).
- Pasiūlymų skydelis, paieškos laukelis ir klaidos žinutė: DS V.3 „Inputs“ (8138:3541) ir „Modals“ (8138:5355), kintamieji `--ds-*`.
- `svetaine-tokens.css`: dabartinės svetainės reikšmės (`--ms-*`).

## Struktūra

```
index.html           prototipas: HTML, CSS ir JS viename faile
svetaine-tokens.css  svetainės CSS kintamieji
assets/icons/        ikonos iš Figma
assets/img/          logotipas, iliustracijos, atmintinės nuotrauka
assets/logos/        klientų logotipai
```
