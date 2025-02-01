# FullStack -harjoitustyö
Tässä dokumentissa näytetään, miten lisätään palvelimelle lähetettäviä tietoja ja päivitetään sivun tietoja automaattisesti.

## Selaimelta annettavien tietojen vienti palvelimelle
### Frontend
Selaimella on nyt yksi syöttökenttä ja yksi painike.

![selain1](kuvat/selain1.PNG)

Lisätään toinen painike ja muutetaan tekstit

![selain2](kuvat/selain2.PNG)

Lisätään toinen tapahtumakuuntellija

![selain3](kuvat/selain3.PNG)

### Backend

Tehdään palvelimelle vasatavat temput

Ensin lähdöille oma käsittely

![selain4](kuvat/selain4.PNG)

Muokataan browseTags-funtioita, jotta voidaan välittää selaimelta tulevat tiedot

![server1](kuvat/server1.PNG)

Muodostetaan oikeanmuotoinen string >>nodename>> 

![server2](kuvat/server2.PNG)

Tuodaan OPC UA -osoite. Vaatii bodyParserin.

![server3](kuvat/server3.PNG)

Nyt haku saa selaimelta tulevan osoitteen

![server4](kuvat/server4.PNG)

## Tilojen seuranta

Haluttujen tagien tiloja halutaan seurata, joten niille tiloille pitää muodostaa funktio, joka hakee niiden tiedot sekunnin välein.

Muokataan ensin niin, että jos tila on True, silloin tausta menee vihreäksi.

![selain5](kuvat/selain5.PNG)

![selain6](kuvat/selain6.PNG)

Jolloin selaimessa True-tilat erottaa helposti

![selain7](kuvat/selain7.PNG)

Aloitetaan pollaus, kun tilat on haettu ensimmäisen kerran

![selain8](kuvat/selain8.PNG)

Tiedot haetaan samalla tavalla kuin painikkeella

![selain9](kuvat/selain9.PNG)

Serverin puolella on tallessa address ja kansio, mistä haetaan

![server5](kuvat/server5.PNG)

Varmaan voisi helpomminkin tehdä...