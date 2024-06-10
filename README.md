## Datentypen

### Strings
Als erstes definieren wir zwei Beispiel-Strings:
```javascript
let text_1 = 'Hallo zusammen';
let text_2 = 'Willkommen zum JavaScriptkurs';
```

Man kann Strings einfach zusammenkleben (konkatenieren):
```javascript
let message = text_1 + text_2;
console.log(message); // Ausgabe: Hallo zusammenWillkommen zum JavaScriptkurs
```

Mit `\n` kann man einen Zeilenumbruch hinzufügen:
```javascript
console.log(text_1 + '\n' + text_2);
// Ausgabe: 
// Hallo zusammen
// Willkommen zum JavaScriptkurs
```

Man kann Strings auch wiederholen:
```javascript
console.log(text_1.repeat(5));
// Ausgabe: Hallo zusammenHallo zusammenHallo zusammenHallo zusammenHallo zusammen
```

Man kann einzelne Buchstaben aus einem String holen (der erste hat den Index 0). Negative Zahlen führen dazu, dass von 'hinten' angefangen wird:
```javascript
console.log(text_1[0], text_1[text_1.length - 1]); 
// Ausgabe: H n
```

Oder Ausschnitte:
```javascript
console.log(text_1.slice(0, 3), text_1.slice(0, -2)); 
// Ausgabe: Hal Hallo zusamm
```

### Zahlen
Es gibt Zahlen. Wunderbar. Man kann Zahlen addieren:
```javascript
console.log(1 + 2); // Ausgabe: 3
```

Subtrahieren:
```javascript
console.log(4 - 7); // Ausgabe: -3
```

Multiplizieren:
```javascript
console.log(3 * 5); // Ausgabe: 15
```

Exponenzieren:
```javascript
console.log(2 ** 8); // Ausgabe: 256
```

Und dividieren:
```javascript
console.log(8 / 4); // Ausgabe: 2
```

Ganzzahlige Division kann mit `Math.floor` erreicht werden:
```javascript
console.log(Math.floor(14 / 3)); // Ausgabe: 4
```

Den Rest einer Division berechnet man mit `%`:
```javascript
console.log(14 % 3); // Ausgabe: 2
```

Zahlen kann man z.B. auch als Strings erzeugen und dann konvertieren:
```javascript
let a = parseInt('5');
console.log(a, typeof a); // Ausgabe: 5 'number'
```

### Booleans
Die einzigen Werte von booleans sind:
```javascript
console.log(true);  // Ausgabe: true
console.log(false); // Ausgabe: false
```

Booleans sind das Ergebnis z.B. von Vergleichen:
```javascript
console.log(1 == 1);           // Ausgabe: true
console.log(2 >= 3);       // Ausgabe: false
console.log('Hallo' != 'Welt');// Ausgabe: true
console.log(1 <= 0.5);         // Ausgabe: false
console.log(2 > 0);            // Ausgabe: true
```

Man kann booleans auch mit `&&` und `||` kombinieren:
```javascript
console.log(true && true);   // Ausgabe: true
console.log(true && false);  // Ausgabe: false
console.log(true || false);  // Ausgabe: true
```

Alles in JavaScript hat einen Wahrheitswert:
```javascript
console.log(Boolean(0));     // Ausgabe: false
console.log(Boolean(10));    // Ausgabe: true
console.log(Boolean("Hallo"));// Ausgabe: true
console.log(Boolean(""));    // Ausgabe: false
```

### `typeof` Operator

Der `typeof` Operator wird verwendet, um den Datentyp einer Variablen oder eines Wertes in JavaScript zu bestimmen. Hier sind einige Beispiele:

#### Zahlen
```javascript
let a = 42;
let b = 3.14;
console.log(typeof a); // Ausgabe: 'number'
console.log(typeof b); // Ausgabe: 'number'
```

#### Strings
```javascript
let c = 'Hallo Welt';
console.log(typeof c); // Ausgabe: 'string'
```

#### Booleans
```javascript
let d = true;
let e = false;
console.log(typeof d); // Ausgabe: 'boolean'
console.log(typeof e); // Ausgabe: 'boolean'
```

### If/Else
```javascript
let text = 'Ein willkuerlicher Text der evtl ausgegeben werden soll';
let ausgabe = false;

if (ausgabe) {
    console.log(text);
} else {
    console.log("Oder auch nicht - ausgabe = false");
}
// Ausgabe: Oder auch nicht - ausgabe = false
```

Auch mehrere Zweige sind möglich:
```javascript
let zahl = 5;

if (zahl < 5) {
    console.log("Die Zahl ist kleiner als 5.");
} else if (zahl == 5) {
    console.log("Die Zahl ist 5.");
} else if (zahl == 6) {
    console.log("Die Zahl ist 6.");
} else {
    console.log("Die Zahl ist größer als 6.");
}
// Ausgabe: Die Zahl ist 5.
```

### Funktionen
Funktionen sind ähnlich zu mathematischen Funktionen, sie nehmen Argumente und geben Ergebnisse zurück. Ein Beispiel ist die eingebaute Funktion `length`. Es gibt weitere bereits in JavaScript definierte Funktionen:
```javascript
console.log("Hallo Welt".length); // Ausgabe: 10
```

Eigene Funktionen definiert man so:
```javascript
function foo(a, b) {
    return a + b;
}
```

Dies definiert eine Funktion `foo`, die zwei Argumente `a` und `b` nimmt und dann die Summe beider zurückgibt:
```javascript
console.log(foo(2, 3)); // Ausgabe: 5
```

Argumente können auch sogenannte defaults haben:
```javascript
function bar(a, b = 5) {
    a = a / 2;
    return a + b;
}
```

Verwendung der Funktion `bar`:
```javascript
console.log(bar(2));    // Ausgabe: 6
console.log(bar(2, 0)); // Ausgabe: 1
```

Natürlich! Hier ist der Teil für Arrays in JavaScript umgeschrieben und erweitert, um die Konzepte klarer zu machen:

## Mehr Datentypen

### Arrays
Arrays halten mehrere verschiedene Werte:
```javascript
let l = [1, 2, 3];
console.log(l); // Ausgabe: [1, 2, 3]
```

Arrays können ganz verschiedene Datentypen enthalten:
```javascript
console.log([1, 2.0, "Hallo Welt"]); // Ausgabe: [1, 2.0, 'Hallo Welt']
```
...was nicht heißt, dass man das oft benutzt oder tun sollte.

Das schon genannte `length` funktioniert auch für Arrays:
```javascript
console.log(l.length); // Ausgabe: 3
```

Arrays können verändert werden:
```javascript
l.push(5);
console.log(l); // Ausgabe: [1, 2, 3, 5]
```

```javascript
l[2] = 18;
console.log(l); // Ausgabe: [1, 2, 18, 5]
```

Diese Einführung sollte Ihnen einen grundlegenden Überblick über den Umgang mit Arrays in JavaScript geben!

### Loops

#### For
In JavaScript kann man über Arrays mit `for` iterieren:
```javascript
for (let i of [1, 2, 3]) {
    console.log(i);
}
// Ausgabe: 
// 1
// 2
// 3
```

Am häufigsten möchte man über eine Reihe von Zahlen iterieren, dafür gibt es `for` Loops:
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
// Ausgabe: 
// 0
// 1
// 2
// 3
// 4
```

#### While
`while` iteriert so lange wie ein Konditional `true` ist:
```javascript
let i = 0;

while (i < 5) {
    console.log(i);
    i++;
}
// Ausgabe: 
// 0
// 1
// 2
// 3
// 4
```

`while` ist besonders gut für endlose Loops zusammen mit dem Keyword `break`, das den aktuellen Loop beendet:
```javascript
let i = 0;

while (true) {
    console.log(i);
    i++;
    
    if (i == 5) {
        break;
    }
}
// Ausgabe: 
// 0
// 1
// 2
// 3
// 4
```

## Übungen

#### Strings und Zahlen in JavaScript

### Aufgabe 1: String in Großbuchstaben umwandeln

Schreiben Sie ein Programm, das einen String `str` in Großbuchstaben umwandelt und das Ergebnis auf der Konsole ausgibt.

**Vorgaben:**
```javascript
let str = "Hallo Welt!";
```

**Erwartete Ausgabe:**
```
HALLO WELT!
```

### Aufgabe 2: Ersten Buchstaben eines Strings in Großbuchstaben umwandeln

Schreiben Sie ein Programm, das den ersten Buchstaben eines Strings `str` in Großbuchstaben umwandelt und das Ergebnis auf der Konsole ausgibt.

**Vorgaben:**
```javascript
let str = "hallo welt!";
```

**Erwartete Ausgabe:**
```
Hallo welt!
```

### Aufgabe 3: Zeichen zählen

Schreiben Sie ein Programm, das die Anzahl der Vorkommen eines bestimmten Zeichens in einem String zählt. Verwenden Sie den String `str` und das Zeichen `char`.

**Vorgaben:**
```javascript
let str = "JavaScript ist großartig!";
let char = 'a';
```

**Erwartete Ausgabe:**
```
Das Zeichen 'a' kommt 3 Mal in dem String vor.
```

### Aufgabe 4: Durchschnitt berechnen

Schreiben Sie ein Programm, das den Durchschnitt von vier Zahlen berechnet und das Ergebnis auf der Konsole ausgibt. Verwenden Sie die Zahlen `num1`, `num2`, `num3` und `num4`.

**Vorgaben:**
```javascript
let num1 = 5;
let num2 = 10;
let num3 = 15;
let num4 = 20;
```

**Erwartete Ausgabe:**
```
Der Durchschnitt ist: 12.5
```

### Aufgabe 5: Modulo-Berechnung

Schreiben Sie ein Programm, das den Rest berechnet, wenn eine Zahl `a` durch eine Zahl `b` geteilt wird. Geben Sie das Ergebnis auf der Konsole aus.

**Vorgaben:**
```javascript
let a = 17;
let b = 4;
```

**Erwartete Ausgabe:**
```
Der Rest von 17 geteilt durch 4 ist: 1
```

### Aufgabe 6: Zeichen ersetzen

Schreiben Sie ein Programm, das alle Vorkommen eines bestimmten Zeichens in einem String durch ein anderes Zeichen ersetzt. Verwenden Sie den String `str`, das Zeichen `oldChar` und das Zeichen `newChar`.

**Vorgaben:**
```javascript
let str = "Hallo Welt!";
let oldChar = 'l';
let newChar = 'x';
```

**Erwartete Ausgabe:**
```
Haxxo Wext!
```

## The Challenge

### Task: Filtering presentations

Gegeben ist eine Liste von Dateinamen. Die Dateinamen enthalten Namen von Personen. Schreiben Sie eine Funktion, die als Argument den Namen einer Person bekommt. Die Funktion soll dann einen zufällig gewählten Dateinamen zurückgeben, der nicht den Namen der Person enthalten darf. 

```javascript
const datalist = ['kühlschränke_fabian.pptx','bohrmaschinen_robin.pptx', 'geb_robin_final.pptx', 'schleifsteinsteffen.pptx', 'badewasserqualitaet_marco-2019', 'franzi_stuggi.pdf', 'gfk_entsorgung.katha.pdf']
```
#### Additional Task: Filtering presentations EXTRA

Erweitern Sie die Funktion jetzt um ein weiteres Argument, das es erlaubt eine Liste von Dateinamen zu übergeben, die ebenfalls nicht ausgewählt werden dürfen. 

#### Additional addtional Task: Filtering presentations EXTRA XXL

Verfassen Sie nun ein script, das die Dateinamen aus einem gegebenen Ordner extrahiert und die ausgewählte Datei unter einem anonymen Namen in einen anderen Ordner kopiert. In diesem Fall ist die Verwendung von Programmiersprachen wie Python, R, C++, C, Fortran, Java, php, haskell oder Rust erlaubt 🦐🦧🦃🐁
