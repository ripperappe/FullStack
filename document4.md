# FullStack-harjoitustyö

Tässä dokumentissa esitellään haettujen datojen päivitys. Tämän toimintaan saaminen vei aikaa kaikkein eniten, kokeilin SSE:tä ja etsin myös muita vaihtoehtoja. Tämä tuntuu vähän "purkkapaikalta", mutta toimii.

## Backend

browseTags-funktio saa parametreiksi nodeAddress:in ja modeGlabalin. Molempien muistipaikkojen tiedot on päivitetty silloin, kun selaimessa on painettu joko "Hae tulot"- tai "Hae lähdöt" -painiketta. Funktio palauttaa vain halutut osat selaimelle.

![server6](kuvat/server6.PNG)

## Frontend

Kun tiedot on haettu onnistuneesti, asetetaan muuttuja "munkki" = 1

![selain12](kuvat/selain12.PNG)

Voidaan aloittaa pollaus. Funktio startSimulation saa parametrinä joko fetchDataButtonInputs tai fetchDataButtonOutputs sen mukaan, kumpaa painiketta on painettu edellisen kerran

![selain13](kuvat/selain13.PNG)



startSimulationilla simuloidaan painikkeen painamista sekunnin intervallilla. buttonID-muuttujassa on siis nyt joko fetchDataButtonInputs tai fetchDataButtonOutputs. Tämä siis välitetään funktiolle simulateButtonClick. HUOMAA: clearInterval tarvitaan, ettei setInterval -oliota luoda loputtomasti. 

![selain14](kuvat/selain14.PNG)

simulateButtonClick nyt simuloi sekunnin välein painallusta ja tiedot päivittyvät oikein selaimelle.
![selain15](kuvat/selain15.PNG)


