# Hämta nycklar
För att säkra meddelandeinteraktioner mellan LMS och JuezLTI används OAuth-protokollet. OAuth-signering kräver en **nyckel** och delad **hemlighet** för att signera meddelanden. Nyckeln sänds med varje meddelande, såväl som en OAuth-genererad signatur som är baserad på nyckeln. JuezLTI letar upp hemligheten baserat på den tillhandahållna nyckeln och beräknar en egen signatur. Om den beräknade signaturen och den överförda jämförs för att verifiera avsändaren.

Proceduren för att få nyckeln och hemligheten inkluderar:
- [Hämta nycklar](#hamta-nycklar)
  - [JuezLTI-autentisering](#juezlti-autentisering)
  - [Begäran av nyckel/hemlighet](#begaran-av-nyckelhamlighet)
  - [Authorization by JuezLTI admin](#autentisering-av-juezlti-admin)
  - [Nyckel/hemlighet skickad](#nyckelhemlighet-skickad)

Dessa steg visas i bilden nedan:
![Hämta nycklar](../docs/img/gettingCredentials/juezLTI_gettingCredentials.jpg)

## JuezLTI-autentisering

JuezLTI använder [Tsugi](https://www.tsugi.org) för att hantera nyckel-/hemliga förfrågningar och Tsugi kräver autentisering med ditt Google-konto. Gå sedan till [JuezLTI Tsugi-sida](https://beta.juezlti.eu/tsugi/) och klicka på Logga in som bilderna nedan visar:
![Tsugi inloggning](../docs/img/gettingCredentials/loginTsugi.png)
![Välj Google-konto](../docs/img/gettingCredentials/googleLogin.png)

Det valda Google-kontot kommer att få nyckel-/hemlighetsuppgifterna.

Efter autentisering via Google kommer en profilsida att visas och du kommer att kunna välja dina profilinställningar och spara dem genom att klicka på knappen **Spara** eller **Spara profil**:
![Välj profilinställningar](../docs/img/gettingCredentials/profile.png)

## Begäran av nyckel/hemlighet

När du är autentiserad klickar du på Inställningar
![Åtkomst via inställningar](../docs/img/gettingCredentials/settings.png)

Om detta är din första begäran kommer du att se en (0) nära **Hantera LMS-åtkomstnycklar**. Klicka på **Hantera LMS-åtkomstnycklar**
![Hantera LMS-åtkomstnycklar](../docs/img/gettingCredentials/LMS_Access_keys_0.png)
Knappen LTI-nycklar markeras och meddelandet _"Du har inga IMS LTI-nycklar för detta system."_ visas under.

Klicka på knappen **Nyckelbegäran**
![Klicka på knappen Nyckelbegäran](../docs/img/gettingCredentials/keyRequestButton.png)

Och sedan, på **ny nyckelbegäran**
![Klicka på knappen Ny nyckelbegäran](../docs/img/gettingCredentials/newKeyRequest.png)

Fyll i formuläret och förklara varför eller var du ska använda nycklarna.
![Fyll i formuläret](../docs/img/gettingCredentials/explainWhy.png)

En ny nyckel med status (**Väntar**) har begärts.
![Nyckel väntar skapad](../docs/img/gettingCredentials/keyWaiting.png)

## Autentisering av JuezLTI admin

Ett e-postmeddelande skickas till personalen på JuezLTI och din nyckelbegäran kommer att godkännas så snart som möjligt. I det ögonblicket kommer du att få ett e-postmeddelande med bekräftelsen till ditt Google-konto.

## Nyckel/hemlighet skickad

När du får bekräftelsen på godkännande till din e-post kommer du att kunna logga in igen och den godkända nyckeln kommer att visas i avsnittet **LTI Keys**.
![Nyckel godkänd](../docs/img/gettingCredentials/keyApproved.png)