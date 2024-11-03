# Johdanto

Tämä on Sovellusten hakkerointi ja haavoittuvuudet - ICI012AS3A-3001 -kurssin toisen viikon tehtävien vastausdokumentti. Kyseiset tehtävät ja niiden tehtävänannot löytää osoitteesta https://terokarvinen.com/application-hacking/#h1-korkeat-standardit. 

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

<br/>

## OWASP: [OWASP Top 10](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
  - Broken access control on tällä hetkellä vaarallisin turvallisuusriski.
  - Pähkinänkuoressa liittyy käyttöoikeuksiin (Ryhmäpolitiikan manipulointi, korotetut käyttöoikeudet root jne).
  - Suhteellisen helppo estää (ainakin teoriassa).
  - Tämän haavoittuvuuden mahdollistaa ihmistekijä sekä ohjelmien konfiguroinnin virheet.
    
<br/>

## Karvinen 2023: [Find Hidden Web Directories](https://terokarvinen.com/2023/fuzz-urls-find-hidden-directories/)
  - Fuff on työkalu jolla voi löytää piilotettuja hakemistoja verkosta.
  - Fuff etsii nettisivuilta normaalista näkymästä piilotettuja urleja.
  - Fuff on automaattinen ohjelma.
  - Fuzzeri jos oikein ymmärsin antaa ohjelmalla satunnaisia rikkinäisiä tai sekavia syötteitä jotta ohjelma tekee jotain odottamatonta.
  
<br/>

## PortSwigger: [Access control vulnerabilities and privilege escalation](https://portswigger.net/web-security/access-control)
  - Käyttöoikeuksien hallinta on tärkeä osa tietoturvaa
  - Käyttöoikeuksien hallinta määrää kuka saa muokata/nähdä mitäkin tietoa.
  - Vertical privilege escalation on eskalaatio jossa käyttäjä saa korotettua omat oikeudet esim, admin tasolle.
  - Horizontal privilege escalation taas on eskalaatio jossa käyttäjä pääsee käsiksi toisten käyttäjien tietoihin / järjestelmiin.
  - Miten estetään: Koulutusta, varmistusta ja toimivaa koodia!
  
<br/>

## Karvinen 2006: [Raportin kirjoittaminen](https://terokarvinen.com/2006/raportin-kirjoittaminen-4/)
  - Lähteet kuntoon!
  - Luettavuus ja täsmällisyys on tärkeintä! --> Muuten tekstistä ei saa selvää tai se ei  vastaa kaikkiin kysymyksiin.
  - Pahin moka akateemisissa tuotoksissa on plagiointi oli se sitten tapahtunut vahingossa tai ei!
  - Jos tuotos on ohje, se pitää olla kattava jotta lukija pääsee samaan lopputulokseen pelkkien ohjeiden avulla.

<br/>

## Vapaaehtoinen: [PortSwigger 2020: What is SQL injection?](https://www.youtube.com/watch?v=wX6tszfgYp4)
  - SQL injektio on webissä oleva turvallisuushaavoittuvuus joka mahdollistaa hyökkääjälle SQL pyyntöjen suorittamisen verkkosivuilla.
  - Tyypillisin ominaisuus SQL injektiossa on antaa jollekin parametrille arvo true.
  - SQL koodia voidaan injektoida mihin tahansa osaan SQL pyyntöä.
  - SQL koodia voidaan injektoida myös update,- insert,- ja select -statement osioihin
  - SQL injektion estäminen = varmistamatonta syötettä ei päästetä läpi.

<br/>
<br/>
<br/>
<br/>

# a)

Aloitin tehtävä [ohjeiden](https://terokarvinen.com/hack-n-fix/) mukaisesti. Asennus onnistui ongelmitta ja pääsin yhdistämään tehtävän verkkosivulle:

<br/>

![image](https://github.com/user-attachments/assets/f545af7b-1c8f-497d-ab2d-d37477ff7ee7)

<br/>

Ensimmäinen ongelma mikä tehtävässä vastaan oli se, ettei sivun syötteeseen pystynyt kirjoittamaan mitään muuta kuin numeroarvoja. Pienen pähkäilyn jälkeen sain selville, että pystyin vaihtamaan kehittäjätyökalujen avulla input typen arvon "number" tyhjäksi. Tämä mahdollistaa SQL koodin kirjoittamisen hakukenttään.

<br/>


![image](https://github.com/user-attachments/assets/e15daaf1-ab65-4469-b0cf-4e58168e9f6d)


<br/>

Seuraavaksi minun piti selvittää keino jolla saisin selville tehtävän ratkaisun. Koska en ole vielä ennen käyttänyt SQL-kieltä, oli minulla paljon opeteltavaa ennen kuin pystyin edes aloittamaan tehtävää. Olin jumissa tässä kohtaa useamman päivän ajan ja en vain saanut ratkaistua tehtävää vaikka yritin kaikkeni. Katsoin tehtävänannosta ratkaisun joka oli seuraava:

<br/>

![image](https://github.com/user-attachments/assets/2afacd75-440b-4b64-8771-9292d43e78b7)

<br/>

En ymmärrä miten kyseinen komento saa selville ratkaisun.

<br/>
<br/>
<br/>
<br/>

# b) Korjaa 010-staff-only haavoittuvuus lähdekoodista.

Tässä kohtaa jouduin heittämään pyyhkeen kehään, sillä vähäisellä sql:n ymmärryksellä tämän tehtävän ratkaiseminen ei minulla onnistunut. Tässä vaiheessa siirryin seuraavaan 020-your-eyes-only -tehtävään jotta saisin tehtyä sen määräaikaan mennessä. Mikäli tulevaisuudessa on mahdollista, palaan tekemään tämän tehtävän loppuun.

<br/>
<br/>
<br/>
<br/>

# c) Ratkaise dirfuzt-1 artikkelista Karvinen 2023: [Find Hidden Web Directories - Fuzz URLs with ffuf](https://terokarvinen.com/2023/fuzz-urls-find-hidden-directories/)

Aloitin tämän tehtävän tekemisen ohjeiden mukaisesti ja asensin dirfuzt-0:

<br/>

![image](https://github.com/user-attachments/assets/5af57ac1-b04c-4a8f-86d1-e59ddebfac71)

<br/>

ffuf työkalun ajaminen osoitteessa http://127.0.0.2:8000

<br/>

![image](https://github.com/user-attachments/assets/e0638975-905e-4934-b159-c426aef16200)

<br/>

Rajoittamalla sivun vastausajan 132:teen löysi ffuf sitten oikean admin hakemiston:

<br/>

![image](https://github.com/user-attachments/assets/c0725684-b05e-4358-9547-3b57b66d34f5)

<br/>

Tässä vaiheessa siirryin dirfuzt-1:seen ja ajoin aikaisemmin tehtyn haun uudestaan. Tässä kertaa Rajoittamalla vastausajan 154:seen löysi ffuf admin versionhallinnan, (.git) sekä versionhallinnan (wp-admin):

<br/>

![image](https://github.com/user-attachments/assets/ba9e19f9-4808-403c-b916-53c639781c5f)


<br/>

![image](https://github.com/user-attachments/assets/f749a0ba-de50-4953-970d-2e59fa65bada)


<br/>

![image](https://github.com/user-attachments/assets/36be6f19-9d25-49c5-8d2e-9a78dd3783d0)

<br/>

# d) Murtaudu 020-your-eyes-only

Asensin aluksi Djanko appin [ohjeiden](https://terokarvinen.com/hack-n-fix/) mukaisesti ja pääsin sisään webbisivulle:

<br/>

![image](https://github.com/user-attachments/assets/f44b0cb5-8539-453a-8303-737a01842ddc)

<br/>

Aloitin tehtävän ajamalla ensin ffuffin osoitteelle 127.0.0.1:8000, jolloin ffuff löysi vain admin kirjautumisen hakemiston:

<br/>

![image](https://github.com/user-attachments/assets/f7827ff2-9cf8-42f1-937b-ec96bb41df57)

<br/>

Tämän jälkeen testasin saman admin consolen osoitteelle 127.0.0.1:8000/admin-console, mutta ffuff ei löytänyt sieltä mitään. 

Kekkasin seuraavaksi tutkia itse admin kirjautumisen osoitetta 127.0.0.1:8000/accounts/login/?next=/admin-dashboard/ osoitetta ja ffuf alkoi löytää hakemistoja:

<br/>

![image](https://github.com/user-attachments/assets/db2ecdd2-3105-4ee9-9a8f-708cbf610f84)

<br/>

Tässä vaiheessa jäin jumiin pitkäksi aikaa, sillä en tiennyt mitä minä tällä tiedolla tekisin. Hetken mietiskelyn jälkeen menin katsomaan tehtävänannon vinkkejä ja luin kohdan: "Some views are available to all. Some are available to logged in users. Some only for admin.". Tämän nähtyäni kokeilin luoda oman käyttäjän "apina1" ja pääsin katsomaan miltä sivu näyttää kun kirjautuu sisään käyttäjänä.

<br/>

Testasin ffuffata uudestaan osoitteen 127.0.0.1:8000 jolloin ohjelma palautti taas hakemiston "admin-console". Huvin vuoksi kokeilin päästä sisään kyseiseen hakemistoon sisäänkirjautuneena ja hupsista!: 

<br/>

![image](https://github.com/user-attachments/assets/5fd5eb45-7af9-4b6a-b3dc-5102f7022ce6)

<br/>
<br/>
<br/>
<br/>

# e) Korjaa 020-your-eyes-only haavoittuvuus.

Tässä kohtaa minulla kävi sama kuin tehtävässä b). Infrapuolla tulee hyvin vähän koodattua ja sen huomasin näitä tehtäviä tehdessä. Olen kuitenkin katsonut ratkaisun teron sivulla Solution / Walktrough osiosta mutta minusta ei ole mitään järkeä käydä kopsaamaan toisen hiellä ja tuskalle tuotettua ratkaisua omaan tehtävädokumenttiini. Nöyrästi nostan siis hattua Robinille!

<br/>
<br/>
<br/>
<br/>

# g) Vapaaehtoinen

<br/>

Ratkaisin tehtävän:

<br/>

![image](https://github.com/user-attachments/assets/3ea17b02-3e4f-46b5-9fd9-b9fd059cc013)

<br/>
<br/>
<br/>
<br/>

# h) Vapaaehtoinen

<br/>

Ratkaisin tehtävän:

<br/>

![image](https://github.com/user-attachments/assets/c2e63525-d237-43ae-acea-b01349eca128)

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
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>




# Pohdintaa (Ei tarvitse arvioida jos ei halua tämä lähinnä omaksi iloksi)

<br/>

Ymmärrän SQL kielen käytön ja sen miten se hakee taulukosta haluttavat arvot. Itse injektoiminen taas oli minusta todella vaikeaa sillä a) Kieli oli minulle uusi (Infrapuolella tasan yhdellä kurssilla katsottiin 30 min SQL injektion toimintaa), ja b) Tähän mennessä minulla ei ole ollut tarvetta opetella sitä. Tämän lisäksi aikarajoitteet alkoivat painaa kovasti otsalohkoa viikon edetessä. Tämä lähinnä johtui siitä, että en saanut tehtäviä a) ja b) suoritettua itsenäisesti.

Suurena apuna tehtävissä oli PortSwigger sivuston käyttäminen sekä sen sisältämien labrojen tekeminen. Tulen varmasti tulevaisuudessa tutkimaan sivustoa vielä tarkemmin vaikka sitä ei tällä kurssilla enempää käytettäisikään. Esim Burp Suite vaikuttaa mielenkiintoiselta.



<br/>

"Meikämandoliini yrittämässä injektoida SQL koodia 500.kertaa webbisivulle tuloksetta (Koodissani on satoja simppeleitä virheitä)"

<br/>

![image](https://github.com/user-attachments/assets/9371d86e-bba4-4056-a414-bacc05566db2)

<br/>
<br/>
<br/>
<br/>

## Opiskelumateriaalien lähteet:

1. https://portswigger.net/web-security/sql-injection | Luettu 29.10.2024
2. https://www.w3schools.com/sql/ | Luettu 30.10.2024
3. https://www.youtube.com/watch?v=zsjvFFKOm3c | Katsottu 28.10.2024


