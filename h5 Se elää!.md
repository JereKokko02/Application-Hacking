# Johdanto

Tämä on Sovellusten hakkerointi ja haavoittuvuudet - ICI012AS3A-3001 -kurssin viidennen viikon tehtävien vastausdokumentti. Kyseiset tehtävät ja niiden tehtävänannot löytää osoitteesta https://terokarvinen.com/application-hacking/#h1-korkeat-standardit. 

<br/>

Tämän tehtävädokumentin testit on tehty Debian 12 Bookworm virtuaalikoneella Oracle Virtual Boxia käyttäen.
Tässä on kyseisten ohjelmien versiot:

<br/>

- Debian 12.7 Bookworm
- Oracle Virtual Box version 7.0.14 r161095 (Qt5.15.2)
- Isäntäkoneen työpöytäversio Windows 11 Home

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

# a) Lab1. Tutkiminen mikä on ohjelmassa vialla ja miten se korjataan.

Minulla oli ongelmia gbd:n käyttämisessä joten teen tämän tehtävän nytten lähdekoodin perusteella:

<br/>

![image](https://github.com/user-attachments/assets/2be4fe35-6bc5-4674-a4bf-4b3ea228503c)

<br/>

Koodi ei toimi seuraavista syistä:

1. Char * Bad messagen arvo on "null" , eli se ei johda mihinkään arvoon jota ohjelma voisi käyttää.
2. Print_scrambled(bad_message); Ei tuota mitään null -arvon vuoksi.

<br/>
<br/>
<br/>
<br/>

# Lab2. Selvitä salasana ja lippu + kirjoita raportti siitä miten aukesi.

Tässä on nyt se ongelmana että tehtävää ei voi ratkaista ilman gdb:n osaamista. Lähdekoodistahan salasanan löytää heti mutta se ei ole tehtävän tarkoitus. Nyt en osaa muuta sanoa kuin että tämä tehtävä jää parannettavaksi.

<br/>
<br/>
<br/>
<br/>

## Tehtävissä myös hyödynnetyt lisälähteet

1. https://www.youtube.com/watch?v=Dq8l1_-QgAc&t=73s | Katsottu 29.11.2024
2. https://www.geeksforgeeks.org/null-pointer-in-c/ | Luettu 24.11.2024






