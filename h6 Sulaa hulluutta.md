







# a)  Tutki tiedostoa h1.jpg jo opituilla työkaluilla. Mitä saat selville?

<br/>

## Testatut menetelmät:

<br/>

Silmät:

<br/>

![image](https://github.com/user-attachments/assets/e9eb71c0-90b5-47fd-8636-58c2e0308cc0)

<br/>

Tämä kuva on tehty tekoalyä käyttäen jonka näkee jo ihan omilla silmillä. En löytänyt itse kuvasta mitään vinkkejä ja kuvan kirjoissa on oletetusti vain satunnaisia kirjainyhdistelmiä.

<br/>
<br/>

Nano:

<br/>

![image](https://github.com/user-attachments/assets/46d07636-f783-47b5-b378-6003d0095116)

<br/>
<br/>

Strings:

<br/>

![image](https://github.com/user-attachments/assets/62f539f0-b246-4636-96a2-0536e892d69d)

Stringseistä en löytänyt mitään huomiota herättävää.

<br/>
<br/>

upx:

<br/>

![image](https://github.com/user-attachments/assets/41b96f4b-1efe-4fad-a5b6-36828f192924)

<br/>
<br/>

Ghidra :

<br/>

![image](https://github.com/user-attachments/assets/fc8c9ac1-ad84-4c28-961e-5f1f44593936)

Ghidralla ei voi kuvaa tarkastella sillä ghidra ymmärtää lähinnä koodikieltä.

<br/>
<br/>

Mikään näistä ei paljastanut mitään kiinnostavaa mutta auttoi rajaamaan ratkaisuja.

<br/>
<br/>
<br/>
<br/>

# b) Tutki tiedostoa h1.jpg binwalk:lla. Mitä tietoja löydät nyt tiedostosta?

<br/>

Asensin binwalkin:

<br/>

![image](https://github.com/user-attachments/assets/2aeb72ff-4c09-49cf-86f9-98157779c693)

<br/>

Katsoin alkutietoja kuvasta:

<br/>

![image](https://github.com/user-attachments/assets/dc84d8db-73e2-45c4-8ed5-ca9b82df4c18)

<br/>

Ajoin komennon "binwalk -e h1.jpg" jotta saisin haettua kuvaan piilotetut tiedostot ja siirryin sen hakemistoon: (huom, koneellani kyseinen kuva on nimellä h24.jpg)

<br/>

![image](https://github.com/user-attachments/assets/7c4d54b3-9bf5-4ce7-8218-9bd31da6a46d)

<br/>

Kyseisellä tiedostolla ei ole mitään erityistä sisältöä enkä löytänyt mitään mikä viittaisi lippuun. Olettaisin että sellaista ei ole, sillä sitä ei mainita tehtävänannossa.

Varmistin vielä kuitenkin ettei tiedostossa ole mitään muuta piilotettua käyttämällä työkalua nimeltä "exiftool"

<br/>

![image](https://github.com/user-attachments/assets/47457d7f-72a1-4b8b-8c4b-bbcc75d514ea)

<br/>

Tällä työkalulla voi paljastaa esimerkiksi kuvaan liitettyjä kommentteja tagejä jne. Jos kiinnostaa niin kannattaa käydä katsomassa kyseinen työkalu (linkki)[https://exiftool.org/install.html]

<br/>
<br/>
<br/>
<br/>


# c) FOSS (Free Android OpenSource). Tutustu Android-sovelluksiin Offan (2024) listalta: Android FOSS. Valitse listalla itsellesi mielenkiintoisin applikaatio ja mene sen GitHubiin. Lataa ohjelman APK itsellesi ja käytä seuraavia työkaluja tutustuaksesi, miten APK:n voi avata.

<br/>

Valitsin kalenterisovelluksen nimeltä "(Birday)[https://github.com/m-i-n-a-r/birday]" 

Latasin sen apk:n
![image](https://github.com/user-attachments/assets/6b049334-f5c6-4c3f-8cf1-22b2bd61098a)
![image](https://github.com/user-attachments/assets/f3d8b8d9-95ee-4e10-bf00-40cc847ef11c)

Kokeillaan avata apk:sta esim tärkeä Androidmanifest tiedosto:
![image](https://github.com/user-attachments/assets/b7ac15d7-9949-4c5f-b1f7-de3268423227)

apk-muodossa meille ei ole oikeutta tarkastella paketin tiedostoja
![image](https://github.com/user-attachments/assets/5d584c48-fee6-4df3-b899-3bb278fd7402)

Sitten vaan ratkaisemaan!


## Zip:

Nimetään .apk .zip:ksi ja hups, saman manifestin voi avata.

![image](https://github.com/user-attachments/assets/72d5c4fa-a763-4425-8af1-185870ba1a8e)

![image](https://github.com/user-attachments/assets/67f3f4c3-c53c-46d5-af74-b9174cc3a15a)

Unzippauksen jälkeen tiedoston voi avata normaalisti:
![image](https://github.com/user-attachments/assets/81a9bebd-3617-4bb9-9d6f-3bef1f26ad71)

## JADX:

Onnistunut asennus: 
![image](https://github.com/user-attachments/assets/6b842f85-6fe4-440b-88bc-8ab2e12af76a)

Avataan apk jadx-guilla:
![image](https://github.com/user-attachments/assets/8d6bb0df-13f1-4a38-85ec-990ca234acd4)

Ja tarkastellaan taas avattua manifestia:
![image](https://github.com/user-attachments/assets/a4c8c12a-ff8a-4f57-a7cf-8add5fdb1f36)
























Lähde

https://linuxcommandlibrary.com/man/binwalk
