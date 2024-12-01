







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













Lähde

https://linuxcommandlibrary.com/man/binwalk
