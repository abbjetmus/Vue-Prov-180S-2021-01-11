# vue-prov-2021-01-11
Börja med att klona eller ladda ner projektet.
<br>
`git clone https://github.com/abbjetmus/Vue-Prov-180S-2021-01-11.git`
<br>
## Att tänka på

1. Använd back-ticks **\` \` (shift + `)** om du vill ha html över flera rader i en komponent.
```
var testcomponent = {
       template: `
           <div>
              <p></p>
           </div>
          `
       }
```
2.	Använd små bokstäver på komponent-namn och event/metoder.

## Fråga 1 - Interpolation

Skapa ett data objekt som heter **address** som innehåller variablerna/properties **gata**, **postnummer** och **stad**. Objektets variabler/properties ska innehålla värden på din egna post-address.<br>
Skriv sedan ut texten *Jag bor på Fregattvägen 7A, 749 48 Enköping* med hjälp av ditt address objekt.

### Resultat
**Jag bor på Fregattvägen 7A, 749 48 Enköping**<br><br>

## Fråga 2 - Loopa
1. Skapa en data variabel med namnet **cities** som är en **array [ ]** och innehåller tre objekt med städer:

```
{id: 1, name: 'Västerås', county: 'Västmanland'},
{id: 2, name: 'Karlstad', county: 'Värmland'},
{id: 3, name: 'Borlänge', county: 'Dalarna'}
```

2. Loopa sedan igenom arrayen med städer i en html lista där du skriver ut *namnet - bindestreck länet*,<br>
du väljer själv om du vill använda <**ul**> unorderd-list eller <**ol**> ordered-list.

### Resultat
* Västerås - Västmanland
* Karlstad - Värmland
* Borlänge - Dalarna

## Fråga 3 – Två-vägs-bindning
1. Skapa två inmatningsfält, en för förnamn och en för efternamn med hjälp av **input**-taggen.
2. Använd två-vägs-bindning för att binda inmatningsfälten till två data variabler.
3. Visa sedan resultatet som fullständigt namn med valfria taggar.

### Resultat
![Uppgift3](./assets/uppgift3.gif)

## Fråga 4 – Watch 
1. Skapa en data variabel med namnet **id**:
2. Skapa en Watcher som lyssnar på **id** variabeln.
2. Skapa ett inmatningsfält med **input**-taggen. 
3. Fältet ska kunna ta in en siffra och två-vägs-binda med hjälp av v-model till **id** variabeln.
5. Använd sedan följande *fetch*-anrop i din watcher för att hämta ner ett photo med hjälp av **id:t**, du måste alltså lägga till id:t i anropet t.ex. *'https://jsonplaceholder.typicode.com/photos/1'* där id = 1. Bra att kolla först att id har ett värde också.
```
fetch('https://jsonplaceholder.typicode.com/photos/')
  .then(response => response.json())
  .then(json => console.log(json))
```
2. Titta på datats typer i webbläsarens konsol.
3. Lagra sedan datat i en data variabel som heter **photo**.
4. Presentera **photo** i html:en med lämpliga taggar.

### Resultat
![Uppgift4](./assets/uppgift4.gif)

## Fråga 5 – Style bindning
Du har fått en div-tagg med en t-shirt som bakgrundsbild. Under den finns det 4 knappar **buttons**.<br>
Din uppgift är att byta färg på t-shirten till den färgen som står på knappen när man klickar på den.
Detta görs genom att byta bakgrundsfärg på div-taggen.
1. Skapa en data variabel som heter **color**.
2. När man klickar på en knapp ska color uppdateras till den färgen.
3. Använd style-binding på div-taggen så att den binder till color data-variabeln och sätter bakgrundsfärgen.

### Resultat
![Uppgift5](./assets/uppgift5.gif)

### Fråga 6 – Slots 
1. Skapa en komponent som heter **postcomponent**. 
2. **postcomponent** ska ha två namngivna slots med namnen "title" och "description".
**title** sloten ska vara en <**h1**> tagg och **description** sloten ska vara en <**p**> tagg.
3. Använd sedan **postcomponent** i '#app'-komponenten och skicka in två <**div**> taggar via slotsen med texten *"Det här är en titel"* och *"Det här är en beskrivningen"*.

### Resultat

# Det här är en titel<br><br>
Det här är en beskrivningen <br><br>


## Fråga 7 – Komponent kommunikation
1. Skapa en data variabel med namnet **cities** som är en **array [ ]** och innehåller fem objekt med städer:

```
{id: 1, name: 'Västerås', county: 'Västmanland'},
{id: 2, name: 'Karlstad', county: 'Värmland'},
{id: 3, name: 'Borlänge', county: 'Dalarna'},
{id: 4, name: 'Malmö', county: 'Skåne'},
{id: 5, name: 'Helsingborg', county: 'Skåne'},
{id: 6, name: 'Kiruna', county: 'Lappland'},
```

Skapa också en variabel som heter **selectedCity**<br>

2. Skapa sedan en komponent som heter **cityitem** som tar in en stad som props.
**cityitem** visar stadens namn tillsammans med en knapp bredvid.<br>
3. När man klickar på knappen ska staden skickas till parent komponenten (app-komponenten) och tilldelas till
selectedCity.<br>
4. **selectedCity** ska sedan visas i html med all information.

### Resultat
![Uppgift6](./assets/uppgift6.gif)

## Fråga 8 – Life-cycle-hooks
1. Skapa 3 stycken olika life-cycle-hooks.
2. Beroende på vilken ordning som de körs när en vue-komponent laddas in i webbläsaren skriv ut från life-cycle-hooken till konsolen *Jag körs [först|mellan|sist]!*.

### Resultat
![Uppgift8](./assets/Uppgift8.PNG)

