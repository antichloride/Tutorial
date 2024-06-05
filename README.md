Sure, here is the tutorial in Markdown format:

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

Hier sehen wir auch, dass es zwei verschiedene Typen von Zahlen gibt:
```javascript
console.log(typeof 2); // Ausgabe: 'number'
console.log(typeof 2.0); // Ausgabe: 'number'
```

In JavaScript sind alle Zahlen vom Typ `number`.

Die Ergebnisse von Division sind immer `number`:
```javascript
console.log(0.5 + 0.25); // Ausgabe: 0.75
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

### Bools
Die einzigen Werte von bools sind:
```javascript
console.log(true);  // Ausgabe: true
console.log(false); // Ausgabe: false
```

Bools sind das Ergebnis z.B. von Vergleichen:
```javascript
console.log(1 == 1);           // Ausgabe: true
console.log(2.0 >= 3.0);       // Ausgabe: false
console.log('Hallo' != 'Welt');// Ausgabe: true
console.log(1 <= 0.5);         // Ausgabe: false
console.log(2 > 0);            // Ausgabe: true
```

Man kann bools auch mit `&&` und `||` kombinieren:
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

Diese Einführung sollte Ihnen einen grundlegenden Überblick über den Umgang mit Strings, Zahlen, Booleans, Kontrollstrukturen und Funktionen in JavaScript geben!
