















# x) Lue/katso/kuuntele ja tiivistä.


### Hammond 2022: https://www.youtube.com/watch?v=oTD_ki86c9I

  - Kyseessä capture the flag -tehtävä
  - Ghidra on open source reverse engineering -työkalu.
  - Videossa käydään läpi Ghidran toiminta.
  - Ghidralla näkee siis erilaisten ohjelmien toiminnan. Kyseessä siis staattinen analyysi.

    <br/>
    <br/>

### Vapaaehtoinen: € Eagle and Nancy 2020: The Ghidra Book: 2. Reversing And Disassembly Tools: https://learning.oreilly.com/library/view/the-ghidra-book/9781098125684/xhtml/ch02.xhtml#ch02lev29

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

## Vaihe 1. Käänteismallinna packd -tiedosto C-kiellle.

Aloitin tehtävän avaamalla ghidraan packd -tiedoston ezbin-challenges kansiosta:

![image](https://github.com/user-attachments/assets/6fcf5b16-a50e-4e16-a9e8-9cae99aa290a)

Tämän jälkeen avasin kyseisen tiedoston dragonhead jutskalla:

![image](https://github.com/user-attachments/assets/2f86f309-205b-4a86-b0b7-01c6a2e44041)

Painoin analysointiin kyllä ja pääsin ohjelmaan.

Huomasin että jos ohjelma ei anna decompilata, niin tiedosto pitää vain käynnistää uudelleen:

![image](https://github.com/user-attachments/assets/a80a771d-0e46-47ec-8f0f-7affef385f38)

Tässä vaiheessa Ghidra on siis kääntänyt binäärin C-kielelle.


## Vaihe 2. Anna muuttujille sopivat nimet ja selitä ohjelman toiminta.


#c jeejee


# d)  Nora CrackMe: Käännä binääreiksi Tindall 2023

Aloitin tehtävän kloonaamalla Noran githun repositoryn omalla koneelle:

![image](https://github.com/user-attachments/assets/bd6eff88-4b04-4c22-8cee-8829722b0458)

Sitten luin README.md tiedoston ja seurasin sen ohjetta. Tämä oli niin simppeli kun ajaa make komento crackeme01.c tiedostolle. Tämä käänsi kyseisen tiedoston binääriksi ja se näytti avattuna tältä:

![image](https://github.com/user-attachments/assets/e0f3666b-1806-44ee-8841-de05a9727bc5)

Vinkki vinkkelson: .64 tiedoston perässä antaa vinkin siitä, miten koodi on muutettu binääriksi. Esim tässä tapauksessa se on muutettu base64 muotoon.

Käännän tarvittavat tehtävät samalla tavalla kun etenen niissä. En siis muuta kaikkia nyt binääriksi kerralla.


# e) Nora crackme01. Ratkaise binääri.

Ajamalla strings -komennon saa selville salasanan: password1

![image](https://github.com/user-attachments/assets/6ac4bf1e-c520-48ed-8864-00095248f0b4)

Ratkaisu:

![image](https://github.com/user-attachments/assets/be9e7dd7-82a2-4d2d-b635-9e5ee9f8f890)


# f) Nora crackme01e. Ratkaise binääri.

Tässä tapauksessa simppeli strings- komento toimii myös:

![image](https://github.com/user-attachments/assets/a1514089-21d0-42b2-a86f-0675d495b10e)

Kuten kuvasta huomaa, salasana on "slm!paas.k" mutta kun sen syöttää saa bash -virheen: 

![image](https://github.com/user-attachments/assets/cc048a11-7f1e-4024-9d6a-a2c930419921)

Tämä johtuu siitä, että bash olettaa että syöttäni salasana on bash -komento, sillä se sisältää huutomerkin "!". Aluksi luulin että siitä pääsisi läpi "" -merkeillä mutta pikainen bash-manuaalin selaaminen kertoi että tässä tapauksessa pitää käyttää '' -merkkejä.

Ratkaisu siis:

![image](https://github.com/user-attachments/assets/a0fb3afb-0103-4dd1-9eca-23e5bab1afd1)


# g) 













































## Tehtävissä myös hyödynnetyt lisälähteet

1. https://medium.com/geek-talk/how-to-reverse-engineer-your-first-binary-15a047c48649
2. https://www.gnu.org/software/bash/manual/bash.html#Quoting | Bash manuaali. Luettu 16.11.2024

