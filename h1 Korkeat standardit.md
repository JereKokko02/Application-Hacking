# Tämä tiedosto sisältää Sovellusten hakkerointi ja haavoittuvuudet -kurssin ensimmäisen viikon tehtävän *H1 korkeat standardit* vastaukset. 

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

# a) Tutustu kurssin sanastoon, joka on määritelty SFS-EN ISO/IEC 27000:2020:en standardissa, kappaleessa 3. Terms and Definitions. Selvitä seuraavien kappaleiden määritteet ja selitä omin sanoin mitä ne tarkoittavat: 3.2, 3.31, 3.56, 3.58, 3.77

<br/>

- 3.2: Hyökkäys on keino tuhota, paljastaa, muokata, poistaa käytöstä, saada luvatta haltuunsa, tai käyttää luvatta omaisuutta.

<br/>
  
- 3.31: Tietoturvaloukkaus on tapahtuma jossa omaisuutta varastetaan tai sen varastaminen tehdään mahdolliseksi tietoturvahyökkäyksen ansiosta.

<br/>

- 3.56: Vaatimus on sovittu kriteeri joka vaaditaan jokaisen allekirjoittaneen organisaation  täytettäväksi, tai se on itsestään selvä toimenpide joka täytyy suorittaa.

<br/>

- 3.58: Tarkistus on toimenpide jolla tarkastetaan vaatimusten noudattaminen.

<br/>

- 3.77: Haavoittuvuus on kohde jota voidaan hyödyntää rikolliseen toimintaan. Haavoittuvuus mahdollistaa hyökkäyksen.

<br/>
<br/>
<br/>



# b) Tutustu standardiin ISO 27034-1 - 5. Selvitä mistä standardi kokonaisuudesta on kyse.

<br/>

ISO 27034 on standardi joka sisältää kuusi osaa. Nämä osat ovat: 1. Yleiskatsaus ja käsitteet, 2. Organisaation normatiiviset puitteet, 3. Sovelluksen tietoturvan hallintaprosessi, 4. Sovelluksen suojauksen validointi, 5. Protokollat ​​ja sovellusten suojauksen hallintatietorakenne, sekä 6. Turvallisuusohjeet tiettyjä sovelluksia varten. Yhdessä nämä osat antavat ohjeet sekä täytettävät kriteerit organisaatiolle ISO 27034 standardin käyttöönotolle.

Pähkinänkuoressa ISO 27034 standardin osat 1-5 antavat siis organisaatiolle perustan kyseisen standardin sovellusturvan hallintaan.

<br/>
<br/>
<br/>



# c) Kuuntele podcast: Meurman 2021. Laatulöpinät 30.
## Mitä mieltä olet podcastin väittämistä?

<br/>

### 1. *Mikään ohjelmisto ei ole täysin tietoturvallinen.*

<br/>

   - Olen samaa mieltä Kokkolan kanssa siitä ettei mikään ohjelmisto ole täysin tietoturvallinen. On vain olemassa ohjelmistoja jotka hoitavat tietoturvan paremmin kuin toiset ohjelmistot. Aina löytyy jokin haavoittuvaisuus!
  
<br/>
  
### 2. *Hallinnollinen tietoturva on teknisen tietoturvan onnistumisen edellytys.*

<br/>

   - Tästäkin olen samaa mieltä. Hallinnollinen tietoturva pitää huolen siitä, että yrityksellä on selvä strategia tietoturvan suunnittelulle, sen toteuttamiselle, sekä sen ylläpidolle. Tämän lisäksi hallinnollinen tietoturva antaa yrityksen henkilöstölle myös selvät ohjeet siitä, mitä pitää tehdä että tietoturva onnistuu, kuinka se toteutetaan, ja mikä on toteutettavien toimien tarkoitus.

<br/>

### 3. *Automaatiotestaus on ohjelmiston tietoturvan kannalta erittäin tärkeää.*

<br/>

  - Minusta automaatiotestaus on tietoturvan kannalta tärkeää, sillä se usein poistaa ihmisvirheen prosessista (Jos siis testaus suoritetaan ohjelmilla jotka on todettu toimiviksi). Tämän lisäksi automaatiotestaus nopeuttaa ja sulavoittaa testausprosessia --> projekti pysyy aikataulussa. Tämän lisäksi koneet löytävät myös kooditasolla / laitteistotasolla myös ne ongelmat joita ihminen ei edes kykene näkemään. Kuitenkin kuten Kokkolakin podcastissa toteaa, automaatiotestauksellakin on haittapuoli juuri esimerkiksi koodin lukemisessa. Ohjelma toki sanoo että koodi toimii, mutta se voi olla täysin spagettikoodia ihmisen silmille. Testauksella pitää siis olla selvä tarkoitus --> yhteydessä hallinnollisuuteen!

<br/>

### 4. *Ohjelmistoa suunniteltaessa voidaan tehdä paljonkin auttamaan käyttäjää toimimaan tietoturvallisesti. Usein nämä toimenpiteet kuitenkin vaikuttavat negatiivisesti käytettävyyteen.*

<br/>

   - Olen samaa mieltä. Itsekin olen joutunut kirjoittamaan monet salasanat *trial-and-error* metodilla läpi kun olen rekistöröitynyt uuteen palveluun. Itse asiassa olen kirjautunut elämäni aikana tasan yhteen palveluun jossa salasanan kriteerit oli täydellisesti ilmoitettu rekisteröitymisvaiheessa. Itsestäni tuntuu että tällaiset käytettävyyteen negatiivisesti vaikuttavat tietoturvatoimet johtuvat siitä, että a) Tietoturvakriteereitä ei ole selvästi suunniteltu suunnitteluvaiheessa, tai b) niitä on lähdetty toteuttamaan pilke silmäkulmassa ja koko homma on lähtenyt käsistä.

<br/>

### 5. *Ohjelmiston tietoturvallisuuden suunnitteluun vaikuttaa paljolti se, kuinka arkaluonteisia tietoja ohjelmistolla on tarkoitus käsitellä.*

<br/>

  - Tästä väittämästä olen samaa mieltä. Arkaluonteinen materiaalihan ei tarkoita esimerkiksi potilastietoja tai henkilötietoja, vaan se kattaa kaiken sen materiaalin jonka katoamisella on suuri vaikutus henkilöön tai henkilöihin. Eli siis liiketoimintasalaisuudet, patentit, liiketoiminnalle tärkeät tiedostot jne, luokitellaan arkaluontoisiksi materiaaleiksi. Ja aina kun käsitellään Arkaluontoista materiaalia, pitää sen tietoturva suunnitella jo suunnitteluvaiheessa sillä se voi vaatia erikoisratkaisuja.

<br/>

### 6. *Ohjelmistokehittäjät näkevät omat ohjelmistonsa aina merkittävästi riskialttiimpina, kuin muiden tekemät ohjelmistot.*

<br/>

  - Olen eri mieltä väittämän kanssa. Mielestäni tässä väittämässä on enemmän kyse ohjelmistokehittäjän kokemuksesta. Juniorikehittäjä ei ole saanut vielä tarpeeksi kokemusta että voisi pitää omia ohjelmistojaan Fort Knoxin seuraajina. Veteraanikehittäjä taas tietää todennäköisemmin oman koodinsa vahvuudet ja heikkoudet ja voi täten verrata niitä toisten tekemiin ohjelmistoihin. Sanoisinkin siis, että väittämä on totta Juniorikehittäjän kohdalla.

<br/>
<br/>
<br/>



# d) Asenna Debian 12-Bookworm virtuaalikoneeseen.

Tehty onnistuneesti aikaisempaa osaamista hyödyntäen. En keksi mitään muuta kirjoitettavaa joten tässä puujalkavitsi: 

<br/>

Mitä hämähäkki teki tietokoneella?

<br/>

Loi verkkosivun. 🕷️🕸️

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

# Lähteet joita on myös hyödynnetty tehtävien yhteydessä:

### 1. Sovellusten hakkerointi ja haavoittuvuudet - ICI012AS3A-3001 -kurssin materiaali: "ISO27000-2020-en.pdf" PDF-tiedosto. | Luettu 26.10.2024

### 2. Sovellusten hakkerointi ja haavoittuvuudet - ICI012AS3A-3001 -kurssin materiaali: "ISO27034-1-1719737070995" PDF-tiedosto. | Luettu 26.10.2024

### 3. Laatulöpinät-podcast: Tietoturvallisuus ohjelmistokehityksessä 25.10.2021. https://www.arter.fi/podcast/laatulopinat-podcast-tietoturvallisuus-ohjelmistokehityksessa-tarkastele-kokonaisuutta-ja-hyodynna-viitekehykset/ | Kuunneltu 12.10.2024

### 4. Savelan.fi Mitä tarkoittaa hallinnollinen tietoturva? https://www.savelan.fi/mita-tarkoittaa-hallinnollinen-tietoturva/ | Luettu 24.10.2024.

### 5. https://github.com/akx/markdown-cheatsheet-fi/blob/master/Markdown-Ohje.md. | Kerrattu Markdownin käyttö 22.10.2024.


