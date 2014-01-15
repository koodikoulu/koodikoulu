Intro
-----

1.  Tietokone - mitä osia kuuluu?
2.  Tiedosto, mikä se on?
3.  Ohjelma, mikä se on?

Koodataan!
----------

- Turtle Roy : [http://turtle-roy.herokuapp.com/](http://turtle-roy.herokuapp.com/) (API yms githubissa: [https://github.com/raimohanska/turtle-roy](https://github.com/raimohanska/turtle-roy))

- Hiukan Turtle-grafiikkaa

fd 100 lt 90 rt 90

- Lista

[1,2,3]

- Sekvenssi, eli tehdään asioita peräkkäin

s [fd 100, lt 90]

- Toisto, eli tehdään sama juttu monta kertaa (kokeile muuttaa parametrejä -\> jännän äärellä)

r 4 s [fd 100, lt 90]

- Funktiot, eli opetetaan tietokoneelle juttuja

let askel = s [fd 100, lt 90] let neliö = r 4 askel neliö

- Parametrisoidut funktiot, eli tehdään samalla koodilla eri näköisiä juttuja

let ympyra sade = repeat 45 (s [fd sade, lt 8]) ympyra 2 ympyra 4
