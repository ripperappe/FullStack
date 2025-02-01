# FullStack -harjoitustyö

Tässä dokumentissa toimintaa selittävä kaavio, asennuksia ja ohjelmaa siihen asti, kun selaimelle tulostetaan ohjelmassa annetusta kansioista kaikki tagit, niiden nimet ja tilat. Tässä vaiheessa selaimelta annettavat parametrit eivät toimi eikä tageilla ei ole tapahtumakuuntelijoita. Ohjelman commit gitissä "Perustoiminnot OK"
## Diagram
![diagram](kuvat/diagram.PNG)

## Asennus
Aloitetaan tekeminen palvelimen päästä, asennetaan node.js (jos ei vielä asennettu)

Mennään kansioon, johon halutaan node.js pyörimään

> npm init -y


![kansiot](kuvat/kansiot.PNG)

Asennetaan express (node.js toimii "sulavammin ja helpommin", CRUD!!)

> npm install express


![express](kuvat/express.PNG)

## Ohjelma

Tuodaan modulit ja määritellään asetuksia...

![koodi1](kuvat/koodi1.PNG)

Configuroidaan OPC UA -client ja muodostetaan yhteys palvelimelle

![koodi3](kuvat/koodi3.PNG)

Käsitellään selaimelta tuleva pyyntö

![koodi4](kuvat/koodi4.PNG)

Selaimelle lähetettävä teksti siivotaan ylimääräisistä

![koodi5](kuvat/koodi5.PNG)

OPC UA -serveriltä haetaan tietoja browseTags- ja browseSubsequentLevel -funktioilla.

![koodi6](kuvat/koodi6.PNG)

