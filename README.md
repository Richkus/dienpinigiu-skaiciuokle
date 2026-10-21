# Dienpinigių skaičiuoklė: prototipas

Mokesčių SUFLERIO dienpinigių skaičiuoklės prototipas. Tikslas: išspręsti problemą, kai žmogus įveda šalį (pvz. „Vokietija“), bet nepasirenka jos iš pasiūlymų sąrašo, ir skaičiuoklė tyliai rodo 0,00 €.

**Peržiūra:** https://richkus.github.io/dienpinigiu-skaiciuokle/

## Variantai

Perjungiama apačioje dešinėje arba nuoroda:

| Nuoroda | Kas tai |
|---|---|
| [`?v=a`](https://richkus.github.io/dienpinigiu-skaiciuokle/?v=a) | **A · Rašymas.** Dabartinis laukas su pataisymais: jei šalis nepasirinkta, laukas paraudonuoja, rodoma klaida ir pasiūlymas „Gal turėjote omenyje“. Enter / Tab paima pažymėtą pasiūlymą. |
| [`?v=b`](https://richkus.github.io/dienpinigiu-skaiciuokle/?v=b) | **B · Sąrašas su paieška.** Laukas yra mygtukas, į jį rašyti negalima. Paspaudus atsidaro skydelis su paieškos laukeliu ir sąrašu. |

Abiem atvejais:

- kol šalis nepasirinkta, Norma ir Suma rodo „–“, ne 0,00 €;
- paieška nekreipia dėmesio į lietuviškas raides ir ieško bet kurio žodžio pradžios („karalyst“ randa Jungtinę Karalystę);
- jei tikslaus atitikmens nėra, nukerpamos 1-2 paskutinės raidės ir rodoma „Gal ieškote:“ („Vokietija“ → „Vokietijos Federacinė Respublika“);
- galima pridėti kelias šalis, skaičiuojama bendra suma.

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
