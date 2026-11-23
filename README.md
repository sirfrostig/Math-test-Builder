# Math test builder

*Gäller version 0.1.98.*

Ett program för att bygga matteprov med slumpade tal, skriva ut ett eget prov till varje elev, skanna in
de ifyllda proven med kameran, rätta dem på skärmen och ta fram resultat och rapporter. Allt ligger i
**en enda HTML-fil** som körs i webbläsaren, utan installation, konto eller server.

- Gränssnittet är på engelska. Utskriften (Namn, Klass, Sida, Svar) har svenska etiketter.
- Använd **Chrome eller Edge**. Spara i mappar (se nedan) kräver någon av dem.
- Filen heter `math-test-builder-vX.Y.Z.html`. Versionen står alltid i filnamnet och i programmets rubrik.

## Innehåll

1. [Komma igång](#komma-igång)
2. [Flikarna](#flikarna)
3. [Frågor](#frågor)
4. [Prov, utskrift och skanning](#prov-utskrift-och-skanning)
5. [Rättning och resultat](#rättning-och-resultat)
6. [Frågebanker](#frågebanker)
7. [Spara, dela och dataskydd](#spara-dela-och-dataskydd)
8. [Tips](#tips)
9. [Om något inte fungerar](#om-något-inte-fungerar)

## Komma igång

1. Öppna `math-test-builder-v0.1.98.html` i Chrome eller Edge (dubbelklicka på filen).
2. **Questions**: skapa en fråga (**+ New question**) eller hämta färdiga från en frågebank (se
   [Frågebanker](#frågebanker)).
3. **Tests**: välj frågor och spara ett prov.
4. **Classes**: lägg in en klass med elever.
5. **Assign and print**: tilldela provet till klassen och skriv ut ett prov per elev.
6. **Scan**: skanna de ifyllda proven med kameran.
7. **Answers** och **Results**: rätta och se resultaten.

Allt sparas automatiskt i webbläsarens lagring. Vill du spara i riktiga mappar eller dela med andra, se
[Spara, dela och dataskydd](#spara-dela-och-dataskydd).

## Flikarna

| Flik | Vad den gör |
|---|---|
| **Questions** | Frågebanken: skapa, redigera, filtrera, exportera och importera frågor. Visar också frågor från externa banker. |
| **Tests** | Bygg och spara prov: delar, antal uppgifter, variantgrupper, skrivytor, rubrik och avslutande text, beskrivning. |
| **Classes** | Klasser och elever (valfritt två e-postadresser per elev), och vilka prov klassen har fått. |
| **Assign and print** | Tilldela ett prov till en klass, välj utskriftsalternativ, förhandsgranska och skriv ut. |
| **Scan** | Läs in utskrivna prov med kameran. |
| **Answers** | Rätta: en elev, alla elever, eller fråga för fråga. |
| **Results** | Tabell, statistik, betyg, Excel och PDF-rapporter. |
| **Import** | Läs in frågor från Word-dokument (`.docx`), även ekvationer. |

Överst finns raden för **mappar och frågebanker**.

## Frågor

I uppgiftsskaparen bygger du frågan av block som du drar in i frågan.

- **Slumpade tal**: heltal, mängder, faktorer, exkluderingar ("inte delbart med", "nära") och
  dubblettskydd, så att en elev inte får samma uppgift två gånger. Slumpen styrs av elevens *seed*,
  så samma elev får samma tal när provet skrivs ut igen.
- **Räkning**: bråk, blandad form, decimal, procent, tal till ord med böjningsformer, avrundning,
  vinklar och grader, komplexa tal, symbolisk räkning och `solve`, statistik, tabeller och diagram.
  Derivata och integral finns under verktygsområdet **Calculus**.
- **Figurer**: funktionsritare, koordinatsystem, geometrifigurer, cirklar, skärningspunkter, area
  under grafer, vektorer och mönster som upprepas. Bilder kan läggas in och placeras.
- **Delar (a, b, c ...)**: en fråga kan delas i deluppgifter med egna svar och poäng.
- **Fyrfältare (Four-field problem)**: ett problem som eleven löser på flera sätt i ett rutnät med fält.
  Standard är 4 fält i 2 × 2, men antalet är fritt. Varje fält har egen rubrik, kan vara rutat eller
  blankt, har egna poäng, egen skannad ruta och egen kommentar. Med **Fill the page** får frågan en egen
  sida där innehållet är vridet 90 grader så att fälten blir större. Skanningen vrider tillbaka.
- **Svarsrutor och skrivytor**: en liten ruta för bara svaret, eller en skrivyta (rutad) per uppgift.
- **Poäng**: **E**, **C** och **A** (nivåer), förmågor på poängen (B, P, PL, M, R, K) och **P**, en
  poäng utan nivå. En fråga utan poäng går inte att rätta, och programmet varnar för det i
  uppgiftsskaparen, i provbyggaren, när provet sparas, och vid utskrift och rättning. Knappen
  **Add ungraded points** ger en poäng åt de frågor som saknar poäng.
- **Ångra** med Ctrl+Z (Cmd+Z på Mac), upp till 200 steg.

## Prov, utskrift och skanning

- Ett prov består av **delar**. Varje del har egna frågor, rubrik och skrivytor. Du kan skriva en
  **beskrivning** av provet som visas vid namnet, och **Preview** visar provet med ett exempel på varje
  uppgift.
- Du kan slumpa uppgiftsordningen per elev, sprida uppgifterna över ett visst antal sidor, skriva ut
  bara vissa delar, visa poäng på utskriften, och lägga till en poängsummeringsruta och en betygsruta.
- **Show print preview** visar utskriften på skärmen innan du skriver ut.
- Varje sida kan få en **QR-kod** och tre svarta hörnrutor. De gör att **Scan** känner igen sidan,
  vet vilken elev den tillhör och kan klippa ut varje uppgift.
- **Scan**: håll sidan framför kameran (inbyggd eller webbkamera). Rutan **Mirror the camera image**
  spegelvänder bilden om kameran gör det.

## Rättning och resultat

- **Answers** visar elevens skannade svar bredvid facit och rättningsrutorna. Per poäng väljer du *ej
  bedömd*, *noll*, *halv* eller *hel* (halva poäng slår du på med **Allow half points**). Du kan skriva
  en kommentar per uppgift och en övergripande kommentar per elevprov.
- **Task / Wider / Whole page** växlar hur mycket av sidan du ser. **Hide names** döljer namnen och
  visar eleverna i slumpad ordning (Student 1, Student 2 ...).
- **Bedömda exempel**: vid varje utklipp finns **Save as example**. Det sparar elevsvaret som bild
  (utan namn) tillsammans med poängen, kommentaren, uppgiften och facit på frågan i frågebanken. Nästa
  gång du rättar samma fråga ser du exemplen under rättningsrutan (**Assessed examples**), som
  bedömda elevlösningar vid de nationella proven.
- **Review by another teacher**: exportera ett prov till en `.mtbr`-fil, låt en kollega rätta, och
  jämför bedömningarna.
- **Results**: tabell per elev och uppgift, statistik, betygsgränser, och kommentarer som röda
  trianglar. Du kan visa eller dölja kolumnerna E, C och A.
- **Exporter**: Excel (ett prov eller alla), och en **PDF-rapport per elev** med poäng, kommentarer och
  de skannade sidorna (facit kan tas med). **Export all reports (PDF, zip)** ger en mapp per klass med
  alla rapporter och en mottagarlista (`Recipients ... .xlsx`) med elevernas e-postadresser, så att du
  kan skicka ut rapporterna automatiskt, till exempel med Power Automate och Outlook.

## Frågebanker

En frågebank är en samling frågor och prov på en webbadress. Programmet hämtar dem och visar dem
tillsammans med dina egna frågor.

### Använda en bank

- Raden överst har **+ Add question bank**. Skriv adressen, ett namn (valfritt), ett kortnamn
  (valfritt), välj en färg och tryck **Add bank**.
- Programmet levereras med banken **Mattebanken** (`https://sirfrostig.github.io/mattebanken/`)
  ifylld.
- Varje bank syns som en markering i raden med färg, namn och en **kryssruta**: ikryssad tar du med
  bankens frågor och prov, avkryssad gör du det inte. **Question banks** fäller ihop hela raden.
  Klick på namnet öppnar bankens dialog (färg, kortnamn, **Fetch again**, **Access…**, **Remove bank**).
- Bankens frågor visas i frågelistan med bankens färg som kant och en **etikett med bankens kortnamn**
  (eller namn). Etiketten ersätter knappen **Edit**: frågorna går inte att ändra, men du kan titta på
  dem och göra en redigerbar kopia med **Copy**.
- **Lokal kopia**: första gången du använder en fråga (väljer den i provbyggaren, sparar ett prov med
  den eller bifogar ett bedömt exempel) sparas en kopia i webbläsaren, som en vanlig fråga. Etiketten
  blir då fylld (💾). Sparade kopior ändras aldrig av banken, så att sidan får försvinna. Sparade prov har
  alltid egna kopior av sina frågor. Vill du inte spara kopior av en banks frågor tar du bort
  kryssrutan **Save a copy of a question on this device when I use it** för den banken.
- Frågor du inte har använt sparas inte på enheten. Frågor du redan använt ligger kvar även om du
  kryssar ur banken.
- Har banken en nyare version av en sparad kopia visas **↻ newer in bank**.
- På **Tests** finns rutan **Use test from question bank** med bankernas färdiga prov. Tryck
  **Save to my tests** för att kunna använda ett prov, och **Preview** för att titta på det.
- Namn och beskrivning följer banken. Ändrar banken sitt namn byts det vid nästa hämtning, även på
  taggen. Ett namn du själv skrev ändras inte.

### Skapa en egen bank

Det enklaste är ett **publikt GitHub-repo**. Du behöver varken bygga något eller slå på GitHub Pages.

1. Skapa ett publikt repo och ladda upp filer i valfri mappstruktur: frågor exporterade med
   **Export selected questions** (`.mtbq`) och prov exporterade med **Export** vid provet (`.mtbt`).
2. Lägg in adressen i programmet: `https://github.com/ANVÄNDARE/REPO` eller
   `https://ANVÄNDARE.github.io/REPO/`.
3. Nya filer syns efter några minuter. Tryck **Fetch again** vid banken, eller ladda om sidan.

**Flera banker på samma adress**: varje mapp på översta nivån är en egen bank. Filerna i roten och i
mapparna `questions` och `tests` hör till huvudbanken. Mappar som börjar med punkt hoppas över. En fil
`bank.json` i mappen kan ge banken namn, kortnamn och beskrivning:

```json
{ "name": "Algebra", "short": "Alg", "description": "Ekvationer och funktioner" }
```

Nya mappar dyker upp som nya banker av sig själva, och du kan kryssa ur de du inte vill ha. En bank du
tagit bort kommer inte tillbaka.

**Andra webbplatser och privata repon**: använd en indexfil, `index.json`, som listar filerna
(`{"app": "mtb-bank-index", "v": 1, "banks": [{"id", "name", "short", "description", "files": [...]}]}`
eller, för en enda bank, `"files": [...]` överst). Skriptet `tools/make-index.mjs` i webbplatsmallen
skapar den med samma mappregler. Servern måste tillåta att andra webbplatser läser filerna (CORS).

**Lösenord och inloggning**
- Kräver adressen inloggning frågar programmet efter användarnamn och lösenord (eller bara en token) och
  skickar dem i rubriken `Authorization`. Det du skriver i fälten under **Needs a login or a
  password?** när du lägger till banken sparas på enheten tillsammans med banken, i klartext.
- **Krypterade banker**: programmet krypterar inte själv, det kan bara låsa upp. Bankens ägare
  krypterar filen med det fristående skriptet `mtb-encrypt-bank.mjs` (Node 18 eller nyare). Filen
  krypteras med AES-256-GCM, och flera lösenord kan öppna samma fil. Krypterade filer kan inte ligga
  inuti ett index.
- Krypterad fil är ett lås på dörren, inte ett kassaskåp: den som har lösenordet kan kopiera
  frågorna, och en nedladdad fil kan angripas offline, så använd långa lösenfraser.

## Spara, dela och dataskydd

- **Webbläsarens lagring** (localStorage) är arbetskopian: frågor, prov, klasser med elever och
  seeds, och inställningar. Rensar du webbläsarens data försvinner den, så exportera eller använd mappar.
- **Mappar** (Chrome och Edge): **Choose questions folder** och **Choose student folder** sparar
  frågor, prov och klasser som filer i mappar du väljer. **+ Add questions folder** lägger till fler
  frågemappar. Mapparna kan delas mellan kollegor. Frågor kan märkas så att de bara ligger i webbläsaren.
- **Export och import**: frågor (`.mtbq`), prov (`.mtbt`), hela samlingen (**Export questions, tests
  and classes**) och granskningar (`.mtbr`).
- **Elevuppgifter**: namn, klasser, e-postadresser och skannade sidor ligger på din dator, i
  webbläsaren eller i den mapp du valt. Var försiktig med hur du delar en elevmapp eller en
  PDF-rapport. Bedömda exempel sparas utan namn.

## Tips

- **Hovra** över en frågas namn en stund (i frågebanken eller provbyggaren) för att se en förhandsvisning
  med facit.
- **Checked**: kryssa de frågor du vill ha i frågebanken (rutan i början av varje fråga) och sätt
  filtret **Checked** i provbyggaren för att bara se dem. Det du kryssat sparas när sidan laddas om.
- **Taggar** syns inte på frågorna. De används för sökning och för filtret **Tag**.
- Alla knappar, fält och kryssrutor har en förklaring när du håller musen över dem.
- Fliken **Questions** går att fälla ihop med **Hide** för att spara plats.

## Om något inte fungerar

- **Röd ruta med feltext**: programmet visar fel i en ruta som går att kopiera. Skicka texten till den
  som underhåller programmet. Dubbelklicka för att dölja rutan.
- **Ingenting ritas**: använd Chrome eller Edge, och kontrollera att webbläsaren inte blockerar
  lagring för filer.
- **En bank visar ⚠**: håll musen över varningen eller öppna bankens dialog. Meddelandet säger om
  repot inte hittas eller är privat, om GitHubs gräns för antal anrop har nåtts, om
  `api.github.com` inte kan nås, eller om en inloggning eller ett lösenord behövs.
- **Provet går inte att rätta**: en eller flera frågor saknar poäng. Använd **Add ungraded points**
  eller sätt poäng i uppgiftsskaparen.
- **Skanningen hittar inte sidan**: kontrollera att QR-koden och de tre svarta hörnrutorna syns,
  att belysningen är jämn, och prova **Mirror the camera image**.

## Versionshistorik

Hela historiken, med alla ändringar och förklaringar, finns som kommentar överst i HTML-filen
(öppna filen i en textredigerare).
