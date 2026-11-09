# Standardöversättningar för svenska openEHR-arketyper

Dessa tabeller återger projektets tillhandahållna standarder. "Standard" ska följas när termen har den angivna betydelsen; "Kontextberoende" kräver bedömning av användningen. Ofullständiga poster får inte behandlas som fastställda.

## Header: fasta formuleringar
| Engelska | Svenska | Regel |
|---|---|---|
| Purpose: To… | Att… | Inled med ”Att” + verb i infinitiv, t.ex. ”Att mäta…” |
| Use: Used to… | Används för att… | Inled vanligen så; använd passiv form enligt projektets anvisning där det passar |
| Misuse: Not to be used to… | Ska inte användas för att… | Standardinledning |
| Keywords | Nyckelord anpassade till svensk kontext | Får läggas till eller tas bort utifrån relevanta svenska söktermer |

## Data
| Engelska | Svenska | Anmärkning |
|---|---|---|
| Comment | Kommentar | Standard |
| Additional narrative about X, not captured in other fields. | Kommentarer avseende X som inte beskrivs i övriga datafält. | Anpassa X till sammanhanget |
| Multimedia representation | Multimediarepresentation | Standard |
| Clinical interpretation | Klinisk tolkning | Standard |

## State
| Engelska | Svenska | Anmärkning |
|---|---|---|
| Confounding factors | Möjliga felkällor | Kontextberoende; annan term kan vara lämpligare |
| Narrative description of any issues or factors that may impact on the measurement. | Beskrivning av faktorer och felkällor som kan påverka bedömningen av X. | Anpassa till ”mätningen” eller annan relevant aktivitet |
| Position | Kroppsställning | När kroppsställning avses |

## Protocol
| Engelska | Svenska | Anmärkning |
|---|---|---|
| Device | Utrustning | Standard i denna kontext |
| Extension | Tilläggsinformation | Inte ”Extrainformation” |
| Additional information required to capture local content or to align with other reference models/formalisms. | Plats för tilläggsinformation som krävs för lokala anpassningar eller anpassning till andra referensmodeller eller formella krav. | Standardbeskrivning |
| For example: local information requirements or additional metadata to align with FHIR or CIMI equivalents. | Exempelvis lokala informationskrav eller metadata för anpassning till FHIR. | CIMI utelämnas avsiktligt enligt projektets riktlinjer |

## Events
| Engelska | Svenska | Standardbeskrivning |
|---|---|---|
| Any event | Ospecificerad händelse | Ospecificerad standardhändelse vid en tidpunkt eller inom ett tidsintervall som explicit kan definieras i en template eller genereras automatiskt av vissa IT-system. |
| Any point in time event | Ospecificerad händelse vid specifik tidpunkt | Ospecificerad standardhändelse vid en tidpunkt som explicit kan definieras i en template eller genereras automatiskt av vissa IT-system. |

## Löptext
| Engelska | Svenska | Anmärkning |
|---|---|---|
| at runtime | kan genereras automatiskt av vissa IT-system | Anpassa grammatiskt till meningen |
| datetime; date/time | tidpunkt | I den avsedda betydelsen; bevara tekniska datatyper |
| clinician | vårdpersonal | Kontextberoende: ibland läkare |
| container | behållare | Standard i relevant kontext |
| to record | att registrera | Standard i relevant kontext |
| device | utrustning | Standard i relevant kontext |
| element; data element | datafält | Standard |
| explicitly | explicit | Anpassa grammatiskt |
| generic | generell | Anpassa grammatiskt |
| incidental | påverkande | Endast i kontexten påverkande faktorer |
| note | observera | När det används som uppmaning |
| over the age of X | X år eller äldre | Projektets föredragna uttryckssätt; KONTROLLERA att inklusiv gräns inte ändrar källans betydelse |
| under the age of X | X år eller yngre | Projektets föredragna uttryckssätt; KONTROLLERA att inklusiv gräns inte ändrar källans betydelse |
| range category | mätområde | Kontextberoende |
| template | template | Behåll engelska ordet, inte ”mall” |
| narrative description | beskrivning | ”Narrative” tillför normalt inget på svenska |
| individual; person; patient | individ; person; patient | Välj efter kontext, konsekvent inom arketypen |
| Coding of ... with a terminology is preferred, where possible. | Kodning av … till en terminologi är att föredra i de fall det är möjligt. | Standardformulering |

## Anatomi
| Engelska | Svenska | Anmärkning |
|---|---|---|
| Body structure | Kroppsstruktur | Standard |
| Body site | Kroppslokalisation | Standard |
| Body site name | Kroppslokalisation | Standard |
| Structured body site | Strukturerad kroppslokalisation | Standard |
| Structured target body site | Strukturerad avsedd kroppslokalisation | Standard |
| Target body site | Avsedd kroppslokalisation | Standard |
| Location of measurement | Mätställe | Standard |
| Structured location of measurement | Strukturerat mätställe | Standard |
| Source site | Provtagningslokalisation | Vid transplantat: ursprungslokalisation; vid hudtransplantat: tagställe |
| Structured source site | Strukturerad provtagningslokalisation | Standard |
| Specific source site | Preciserad kroppslokalisation | Standard |
| Body segment name | Kroppssegment | Standard |
| Alternative structure | Alternativ kroppsstruktur | Källistan anger ”Alternativ structure”; kontrollera engelsk originalterm |
| System or structure examined | Kroppsstruktur | Standard |

## Läkemedel
| Engelska | Svenska | Anmärkning |
|---|---|---|
| Medication | Läkemedel | Standard |
| Medication component | Innehållsämne | Standard |
| Prescription | Ordination | Källistan stavar ”Perscription”; verifiera originalterm |

## Poster som ännu saknar fastställd svensk översättning
- `has been deliberately left unconstrained to maximise re-use of this archetype`: saknar svensk standardöversättning i det tillhandahållna underlaget. Översätt efter kontext och flagga vid behov.

## Övriga bindande regler
- Arketypklassnamn (ACTION, CLUSTER, ADMIN, COMPOSITION, ENTRY, EVALUATION, INSTRUCTION, OBSERVATION, SLOT) översätts inte.
- Referenser till datafält i samma arketyp använder svenska fältnamn inom ”citattecken”.
- Referenser till andra arketyper i löptext skrivs exempelvis `CLUSTER.device (Medical device)`.
- Anpassa exempel till svenska förhållanden och sökord till svenska användares sökbeteende.
