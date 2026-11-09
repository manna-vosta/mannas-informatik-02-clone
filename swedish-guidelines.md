# Riktlinjer för svensk översättning av openEHR-arketyper

## Syfte och prioritering
Översättning är också kvalitetssäkring och lokalisering till svensk vårdkontext. Prioritera kliniskt korrekt, naturlig och tydlig svenska framför källspråkets meningsbyggnad. Det är tillåtet att omformulera meningar och stycken, men inte att ändra deras kliniska eller tekniska betydelse.

Socialstyrelsens *Språkliga riktlinjer för översättningen av Snomed CT till svenska* gäller som språklig grund, utom det SNOMED-specifika kapitel 1: https://www.socialstyrelsen.se/globalassets/sharepoint-dokument/artikelkatalog/klassifikationer-och-koder/2011-1-14.pdf

Följ i möjligaste mån etablerade svenska termer i SNOMED CT: https://browser.ihtsdotools.org/ . Kontrollera källan innan du hävdar att en term överensstämmer med SNOMED CT. Misstänkta brister i SNOMED CT-översättningar bör rapporteras till Socialstyrelsen.

## Språkregler
- Skriv kort, enkelt och rakt. Undvik onödiga nominaliseringar och mångordighet. Exempel: "Andningsfrekvensen är …" hellre än "Mätningen av andningsfrekvensen är …" när betydelsen är densamma.
- Undvik engelska förkortningar utom när de är väl etablerade i formell svensk medicinsk terminologi.
- Välj bestämd eller obestämd form efter sammanhang och var konsekvent inom arketypen, i möjligaste mån enligt SNOMED-riktlinjerna.
- Undvik snedstreck i löptext. Skriv "mindre än eller lika med", inte "mindre än/lika med".
- Undvik "och/eller": skriv "eller" för inkluderande disjunktion, och "antingen … eller …" när alternativen är ömsesidigt uteslutande.
- Använd svenska citattecken ”…” och citattecken kring namn på datafält som nämns i löptext.
- Använd kommatecken som decimaltecken i svensk text: 39,6, inte 39.6. Ändra aldrig numeriska data, maskinläsbara uttryck eller kodvärden för att uppnå detta.
- Använd semikolon med återhållsamhet enligt svenskt språkbruk.
- Följ SNOMED-riktlinjerna för enheter; bevara maskinläsbara enhetskoder.
- Översätt individual/person/patient utifrån sammanhang och var konsekvent inom arketypen.
- Anpassa exempel och nyckelord till svensk kontext. Lägg till relevanta svenska sökord och ta bort olämpliga originalnyckelord; ändra inte klinisk betydelse.

## Fält och referenser
- Arketypklassnamn och tekniska beteckningar såsom ACTION, CLUSTER, ADMIN, COMPOSITION, ENTRY, EVALUATION, INSTRUCTION, OBSERVATION och SLOT översätts inte. Formulera om meningen i stället för att böja klassnamnet.
- Vid referens till datafält inom samma arketyp, använd det svenska fältnamnet inom svenska citattecken: ”Klinisk tolkning”.
- Vid referens till en annan arketyp i löptext, använd arketyp-ID utan prefix och versionssuffix följt av arketypnamnet inom parentes, t.ex. `CLUSTER.device (Medical device)`. Bevara tekniska ID där de krävs maskinellt.
- Exempel på SLOT-formulering: "En eller flera instanser av denna arketyp kan nästlas i den SLOT för ”Undersökningsresultat” som finns i arketypen OBSERVATION.laboratory_test_result."
- Om en källhänvisning behöver läggas till under översättningsarbetet ska den markeras TYDLIGT MED VERSALER för kontroll före publicering, exempelvis "KÄLLA FRÅN ZZZ". Lägg inte automatiskt in sådana anteckningar i publicerad översättning.

## Brister i källtext
- Om originaltexten är tvetydig, markera detta för mänsklig granskning.
- Om originalet verkar felaktigt eller dåligt formulerat: rapportera till openEHR Sveriges förvaltning på contact@openehr.se. Föreslå en rimlig svensk formulering, men redovisa osäkerheten och ändra inte källspråk eller koder.
- Översätt inte okända termer med påhittade etablerade motsvarigheter. Flagga för granskning.

## Arbetsgång för AI-agent
1. Läs hela denna fil och `standard-translations.md` innan översättningen börjar.
2. Identifiera arketyp, version och kontext för varje fält.
3. Tillämpa standardöversättningar med rätt grad av bindning: fastställda respektive kontextberoende.
4. Kontrollera språk, konsekvens, referenser, exempel, nyckelord och all text i Purpose, Use, Misuse och arketypens fält.
5. Kontrollera att inga tekniska strukturer, begränsningar, koder eller andra språk har ändrats.
6. Redovisa osäkra termer, avvikelser och källtextproblem för mänsklig granskning.
