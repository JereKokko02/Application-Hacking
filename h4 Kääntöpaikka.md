# Johdanto

Tämä on Sovellusten hakkerointi ja haavoittuvuudet - ICI012AS3A-3001 -kurssin neljännen viikon tehtävien vastausdokumentti. Kyseiset tehtävät ja niiden tehtävänannot löytää osoitteesta https://terokarvinen.com/application-hacking/#h1-korkeat-standardit. 

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

# x) Lue/katso/kuuntele ja tiivistä.


## Hammond 2022: https://www.youtube.com/watch?v=oTD_ki86c9I

  - Kyseessä capture the flag -tehtävä
  - Ghidra on open source reverse engineering -työkalu.
  - Videossa käydään läpi Ghidran toiminta.
  - Ghidralla näkee siis erilaisten ohjelmien toiminnan. Kyseessä siis staattinen analyysi.

    <br/>
    <br/>

## Vapaaehtoinen: € Eagle and Nancy 2020: The Ghidra Book: 2. Reversing And Disassembly Tools: https://learning.oreilly.com/library/view/the-ghidra-book/9781098125684/xhtml/ch02.xhtml#ch02lev29

  - Kattava kirja Ghidran toiminnasta
  - Sisältää mm. Peruskäytön, ohjelman konfiguroinnin, esimerkkejä arkielämän käyttökohteista, jne.
  - 23 Chapteria.
  - Sisältää esimerkiksi data-analyysiä, syötteen analyysiä ja binäärin toiminnan analyysiä.
  - Aivoni sulaa kun selaan kirjaa.

<br/>
<br/>
<br/>
<br/>

# a) Asenna Ghidra.

Asensin gidran heidän sivuiltaan: https://ghidra-sre.org/

Tämän lisäksi jouduin asentamaan Java jdk-21 työkalun manuaalisesti, sillä sitä ei ole vielä hyväksytty Debianin pakettivarastoon. Tein sen tämän sivun ohjeiden mukaisesti: https://green.cloud/docs/how-to-install-java-jdk-21-or-openjdk-21-on-debian-12/

<br/>

Ja Ghidran asennus ja ajaminen komennolla /.ghidraRun:

<br/>

![image](https://github.com/user-attachments/assets/660e1b77-a3b1-4e9d-a4a1-2c671e44af51)

<br/>

Asennus onnistui ja kaikki toimii.

<br/>
<br/>
<br/>
<br/>

# b) rever-C. Käänteismallinna packd-binääri C-kielelle Ghidralla. Etsi pääohjelma. Anna muuttujielle kuvaavat nimet. Selitä ohjelman toiminta.

<br/>

## Vaihe 1. Käänteismallinna packd -tiedosto C-kiellle.

Aloitin tehtävän avaamalla ghidraan packd -tiedoston ezbin-challenges kansiosta:

<br/>

![image](https://github.com/user-attachments/assets/6fcf5b16-a50e-4e16-a9e8-9cae99aa290a)

<br/>

Tämän jälkeen avasin kyseisen tiedoston codeBrowserilla:

<br/>

![image](https://github.com/user-attachments/assets/2f86f309-205b-4a86-b0b7-01c6a2e44041)

<br/>

Painoin analysointiin ja sen kaikkiin kysymyksiin kyllä ja pääsin ohjelmaan.

<br/>

Vinkki vinkkelson: Huomasin että jos ohjelma ei anna decompilata, niin tiedosto pitää vain käynnistää uudelleen:

<br/>

![image](https://github.com/user-attachments/assets/a80a771d-0e46-47ec-8f0f-7affef385f38)

<br/>

Tässä vaiheessa Ghidra on siis kääntänyt binäärin C-kielelle.

<br/>

Tähän kohtaan oma osaaminen lakkaakin. Tiedän mitä ohjelma tekee mutta en osaa selittää sitä kooditasolla. Mutta ei huolta jätän tämän vielä muistiin ja palaan siihen mahdollisesti myöhemmin.

<br/>
<br/>
<br/>
<br/>

## Vaihe 2. Anna muuttujille sopivat nimet ja selitä ohjelman toiminta.


#c Jos väärinpäin. Muokkaa passtr-ohjelman binääriä (ilman alkuperäistä lähdekoodia) niin, että se hyväksyy kaikki salasanat paitsi oikean.

En päässyt tässä etenemään sillä C-osaamiseni on vähäistä.

<br/>
<br/>
<br/>
<br/>

# d)  Nora CrackMe: Käännä binääreiksi Tindall 2023

<br/>

Aloitin tehtävän kloonaamalla Noran githun repositoryn omalla koneelle:

<br/>

![image](https://github.com/user-attachments/assets/bd6eff88-4b04-4c22-8cee-8829722b0458)

<br/>

Sitten luin README.md tiedoston ja seurasin sen ohjetta. Tämä oli niin simppeli kun ajaa make komento crackeme01.c tiedostolle. Tämä käänsi kyseisen tiedoston binääriksi ja se näytti avattuna tältä:

<br/>

![image](https://github.com/user-attachments/assets/e0f3666b-1806-44ee-8841-de05a9727bc5)

<br/>

Vinkki vinkkelson: .64 tiedoston perässä antaa vinkin siitä, miten koodi on muutettu binääriksi. Esim tässä tapauksessa se on muutettu base64 muotoon.

<br/>

Käännän tarvittavat tehtävät samalla tavalla kun etenen niissä. En siis muuta kaikkia nyt binääriksi kerralla.

<br/>
<br/>
<br/>
<br/>

# e) Nora crackme01. Ratkaise binääri.

<br/>

Ajamalla strings -komennon saa selville salasanan: password1

<br/>

![image](https://github.com/user-attachments/assets/6ac4bf1e-c520-48ed-8864-00095248f0b4)

<br/>

Ratkaisu:

<br/>

![image](https://github.com/user-attachments/assets/be9e7dd7-82a2-4d2d-b635-9e5ee9f8f890)

<br/>
<br/>
<br/>
<br/>

# e) Nora crackme01e. Ratkaise binääri.

<br/>

Tässä tapauksessa simppeli strings- komento toimii myös:

<br/>

![image](https://github.com/user-attachments/assets/a1514089-21d0-42b2-a86f-0675d495b10e)

<br/>

Kuten kuvasta huomaa, salasana on "slm!paas.k" mutta kun sen syöttää saa bash -virheen: 

<br/>

![image](https://github.com/user-attachments/assets/cc048a11-7f1e-4024-9d6a-a2c930419921)

<br/>

Tämä johtuu siitä, että bash olettaa että syöttäni salasana on bash -komento, sillä se sisältää huutomerkin "!". Aluksi luulin että siitä pääsisi läpi "" -merkeillä mutta pikainen bash-manuaalin selaaminen kertoi että tässä tapauksessa pitää käyttää '' -merkkejä.

Ratkaisu siis:

<br/>

![image](https://github.com/user-attachments/assets/a0fb3afb-0103-4dd1-9eca-23e5bab1afd1)

<br/>
<br/>
<br/>
<br/>

# f) Nora crackme02. Nimeä pääohjelman muuttujat käänteismallinnetusta binääristä ja selitä ohjelman toiminta. Ratkaise binääri.

<br/>

Strings ei tässä toimi sillä password1 ei ole toimiva salasana:

<br/>

![image](https://github.com/user-attachments/assets/27a3fb22-72b8-46b9-9fc3-f22379b9ed0e)

<br/>

Tässä pitää siis käyttää Ghidraa.

<br/>

### Ghidra osuus

Aloitetaan main funktiosta (Löytää symbol trees --> functions):

<br/>

![image](https://github.com/user-attachments/assets/6b3e58cc-69bd-47a8-911a-967a048c228e)

<br/>

Tässä kohtaa pitää tulkata itse C-kieltä. Tässä vaiheessa allekirjoittanut lähtee selvittämään.

<br/>

Ensiksi etsitään kohta missä ykkönen saa arvon 0 kun asia x tapahtuu. Löysin sen tästä:

<br/>

![image](https://github.com/user-attachments/assets/a6d28a4e-f958-4acd-93c8-e73e6785eb4c)

<br/>

Eniten tässä alkoi kiinnostamaan tämä osio:

<br/>

![image](https://github.com/user-attachments/assets/b2000d51-1d9e-4367-884d-0c12772a283a)

<br/>

En tienny entuudestaan mitä C-kielessä \0 tarkoitti joten googlasin sen. Vastaukseksi sain että se on NULL arvo eli arvo joka ei ole mikään merkki tai numero.
Hehe taidanpa tietää mitä tehdä.

<br/>

Noh jos kerta herra haluaa tyhjän arvon niin annetaan sille:

<br/>

![image](https://github.com/user-attachments/assets/0ceaf360-b245-4d6b-ab95-38e168e0966f)

<br/>

Jos elämä olisi yhtä imelää leffaa, niin sanoisin tässä vaiheessa "Guys, I'm in".

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

# Pohdintaa

Ghidra oli todella mukava ohjelma käyttää. Se oli simppeli, siitä löytyi tutoriaaleja ja dokumentaatiota netistä ja sen maskotti on lohikäärme. Mitä muuta voisikaan edes ohjelmalta pyytää?

Tämän viikon tehtävät olivat haastavia mutta kun ne kerran kekkasi, oli helppo saada ainakin tärkeimmät kohdat tehtyä. Tämän lisäksi oli mielenkiintoista etsiä lisää tietoa C-kielestä ja ghidrasta netistä.

<br/>
<br/>
<br/>
<br/>

## Tehtävissä myös hyödynnetyt lisälähteet

1. https://medium.com/geek-talk/how-to-reverse-engineer-your-first-binary-15a047c48649 | Selailtu läpi 14.11.2024.
2. https://www.gnu.org/software/bash/manual/bash.html#Quoting | Bash manuaali. Luettu 16.11.2024.
3. https://youtu.be/fTGTnrgjuGA Ghidran codeBrowser pähkinänkuoressa | Katsottu 16.11.2024.

