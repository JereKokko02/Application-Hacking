













# x) Lue/katso/kuuntele ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva.)

1. Schneier 2015: Applied Cryptography, 20ed: https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec001
   
   - Teoriaa salakirjoituksesta, esimerkkejä, kuvaavia kuvia jne.
   - Code sanan historiaa sekä salauksen historiaa
   - Salausavaimien ero public ja private sekä niitä käyttämällä salaus
   - Esimerkkejä miten purkaa salauksia (Attack osiot)
   - XOR -operaattorin selitys
   - Large numbers = Esimerkkejä miten tieteellisesti kuvataan isoja numeroita ja miten niitä voi käyttää hyväkseen salauksessa

2. Karvinen 2024: https://terokarvinen.com/python-for-hackers/

   - REPL
   - Import base64
   - Pythonin toimintaa
   - loopit
   - Samoja asioita miten esimekiksi python perusteet kurssilla käydään (Ainakin syksyn 2024 toteutuksella)
   - Tässä siis kerrotaan miten teet toimivaa python koodia ja annetaan esimerkkejä eri tilanteista kuten looppien tekemisestä ja niiden rikkomisesta.

<br/>
<br/>
<br/>
<br/>

# a) 1. Convert hex to base64.

<br/>

![image](https://github.com/user-attachments/assets/45280b12-adc0-43cf-8cc4-0dd8ee0f6499)

<br/>

Ratkaisu: 

<br/>

![image](https://github.com/user-attachments/assets/77885e6b-f608-4bec-bd53-3f053dd1a87b)

<br/>

# b) 2. Fixed XOR.

![image](https://github.com/user-attachments/assets/da7df93b-4aad-477b-b1bf-43049bb41120)

<br/>

Ratkaisu:

<br/>

![image](https://github.com/user-attachments/assets/238ecb91-7076-40db-a077-abde6faa6746)

<br/>

# c) 3. Single-byte XOR cipher.

Tässä vaiheessa koodaaminen meni oman osaamisen yli ja päädyin käyttämään apuna chatgpt:tä. Yritin aluksi saada tehtävän ratkaistua vain kysymällä vinkkejä tekoälyltä mutta useamman päivän yrityksen jälkeen en vain saanut tehtävää ratkaistua. Tässä tehtävässä näytän siis miten gpt tehtävän ratkaisi.

Tässä näkyy antamani prompti:

<br/>

![image](https://github.com/user-attachments/assets/3042aa87-07c5-4a8d-9214-d3350e752611)

<br/>

Tässä on gpt:n tuottama koodi:

<br/>

![image](https://github.com/user-attachments/assets/6aa3521c-f6da-4e7f-998b-e6ccf9d1c4c2)

<br/>

Ja tässä on koodin tulostus:

<br/>

![image](https://github.com/user-attachments/assets/22a8db05-caa8-4358-99af-7ff75c26a798)

Ratkaiseva avain oli siis X

# 4. Detect single-character XOR.

Tätä tehtävää en valitettavasti saanut edes gpt:n avulla tehtyä. Nyt en valitettavasti pääse ilahduttamaan.



