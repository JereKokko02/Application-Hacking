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
  
<br/>

## PortSwigger: [Access control vulnerabilities and privilege escalation](https://portswigger.net/web-security/access-control)
  -
  -
  -
  -
  
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



# b)





# g) Vapaaehtoinen

<br/>

Ratkaisin tehtävän:

<br/>

![image](https://github.com/user-attachments/assets/3ea17b02-3e4f-46b5-9fd9-b9fd059cc013)

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




# Pohdintaa (Ei tarvitse arvioida jos ei halua)

<br/>

Ymmärrän SQl kielen käytön ja sen miten se hakee taulukosta haluttavat arvot. Itse injektoiminen taas oli minusta todella vaikeaa sillä a) Kieli oli minulle uusi (Infrapuolella tasan yhdellä kurssilla katsottiin 30 min SQL injektion toimintaa, ja b) Tähän mennessä minulla ei ole ollut tarvetta opetella sitä.

<br/>

"Meikämandoliini yrittämässä injektoida SQL koodia 500.kertaa webbisivulle tuloksetta (Koodissani on satoja simppeleitä virheitä)"
![image](https://github.com/user-attachments/assets/9371d86e-bba4-4056-a414-bacc05566db2)



