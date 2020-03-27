# IOT: onderzoeksrapport NFC

![NFC](https://intel-tele.com/wp-content/uploads/2019/03/mify-o-nfc-1.jpg "NFC picture")

NFC of Near Field Communication is een technologie dat communicatie tussen twee apparaten toe laat zolang ze minder dan 4 cm van elkaar verwijderd zijn. De technologie werd voor het eerst gebruikt in star wars speelgoed van Hasbro, maar werd al snel een populaire feature in smartphones. Het maakt zelfs deel uit van mijn dagelijkse routine. Ik heb namelijk mijn alarm zo ingesteld dat het enkel uit te schakelen valt door een NFC-tag, die zich aan de andere kan van mijn kot bevindt, te scannen. In dit onderzoeksrapport gaan we meer te weten komen over wat NFC is, de geschiedenis ervan, hoe de het precies werkt en waarvoor de het gebruikt wordt.

# Wat is NFC?

Zoals eerder gezegd is NFC een manier om data over te brengen tussen twee objecten zonder dat er effectief contact vereist is. Er zijn twee soorten NFC communicatie. De eerste soort treedt op wanneer er sprake is van communicatie tussen een **reader/writer** en **NFC card emulator**. De card emulator is vaak een fysieke kaart of tag waar een NFC chip in zit. Deze verschilt van de reader/writer in het opzicht dat het geen data kan schrijven of uitlezen van een ander NFC apparaat. Uiteraard kan een reader/writer dit wel. Deze wordt dus gebruikt om informatie uit te lezen of weg te schrijven naar een NFC card emulator. De NFC card emulator is een passief NFC component terwijl de reader/writer actief is. Een voorbeeld van dit type NFC interactie heb ik al eerder gegeven. Wanneer mijn alarm afgaat scan ik met mijn gsm een NFC tag om mijn alarm af te zetten. Hier fungeert mijn gsm als een reader die de tag uitleest en vervolgens, indien ik de juist tag heb ingelezen, mijn alarm uitschakelt. De gsm is de actieve component en de tag is de passieve. Er zijn vijf soorten NFC tags

- **Type 1 tag**

Dit zijn goedkope tags met een vaste opslagcapaciteit: 454 bytes. Deze tag kan zowel worden uitgelezen als herschreven worden.

- **Type 2 tag**

Deze tag bevindt zich ook in de lagere kostklasse, maar is beschikbaar met hogere opslagcapaciteit: 50 / 888 / 1904. Daarnaast kunnen ze ingesteld worden zodat ze enkel uitgelezen en dus niet meer overschreven kunnen worden. Dit noemt men ook wel read-only chips.

- **Type 3 tag**

Dit zijn de duurdere versies. Ze hebben een opslagcapaciteit van 1 / 4 / 9 Kbytes. Ook deze kunnen read-only gemaakt worden.

- **Type 4 tag**

Deze tags bevinden zich in de midden- tot hoge prijsklasse. Ze kunnen een opslagcapaciteit tot wel 106 Kbytes aan en kunnen net zoals de vorige twee types ook read-only gemaakt worden.

- **Type 5 tag**

Deze tag heeft een lagere opslagcapaciteit dan alle andere met maximaal 256 Kbytes. De prijsklasse in laag tot midden klasse. Deze tags kunnen niet read-only gemaakt worden.

De tags die het vaakst worden gebruikt voor onprofessionele doel einden, zoals bij makers, is de MIFARE ultralight. Dit is een type twee tag zonder beveiliging. Daarom is deze zo goedkoop.

De tweede is de **peer-to-peer** communicatie en is specifiek voor wanneer twee objecten met een NFC chip data kunnen overbrengen in beide richtingen. Hierbij kunnen dus beide objecten data lezen en wegschrijven van elkaar. Dit wil zeggen dat bij peer-to-peer NFC beide objecten zich kunnen voordoen als zowel actief en passief. Een voorbeeld hiervan is het doorsturen van een foto of bestand via de NFC functie van je telefoon. Ik ben in staat om een foto te sturen (writing), maar ook om een te ontvangen (als een tag).

# Geschiedenis van NFC

Het eerste patent dat betrekking heeft tot de NFC technologie werd vastgelegd in 1997 door Andrew White en Marc Borret. De technologie werd toen in de praktijk gebruikt in star wars speelgoed van Hasbro. In 2002 werd NFC goedgekeurd als een standaard door twee belangrijke standaardisatie organisaties: ISO en IEC. Later keurde ook de organisatie ECMA deze standaard goed. Later, in 2002 werd het NFC Forum gecreëerd door Philips en Nokia. Dit is de gemeenschap die beslissingen maakt over het gebruik en de toekomst van deze technologie. Vervolgens werd in 2005 de eerste NFC feature in een telefoon geïntroduceerd. Dit in de vorm van een add-on voor de Nokia 5140 en Nokia 3220. In 2006 werd het idee van NFC tags ingevoerd. De eerste android telefoon met de NFC feature werd gereleased in 2010 en was de Samsung Nexus S. In 2011 werd de NFC technologie voor het eerst gebruikt in de PayPass service van Mastercard. Sindsdien kent NFC steeds meer toepassingen zoals de smartposter, waar informatie uit de poster kan uitgelezen worden door de telefoon, als onderdeel van een twee-staps-verificatie systeem en Android Pay van google. Tegenwoordig kunnen we allemaal contactloos betalen met de kaart of smartphone.

# Hoe werkt NFC?

Aangezien de werking van NFC gebaseerd is op elektromagnetische inductie zullen we dit eerst verder uitleggen. Het woord elektromagnetisch bevat twee delen: elektro van elektriciteit en magnetisch van magnetisme. Deze twee zijn dan ook onvoorwaardelijk met elkaar gepaard. Stel we hebben een koperen spoel, zoals links op de onderstaande afbeelding.

![Elektromagnetisch_Inductie](https://cdn57.androidauthority.net/wp-content/uploads/2013/04/magnetic-fields.png "Elektromagnetisch inductie")

 

Wanneer we een potentiaalverschil op de spoel zetten ontstaat er een stroom doorheen de draad. Door het verband tussen elektriciteit en magnetisme resulteert dit in een magnetisch veld dat rond de spoel ontstaat zoals te zien is in de linkse spoel op de afbeelding.

Deze werking is ook van toepassing in de omgekeerde richting. Het plaatsen van een geleider binnen een magnetisch veld zal een stroom opwekken binnen in deze geleider.

De reden van het verband tussen elektriciteit en magnetisme komt door de werking van beide verschijnselen. Dit is namelijk het aantrekken van elektronen door een positieve lading (protonen). Magnetisme is het herstructureren van de positie van elektronen en protonen binnenin magnetisch materiaal. De twee verschijnselen spelen dus als het ware elk met hetzelfde speelgoed. Logisch dus dat ze elkaar beïnvloeden.

Een NFC chip heeft altijd een antenne. Deze is een mini spoel, die dus dezelfde eigenschappen als de grote hierboven heeft. Een actieven NFC component zal een stroom door de spoel sturen waardoor een magnetisch veld ontstaat. Wanneer een passieve component in dit veld terecht komt, zal door de magnetische kracht in de antenne een stroom opgewekt worden. Deze stroom wordt dan vervolgens gebruikt als de energie bron om een vanuit de passieve NFC component de data via binaire, elektrische impulsen door te sturen naar zijn antenne. Door de elektromagnetische inductie worden deze impulsen weer omgezet naar een magnetisch veld dat een stroom veroorzaakt in de antenne van de actieve component. Deze component krijgt dus binaire data binnen door het alterneren van het magnetisch veld. Op deze manier wordt data overgebracht tussen een passieve en een actieve NFC component. Een belangrijk opmerking is dat een passieve component dus geen energiebron nodig heeft, vandaar de naam. Het gebruikt de impulsen van de actieve component, die dus wel een energiebron heeft, om zijn eigen data door te sturen.

NFC wordt beschouwd als een sub technologie van RFID of Radio Frequency Identification. Maar in deze uitleg werd niets gezegd over radio golven? Wel, een ander woord voor radiogolven is elektromagnetisch golven. Doordat er bij NFC stroom impulsen door de antennes wordt gestuurd is het resulterend magnetisch veld dus ook alternerend; het wordt soms sterker en soms zwakker. Dit is dus per definitie een golf, meer bepaald een elektromagnetische golf of een radiogolf. NFC werkt op een frequentie van 13.56Mhz. Dit wil zeggen dat er 13 560 000 keer per seconde een nieuwe puls wordt uitgezonden.

Nu we weten hoe twee componenten contact leggen, moeten we nog te weten komen hoe ze dan effectief data overbrengen. Dit wordt gedaan aan de hand van binaire waarden: 0 of 1. Elke impuls is ofwel een 0 of een 1. De passieve component geeft de waarde van deze bit met het signaal mee door voor respectievelijk een lage of een hoge stroom door de antenne te sturen. Dit resulteert dan in een sterkere of zwakker magnetische veldsterkte van het magnetisch veld, wat dan op zijn beurt een sterkere of zwakkere stroom veroorzaakt in de antenne van de actieve component.

# Toepassingen

![NFC_Toepassingen](https://www.inktweb.nl/blog/wp-content/uploads/what-is-nfc.jpg "Toepassingen van NFC")

NFC wordt vandaag de dag vaak gebruikt bij het contactloos betalen. Dit zowel met de smartphone als via een NFC chip in de bankkaarten. Daarnaast is het ook terug te vinden in toegangs- en personeelsbadges, tickets en zelfs business kaartjes. De mogelijkheden van NFC zijn verrijkend. Het biedt een creatieve manier om de ooit statische media nu interactief te maken, zoals het geval bij de smartposter.

# Bronnen

[https://en.wikipedia.org/wiki/Near-field\_communication](https://en.wikipedia.org/wiki/Near-field_communication)

[https://www.dummies.com/consumer-electronics/5-nfc-tag-types/](https://www.dummies.com/consumer-electronics/5-nfc-tag-types/)

[https://www.quora.com/Can-all-NFC-tags-be-made-read-only-how-is-this-done](https://www.quora.com/Can-all-NFC-tags-be-made-read-only-how-is-this-done)

[https://nl.wikipedia.org/wiki/MIFARE](https://nl.wikipedia.org/wiki/MIFARE)

[https://www.androidauthority.com/what-is-nfc-270730/](https://www.androidauthority.com/what-is-nfc-270730/)

https://www.quora.com/How-does-NFC-work
