# Basreg-introduktion: använda BasregDWH

Det här repo:t innehåller en kort steg-för-steg-användarguide för att komma åt SLU:s Basreg-datalager (**basregDWH**) från **R / RStudio** med hjälp av `odbc`, `DBI`, `dplyr` och `dbplyr`.

**Målgrupp:** Forskare och medarbetare som är bekanta med programmering i stort, men som är nya inom R‑paket och hur man ansluter till en databa.

En maskinöversatt version på svenska finns i foldern /Swedish version och om du vill använda den så använder du markdown och projektfilen i denna. Själva koden och kodkommentarerna är på engelska men alla beskrivningar är på svenska. 

---

## Detta ingår

- `Basreg_introduction.Rproj` — RStudio-projektfil (rekommenderat sätt att öppna detta repo)
- `basreg_userguide.Rmd` — huvudhandledningen (kör koden steg för steg)
- `basreg_userguide.html` — en för-renderad HTML-version som kan läsas i webbläsare
- `basreg_userguide.pdf` — en PDF-version (A4, förkortad vid behov)

---

## Förkunskaper

1. **RStudio**  
   Officiell “kom igång”-guide: https://posit.co/resources/videos/getting-started-with-rstudio/

2. **Åtkomst till SLU Basreg / basregDWH**  
   För behörighet, kontakta **Eva Rundlöf**.

> Om du har en SLU-utgiven Windows-dator verifierar ODBC normalt din identitet automatiskt vid anslutning.  
> Användare på Linux och macOS behöver en separat ODBC-konfiguration.

Den här guiden hjälper dig att komma åt SLU Basreg-databasen (**basregDWH**) med R och RStudio.

Du kan använda vilken miljö du vill för att köra R-kod, men i den här användarguiden utgår vi från RStudio. Om du är obekant med RStudio beskriver Posit (som utvecklar RStudio) gränssnittet här:
https://docs.posit.co/ide/user/ide/guide/code/projects

Om du läser den här dokumentationen med avsikten att använda den för dataanalys, se till att du förstår hur R‑projekt fungerar:
https://docs.posit.co/ide/user/ide/guide/code/projects.html 

---

## Ladda ner detta repo

### Alternativ A: Klona med Git i RStudio (rekommenderas)

1. I RStudio: **File → New Project → Version Control → Git**
2. Klistra in repo-URL:en:
   https://github.com/TKlingstrom/Basreg_introduction
3. Välj en mapp och klicka på **Create Project**

### Alternativ B: Ladda ner som ZIP

1. Öppna repo:t i din webbläsare
2. Klicka **Code → Download ZIP**
3. Packa upp ZIP-filen
4. Öppna `Basreg_introduction.Rproj` i RStudio

---

## Var ska man börja

### Om du vill *köra handledningen*
1. Öppna `basreg_userguide.Rmd` i RStudio
2. Läs introduktionen och börja sedan vid **Steg 1** och kör varje kodchunk i ordning
   - I en R Markdown‑chunk: klicka på den gröna ▶‑knappen uppe till höger i chunken
   - Eller, om du använder ett R‑script: markera koden och tryck **Ctrl + Enter**

### Om du bara vill *läsa handledningen*
- Öppna `basreg_userguide.html` i din webbläsare (rekommenderas)
- Eller läs `basreg_userguide.pdf`

Du kan också kopiera varje kodavsnitt från HTML-dokumentet eller PDF:en till ditt eget R‑script och köra handledningen steg för steg.

---

## Noteringar

- Användare har **läsbehörighet**. Du kan titta på och ladda ner data, men du riskerar inte att ändra databasen. Du bör dock inte köra mycket stora och komplexa matchningsoperationer server-side för att skapa dataset, eftersom det kan påverka andra användare.
- Guiden sparar exempelutdata (CSV) i din aktuella arbetskatalog (`getwd()`).

---

## Författare

Tomas Klingström
