connection.php = Fyll in databas anslutningen

Importera api_heaven.com.sql till phpmyadmin. Den �r direkt exporterad d�rifr�n.

I public_html/index.php s� kommer du �t api'n. Den fungerar s�h�r: ?champ=jinx t ex. Allts� index.php?champ=jinx

I edit har jag gjort ett mer anv�ndarv�nligt interface f�r API'n d�r man skriver in exempelvis "jinx" s� kommer informationen upp d�r med hj�lp av bilder.
Den inneh�ller �ven en login knapp som leder anv�ndaren till kontrollpanelen.


/public_html/edit/controlpanel/index.php
H�r �r kontrollpanelen. Den kr�ver att man m�ste logga in.

	email: cmeducations@cmeducations.se
	password: cmeducations

N�r man har loggat in i kontrollpanelen, har man d� till�telse att g�ra fler konton.

N�r man klickar p� antingen: Update, New champ eller delete s� laddar /scripts/style.js in de nya sidorna i en div med klass "edit".

Url till sidorna:
	
	/public_html/edit/controlpanel/modifydb/change.php - Update (READ, UPDATE)
	/public_html/edit/controlpanel/modifydb/add.php - New champ (READ, CREATE)
	/public_html/edit/controlpanel/modifydb/remove.php - Delete (READ, DELETE)
	/public_html/edit/controlpanel/auth/reg.php - Register (READ, CREATE)

	I varje fil ska det finnas kontroll s� att om det �r fel info som skickas mellan databasen och anv�ndaren s� sk det bli ett felmeddelande. 
	