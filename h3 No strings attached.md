










# a) Strings

Aloitin tehtävän lataamalla tehtävänannosta tehtävän tiedostot omalla virtuaalikoneelle ( napsauta oikealla hiirinäppäimellä zip pakettia ja valitse "kopioi linkin osoite". Sitten vaikka avaat notepadin ja liität linkin siihen. Tästä saat zippitiedoston osoitteen ja voit hakea sen sisällön wgetillä virtuaalikoneen puolella. ps, muista purkaa paketti!)

Testasin tehtävän avautumisen ohjeen mukaisesti:
![image](https://github.com/user-attachments/assets/a4c1dfcd-9497-48b1-b0b8-e1fb6fff8ecf)

<br/>

Kun kyseisen tiedoston avaa linuxin sisäänrakennetulla ohjelmalla strings avautuu kyseisen ohjelman sisältö tekstinä:

<br/>

![image](https://github.com/user-attachments/assets/5048dcc4-15eb-49e1-a10d-edc8159ae986)

<br/>

Kuten saatatkin huomata, oikea salasana näkyy jo aikaisemmassa kuvankappauksessa:

<br/>

![image](https://github.com/user-attachments/assets/075d9cd3-0254-4bbe-a6cb-98d4b11fed25)

<br/>
<br/>
<br/>
<br/>

# b) Tee passtr.c -ohjelmasta uusi versio, jossa salasana ei näy suoraan sellaisenaan binääristä.

Tässä vaiheessa tuli tenkkapoo: Minä en osaa yhtään C:tä mutta ymmärrän miten tekisin "salauksen". Mitä siis teen? Opettelenko kokonaan uuden kielen? Siihenhän menee kymmeniä tunteja ja minulla on rajatusti aikaa.

<br/>

Päädyin siis kysymään koodin chatgpt:ltä. Itse tiesin jo tässä vaiheessa että pystyisin sekoittamaan koodin näkymisen strings komennossa vaihtamalla simppelisti salasanan binäärimuotoon. Salasana näkyisi siis tällöin strings näkymässä binäärinä, mutta käyttäjä pystyisi kirjoittamaan salasanan käyttämällä aakkosia (Binääri on siis suoraan verrannollinen aakkosiin). 

<br/>

Kun muotoilin omat kriteerini promptiksi, sain seuraavan esimerkki vastauksen.

<br/>

![image](https://github.com/user-attachments/assets/6e579b81-ddc1-419d-8995-fe7edd08d585)

<br/>

Tein nopean testauksen binäärimuunnoksen toimivuudesta [netistä](https://www.onlinegdb.com/online_c_compiler) löytyvällä koodaustesterillä ja voila, kaikki toimii:

<br/>

![image](https://github.com/user-attachments/assets/267e9cb8-cbf6-49f2-933d-56c7391589c7)

<br/>
<br/>
<br/>
<br/>

# c) Packd

Aloitin tehtävän kokeilemalla aikaisemmin tehdyn strings tempun, jolloin ohjelma palautti seuraavan printin:

![image](https://github.com/user-attachments/assets/c06783b1-bee4-4b2f-b9dd-056fb677db9f)

Kuten kuvasta huomataan, salasana löytyy mutta se on saanut puukkojunkkarin puukosta! Salasana on riekaleina ja se ei toimi tuollaisenaan! Mutta huolet pois! Vinkkejä junkkarin nimestä saadaan salasanan alta löytyvästä tekstistä: "This file is packed with the upx executable packer...".

<br/> 

Kuka on tämä herra UPX? Miksi hän puukotti salasanaa? Mitkä ovat hänen vaatimuksensa?

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

... ... ...

<br/>
<br/>
<br/>
<br/> 

HAH! Luulitko jo että aion luovuttaa!??! Sanon sinulle saman mitä sanon verenluovutuksessa: EN KOSKAAN LUOVUTA! 

<br/>

Tänäpäivänä meille on jotain mitä Raumalaisilla ei ole: Teknologiaa!

<br/>

Näihin kysymyksiin saamme nimittäin vastauksen osoitteesta googlaamalla https://upx.github.io/!

<br/> 

Mutta nyt pulinat pois. Nopean selvityksen jälkeen sain selville että UPX on avoimeen lähdekoodiin perustuva pakettien ja tiedostojen pakkaustyökalu. Ja vain hän voi palauttaa poloisen salasanamme sen alkuperäiseen kokoon.

<br/> 

Aloitin tehtävän lataamalla UPX työkalun edellämainitusta osoitteesta. Latauksen jälkeen tilanne oli tämä:

<br/> 

![image](https://github.com/user-attachments/assets/9f2be6cf-802f-47e8-a501-27ed73b810cf)

<br/> 

Itse UPX avattuna:

<br/> 

![image](https://github.com/user-attachments/assets/78fce00d-642a-4ec0-aaad-771ebb071bb4)

<br/> 

Tässä kohtaan tein samaan sijaintiin kopion packd -tiedostosta ja yritin avata sen komennolla "upx -d packd". Ja bash alkoi valittaa ettei komentoa löydy:

<br/> 

![image](https://github.com/user-attachments/assets/5026af5f-0ddd-4447-a69a-af6110e77577)

<br/> 

 Tässä kohtaa joku tohelo saattoi tai ei saattanut jäädä jumiin tähän pisteeseen kolmeksi tunniksi. Ja tämä sama tohelo saattoi tai ei saattanut asentaa upx:sää useampaan kertaan ennen kuin tajusi että oikea komento on " ./upx -d packd"

<br/> 

![image](https://github.com/user-attachments/assets/3d96a4fe-a080-4253-ae58-cb9b8acfbfee)

<br/> 

upx alkoi ruksuttamaan ja purki tiedoston. Nyt string komento näyttää seuraavalta:

<br/> 

![image](https://github.com/user-attachments/assets/7bc1062a-a325-4aab-bd18-225dd42260de)

<br/> 

Halleluja! Herra salasana on palautettu omaan kunniaansa! Nyt eikun enää testaamaan:

<br/> 

![image](https://github.com/user-attachments/assets/9e0464a3-18e6-4762-9836-e042b350415a)

<br/> 

JES! Homma onnistui!

<br/> 

Tässä vaiheessa myös huomaa kuinka aikaisempi "this file is packed..." teksti on kadonnut pakkauksen purun jälkeen.

<br/> 
<br/> 
<br/> 
<br/> 
<br/> 
<br/> 

# Pohdintaa

Strings komento tuli minulle uutena. Sen käyttäminen olikin todella helppoa ja siitä on paljon hyötyä minulle tulevaisuudessa. Tehtävät olivat tällä viikolla helpompia kuin aikaisemmilla mutta niissä oli silti todella paljon opittavaa. Uutena asiana tuli myös tämä UPX:n käyttö. Olin aikaisemmin jo tiennyt sen olemassaolosta mutta en ollut käyttänyt sitä. Kuten tekstissä kävikin ilmi, oli minulla sen kanssa aluksi ongelma joka johtui inhimillisestä virheestä. Eli mohlomokasta.

<br/> 

![image](https://github.com/user-attachments/assets/d310df74-9370-43c5-ab37-f59413633638)
Mitä enemmän luen forumeilta linux postauksia, sitä enemmän alan ymmärtää tätä kuvaa.

<br/> 
<br/> 
<br/> 
<br/> 

## Tehtävän apuna käytetyt lähteet:

1. https://en.wikipedia.org/wiki/UPX | Luettu 6.11.2024
2. https://github.com/upx/upx | Selailtu läpi | 6.11.2024
3. https://youtu.be/0jVikfySiII | katsottu 7.11.2024





