# Använda JuezLTI i Moodle

![Juez i LMS](../docs/img/gettingCredentials/juezLTI_UsingCredentialsInLMS.png)

Från Moodle 2.2 och framåt kan **Externt verktyg** göra att användare kan interagera med LTI-kompatibla lärresurser och aktiviteter på andra webbplatser. Då är valet **Externt verktyg** det rätta sättet att använda JuezLTI från Moodle.

Det finns en sammanfattning av dokumentationen för [Externt verktyg](https://docs.moodle.org/400/en/External_tool) på Moodles officiella webbplats.

Beroende på dina privilegier på din institutions Moodle-webbplats kommer du att kunna konfigurera LTI-verktyget på aktivitetsnivå eller på webbplatsadministrationsnivå.

## Aktivitetsnivå

När du har valt **externt verktygs** ![](../docs/img/gettingCredentials/externalTool2.png) eller ![](../docs/img/gettingCredentials/externalTool.png) måste du fylla i formuläret:

- **Aktivitetsnamn** - lägg till en titel, beskrivning vid behov, med ditt val av visning.
- **Förkonfigurerat verktyg** - det här är hur Moodle kommunicerar med verktygsleverantören. Om du är osäker, lämna som standard. Om din administratör har gjort ett verktyg tillgängligt på hela webbplatsen, kommer du att kunna välja det här:![Preconfiguredtool.png](https://docs.moodle.org/400/en/images_en/7/7c/Preconfiguredtool. png)

- **Verktygs-URL** - Detta är URL:en för att ansluta till webbplatsen. Om din moodle-webbplats använder [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) (använder sig av [HTTPS](https://docs.moodle.org/400/en/HTTPS)) kommer du bara att kunna använda ett verktyg som också använder [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security). Se till att verktygets URL har [HTTPS](https://docs.moodle.org/400/en/HTTPS) innan du försöker använda det, annars kan du få en tom sida.

    I betaversionen av JuezLTI måste webbadressen fyllas med [https://beta.juezlti.eu/tsugi/mod/codetest/](https://beta.juezlti.eu/tsugi/mod/codetest/). _Glöm inte att avsluta med "/"_.

- **Öppna container** - det här är hur det externa verktyget kommer att visas.
    - Standard - om du är osäker; lämna som standard
    - Bädda in - det externa verktyget kommer att bäddas in i Moodles kurssida med block och navigeringsfält
    - Bädda in utan block - det externa verktyget kommer att bäddas in på Moodle-kurssidan men utan block
    - Nytt fönster - det externa verktyget öppnas i ett nytt fönster. (Ett nytt fönster eller flik öppnas med det externa verktyget och det gamla webbläsarfönstret som innehåller kurssidan kommer inte att ändras.)

_Följande inställningar är tillgängliga genom att klicka på "Visa mer":_
- **Aktivitetsbeskrivning** - ge en kort beskrivning här
- **Visa beskrivning på kurssidan** - välj att visa beskrivningen tillsammans med aktivitetens namn
- **Visa aktivitetens namn när den startas** - visas när studenten klickar på länken.
- **Visa aktivitetsbeskrivning när den startas** - visas när studenten klickar på länken.
- **Secure tool URL** - Detta åsidosätter verktygets URL när Moodle använder [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) (om din webbplats är konfigurerad att använda [HTTPS](https:/ /docs.moodle.org/400/en/HTTPS))
- **<u>Konsumentnyckel</u>** - här måste du klistra in [**nyckeln** från JuezLTI](hamtaAutentisering.md).
- **<u>Delad hemlighet</u>** - och här, **hemligheten**.
- **Anpassade parametrar** - normalt kan du lämna detta tomt. Verktygsleverantören kan använda detta för att låta dig visa en specifik resurs.
- **URL ikon** - du kan visa en annan ikon än standardikonen för det externa verktyget genom att ange dess URL här
- **Secure Icon URL** - ange webbadressen till en annan ikon här om dina studenter använder Moodle säkert via [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security).

## Integritet

- **Dela startprogrammets namn med verktyget** - detta betyder att studentens namn kommer att visas på den anslutna webbplatsen [som i det här exemplet](https://docs.moodle.org/400/en/images_en/1/ 13/demoexternaltool.png)
- **Dela startprogrammets e-post med verktyget** - detta betyder att elevens e-post kommer att visas på den anslutna webbplatsen [som i detta exempel](https://docs.moodle.org/400/en/images_en/2/ 27/externaltoolfrontpage.png)
- **Acceptera betyg från verktyget** - om detta är markerat kommer den anslutande sidan att skicka tillbaka betyg till Moodles betygsbok. Se [Använda externt verktyg](https://docs.moodle.org/400/en/Using_External_tool) för mer information om detta.

## Inställningar för webbplatsadministration

### Lägga till ett verktyg för hela webbplatsen

En administratör kan manuellt konfigurera externa verktyg i _Webbplatsadministration > Plugins > Aktivitetsmoduler > Externt verktyg > Hantera verktyg_ så att de är tillgängliga på hela webbplatsen.

![Lägga till ett externt verktyg](https://docs.moodle.org/400/en/images_en/thumb/e/e2/moodle310_external_tool_registration.png/450px-moodle310_external_tool_registration.png)

Ett verktyg kan konfigureras av en administratör så att det visas i aktivitetsväljaren (utöver den externa verktygsaktiviteten) så att en lärare kan välja att lägga till i en kurs. Dess beskrivning, om en sådan finns, visas i aktivitetsväljaren.

### Visa mer information

På sidan _"Hantera verktyg"_  kan du också besöka _"Hantera förkonfigurerade verktyg"_ för att se de förkonfigurerade verktygen i ett tabellformat.

Det finns flikar för att lägga till ett externt verktyg, för att se de som väntar och för att se de som har avvisats:
![Konfigurera ett nytt externt verktyg](https://docs.moodle.org/400/en/images_en/thumb/4/43/LTItype.png/450px-LTItype.png)

Du kan också besöka _"Hantera externa verktygsregistreringar"_ för att se verktygsregistreringarna i tabellformat eller för att lägga till en extern registrering med begränsad kapacitet.

För att lägga till ett verktyg med begränsad kapacitet.
1. Klicka på "Konfigurera en ny extern verktygsregistrering"

![Registrera ett externt verktyg](https://docs.moodle.org/400/en/images_en/thumb/d/d9/LTIreg.png/450px-LTIreg.png)

2. Konfigurera detaljerna på inställningssidan:

![Sidan för registreringsinställningar](https://docs.moodle.org/400/en/images_en/thumb/8/8f/LTIregdetails1.png/450px-LTIregdetails1.png)

_'Medlemskap'_, låter det externa verktyget begära en lista över användare med en viss roll i ett specifikt sammanhang t.ex. användare som är anmälda till en kurs.

3. Klicka på bocken för att registrera:

![Aktivera](https://docs.moodle.org/400/en/images_en/thumb/3/3a/ticktoreg.png/450px-ticktoreg.png)

4. När du har fått ett meddelande om att registreringen fungerat klickar du för att slutföra processen:

![Slutför registreringen](https://docs.moodle.org/400/en/images_en/thumb/0/05/reqmet.png/300px-reqmet.png)

5. Om alla krav är uppfyllda kommer du att kunna registrera dig automatiskt.

6. Gå nu till _Webbplatsadministration > Plugins > Aktivitetsmoduler > Externt verktyg > Hantera externa verktygstyper_ och klicka på fliken "Väntande"

7. Klicka på bocken för att aktivera den:

![Aktiverar från fliken Väntar](https://docs.moodle.org/400/en/images_en/thumb/6/68/pendingactivate.png/450px-pendingactivate.png)

Se screencasten [Extern verktygsregistrering](http://www.spvsoftwareproducts.com/temp/lti2-moodle/) för en demonstration av stegen ovan.