## Intro

- Turtle Roy : [http://turtle-roy.herokuapp.com/](http://turtle-roy.herokuapp.com/)
- Ohjeita (englanniksi) Githubissa: [https://github.com/raimohanska/turtle-roy](https://github.com/raimohanska/turtle-roy))

## Harjoitellaan ilman tietokonetta

- Opettaja on tietokone, jolle oppilaat antavat käskyjä.
- Oppilaiden tehtävänä on liikuttaa opettaja huoneen toiseen nurkkaan (väistellen huonekaluja) käyttäen kolmea komentoa: "siirry eteenpäin", "käänny oikealle", "käänny vasemmalle".
- Jos oppilaat sanovat minkä tahansa muun komennolla, esim. "liiku eteenpäin", opettaja vastaa: "En ymmärrä komentoa."
- Tarkoituksena on auttaa oppilaita ymmärtämään, että tietokoneet tottelevat vain täsmällisiä komentoja. (Jos kilpikonnalle ei sano tarkasti oikeaa komentoa, hän vastaa punaisella tekstillä.)

## Koodataan!

- Hiukan Turtle-grafiikkaa

```
clear
fd 100
lt 90
fd 100
rt 90
fd 20
```

- Sekvenssi, eli tehdään asioita peräkkäin

```
s [fd 100, lt 90]
```

- Toisto, eli tehdään sama juttu monta kertaa (kokeile muuttaa parametrejä -\> jännän äärellä)

```
r 4 (s [fd 100, lt 90])
```

- Funktiot, eli opetetaan tietokoneelle juttuja

```
let askel = s [fd 100, lt 90] 
let neliö = r 4 askel
neliö
```

- Parametrisoidut funktiot, eli tehdään samalla koodilla eri kokoisia juttuja

```
let ympyra sade = repeat 45 (s [fd sade, lt 8]) 
ympyra 2 
ympyra 4
```

- Rekursiiviset funktiot, eli itseään kutsuvat funktiot

```
let spiral x = if x == 0 then fd 0 else s [fd x/10, rt 10, spiral (x - 1)]
spiral 100
```

## Jatkoharjoitus: funktioiden yhdisteleminen

- Äänien soittaminen peräkkäin eli melodia. Kokeile soittonopeuden (500) muuttamista pienemmäksi!
- Huom! Toimii tällä hetkellä vain Chrome-selaimessa.

```
let tuiki nopeus = play [c, c, g, g, a, a, g, g, f, f, e, e, d, d, c] nopeus
tuiki 500
```

- Tee kiemuroista kukka

```
let kiemura x = if x == 0 then fd 0 else s [fd x/10, rt 10, kiemura (x - 1)]
let kukka = r 6 (kiemura 102)
kukka
```

- Soita melodia ja piirrä kukka yhtäaikaa.

```
par [kukka, tuiki 160]
```

- Lataa jatkoharjoituksen koodit valmiina: [http://turtle-roy.herokuapp.com/?turtle=LE1BOI519Z](http://turtle-roy.herokuapp.com/?turtle=LE1BOI519Z)

## Vinkkejä

- `clear` tyhjentää ruudun ja palauttaa konnan keskelle
- ` ↑ ` (nuoli ylös)
 - pääset tekemään edellisen jutun uudestaan
 - voit myös muokata komentoriviä liikkumalla sivunuolilla ja lisäämällä ja poistamalla tekstiä
- `ctrl-e` menee rivin loppuun
- `ctrl-a` menee rivin alkuun
- "show editor" -linkistä pääsee muokkaamaan koko ohjelmaa. "run" suorittaa sen alusta.
- Työn tallennus
 - `login "petteri"`
 - `save "häkkyrä"`
- Työn lataus
 - `login "petteri"`
 - `ls`
 - `open "häkkyrä"`
