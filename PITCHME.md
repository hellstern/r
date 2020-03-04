---
@title[Introduktion]
@snap[east span-45 text-center text-blue]
Kom godt i gang med R programmering
@snapend
@snap[south-east span-50 text-orange text-center]
Tue Hellstern
@snapend

---?color=linear-gradient(100deg, white 50%, #567AD2 50%)
@title[Agenda]

@snap[west text-orange span-25 text-20]
  Agenda
@snapend

@snap[east span-60]
@ol[split-screen-list text-07](false)
- Kursus start	kl. 17.00
- Sandwichpause	kl. 18.15 – 18.45
- Kaffe/Te/Kage	kl. 19.45 – 20.00
- Spørgsmål	kl. 21:00
- Slut	kl. 21.30
@olend
@snapend

---?color=linear-gradient(100deg, #567AD2 50%, #567AD2 50%)
@snap[north-west span-30]
**RStudio**
@ol[split-screen-list text-05](false)
- Installation
- Introduktion til brugerfladen

@olend
**Syntaks**
@ol[split-screen-list text-05](false)
- Pakker
- Syntax
- Objekter
- Vektor
- Factor
- Data Frame
- Funktioner
- Manglende værdier
- Logiske operatorer
- Kommentarer
- Hjælp
@olend
@snapend

@snap[north-east span-60]
**Data**
@ol[split-screen-list text-05 text-left](false)
- Opret data
- Indlæs data
- CSV
- Excel
@olend

**Plot**
@ol[split-screen-list text-05 text-left](false)
- Oprettelse af plot
- Demo af forskellige muligheder
@olend

**Eksempler**
@ol[split-screen-list text-05 text-left](false)
- Du skal selv prøve
@olend
@snapend

---

Det er et introduktions seminar

Der vil være mange ”ting” vi **ikke** kan nå på 4 timer

Det er **ikke** et statistik kursus

---

@title[RStudio]
@snap[west span-40 text-07]
Du skal downloade R fra https://cran.r-project.org <br><br>Du skal her vælge den version, der passer til din computer – Linux, OS X (Mac) eller Windows.
@snapend

@snap[east span-60]
![](r/assets/img/rstudio.jpg)
@snapend

+++

@title[RStudio Genveje]
@snap[west span-50 text-13]
@ol[split-screen-list text-05 text-left](false)
- Tab = Liste over mulige kommandoer
- CTRL + Pil op = Auto Complete
- CTRL + Enter = Afvikler den linje kode
@olend
@snapend

@snap[east span-50]
![](r/assets/img/rstudio2.jpg)
@snapend

---

@title[Pakker]
@snap[north-west span-50 text-12]
**Installation af pakker**
@snapend

@snap[west span-50 text-05]
Du kan ”tilføje” funknationalitet til R ved at installere forskellige pakker. <br>
Du kan nederst til højre se, hvilke pakker du har installeret.
Det er også her muligt at opdatere de pakker, du har installeret.
Du kan finde en oversigt over de forskellige pakker her: https://cran.rstudio.com
@snapend

@snap[east span-50]
![](r/assets/img/pakker.jpg)
@snapend

+++

@title[Pakker CRAN]
@snap[north-west span-40 text-12]
**Installation af pakker**
@snapend

@snap[west span-60 text-07]
Du kan enten installere en pakke direkte fra CRAN<br><br>**The Comprehensive R Archive Network**<br><br>eller du kan installere fra en fil (zip, tar.gz).
@snapend

@snap[east span-50]
![](r/assets/img/pakkercran.jpg)
@snapend

+++

@title[Pakker Install]

@snap[north-west span-60]
Pakker
@snapend

@snap[west span-100]
```R
library()  # Pakker der er på din computer
search()   # Pakker der er aktive

## Install Pakker
? install.packages           # Hjælp

install.packages("tidyverse")  # Install
library("tidyverse")           # Load

update.packages("tidyverse")   # Update
remove.packages("tidyverse")   # Remove
```
@snapend

---

@title[R Syntax]

@snap[west span-35 text-07]
Som alle andre programmeringssprog har R nogle forskellige regler for, hvordan koden skal bygges op<br><br>Altså syntaksen for R
@snapend

@snap[east span-60 text-07]
”Navne” i R skal overholde nogle regler:
@ol[split-screen-list text-07 text-left](false)
- Bogstaver – a til z – store og små. *Nej til æøå*
- Tal
- Tegnene ”.” og ”_”. Altså ikke mellemrum eller bindestreg
- Et navn kan ikke starte med et Tal, men skal starte med et bogstav eller et gyldigt tegn
- R er case-sensitiv. Der er forskel på store og små bogstaver
@olend
@snapend

---

@title[Logiske operatorer]
@snap[west span-60 text-07]
**”Navne” i R skal overholde nogle regler:**<br><br>
@ol[split-screen-list text-07 text-left](false)
"=="  Lig med
"!="  Ikke lig med
"<"  Mindre end
">"  Større end
">="  Mindre end eller lig med
"<="  Større end eller lig med
@olend
@snapend

@snap[east span-35 text-07]
Meget af det du kommer til at arbejde med i R, vil kræve en eller anden form for logisk operator.<br>
Med en logisk operator finder du ud af om et udsagn er Sandt eller Falsk.
@snapend

---

@title[Datatyper]
@snap[west span-100 text-07]
**Du kan i R bruge følgende datatyper til dine objekter:**<br><br>
@ol[split-screen-list text-07 text-left](false)
- **logical** - boolean som kan være true eller false.
- **integer** - et heltal
- **double** - et decimaltal
- **character** - tekst
- **factor** - liste af foruddefinerede kategorier
- **vektor** - liste med elementer af den samme datatype
- **list** - liste med elementer af samme datatype og med et tilhørende navn til hvert element
- **dataframe** - tabel/datasæt med værdier
@olend
@snapend

---

@title[Objekter]
@snap[north-west span-40 text-12]
**Objekter**
@snapend

@snap[west span-65 text-07]
I det øverste højre hjørne af RStudio kan du se, hvilke objekter du har brugt og deres værdi.
Kommandoen **ls()** giver dig det samme resultat.
Når du ikke skal bruge et objekt mere, kan du slette de værdier, den indeholder.<br>
Det gør du med kommandoen **rm(objekt_navn)** f.eks. **rm(a)**
@snapend

@snap[east span-30]
![](r/assets/img/objekter.jpg)
@snapend

---

@title[Working Directory]

@snap[north-west span-60]
Working Directory
@snapend

@snap[west span-100]
```r
? getwd

getwd()

setwd("/home/tue/r_kursus")  # Linux/Mac
setwd("C:\\Users\\tuhe\\Documents\\r_kursus") # Windows
```
@snapend

---

@title[Help]

@snap[north-west span-40 text-12]
**Help**
@snapend

@snap[west span-60 text-07]
Du kan få hjælp direkte i R ved at bruge kommandoen **help()** hvor du i parentesen skriver den funktion, du gerne vil have hjælp til f.eks. **help(readxl)** for at få hjælp til "readxl unktionen"
Du kan også bruge kommandoen **? readxl**
@snapend

@snap[east span-30]
![](r/assets/img/help.jpg)
@snapend

---

@title[Import af data]

@snap[north-west span-40 text-12]
**Import af data**
@snapend

@snap[west span-60 text-07]
For at arbejde med data skal de importeres ind i R. Det er simpelt, hvis de filer der skal importeres ligger i R’s aktive bibliotek. Det er en god ide at organisere dine data inden de importeres, hvilket der findes mange gode værktøjer til.
Du kan i RStudio vælge mellem at bruge den grafiske brugerflade eller skrive den funktion, du vil bruge til importen.
@snapend

@snap[east span-30]
![](r/assets/img/import1.jpg)
@snapend

+++

@title[Import af data - Kommandoer]

@snap[west span-100 text-07]
**Standard funktioner til at læse indlæse data med:**<br><br>
@ol[split-screen-list text-07 text-left](false)
- read.table()
- scan()
- read.csv()
@olend
@snapend

@snap[east span-30]
![](r/assets/img/import1.jpg)

+++

@title[Tidyverse]

@snap[north-west span-40 text-12]
Pakken Tidyverse
@snapend

```r
# The easiest way to get readr is to install the whole tidyverse:
install.packages("tidyverse")

# Alternatively, install just readr:
install.packages("readr")

# Or the the development version from GitHub:
# install.packages("devtools")
devtools::install_github("tidyverse/readr")
```

---

@title[Plot standard]

+++

@title[Plot ggplot2]

@snap[north-west span-40 text-12]
Pakken ggplot2
@snapend

```r
# The easiest way to get ggplot2 is to install the whole tidyverse:
install.packages("tidyverse")

# Alternatively, install just ggplot2:
install.packages("ggplot2")

# Or the the development version from GitHub:
# install.packages("devtools")
devtools::install_github("tidyverse/ggplot2")
```