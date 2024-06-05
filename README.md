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

Certainly! Here's the extended tutorial translated into JavaScript and formatted in Markdown:

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

### Arrays als Rückgabewerte
JavaScript hat keine eingebaute Tupel-Datenstruktur wie Python. Stattdessen verwendet man Arrays, um mehrere Werte zurückzugeben:
```javascript
function baz() {
    return [1, "Hallo"];
}

let t = baz();
console.log(t); // Ausgabe: [1, 'Hallo']
console.log(typeof t); // Ausgabe: object
console.log(t[0]); // Ausgabe: 1
```

Arrays sind veränderlich, aber für unveränderliche Arrays kann man `Object.freeze` verwenden:
```javascript
let frozenT = Object.freeze([1, "Hallo"]);
frozenT[1] = "Welt"; // Keine Wirkung, da das Array gefroren ist
console.log(frozenT); // Ausgabe: [1, 'Hallo']
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

Oder über Objekte:
```javascript
for (let i of t) {
    console.log(i);
}
// Ausgabe: 
// 1
// Hallo
```

Am häufigsten möchte man über eine Reihe von Zahlen iterieren, dafür gibt es `for` Schleifen:
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

Oder mit einem Schrittwert:
```javascript
for (let j = 10; j < 30; j += 5) {
    console.log(j);
}
// Ausgabe: 
// 10
// 15
// 20
// 25
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

`while` ist besonders gut für Endlosschleifen zusammen mit dem Keyword `break`, das die aktuelle Schleife beendet:
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

### Übungen

#### Datentypen

##### Strings
JavaScript ist eine objektorientierte Sprache. Alle Dinge in JavaScript sind Objekte. Objekte können Methoden haben. Methoden sind Funktionen, die zu einem Objekt gehören und es selbst immer implizit als Argument haben:
```javascript
let s = 'Hallo Welt';
console.log(s); // Ausgabe: Hallo Welt
console.log(s.toUpperCase()); // Ausgabe: 'HALLO WELT'
```

Schau dir die Methoden an, die Strings haben, und fülle die Lücken:
```javascript
let s = "   dies ist eIn hässLicher TEXT       ";
s = s.trim().toLowerCase().replace(/(?:^|\s)\S/g, function(a) { return a.toUpperCase(); });
console.log(s);
```

##### Zahlen
Untersuche welchen Typ Summen oder Produkte von ints und floats haben:
```javascript
let a = 1;
let b = 2.0;
console.log(typeof a); // Ausgabe: number
console.log(typeof b); // Ausgabe: number
```

Was ist das Problem an:
```javascript
console.log(0.1 + 0.2 === 0.3); // Ausgabe: false
```

JavaScript unterstützt keine komplexen Zahlen direkt. Man kann jedoch Bibliotheken wie `math.js` verwenden, um damit zu arbeiten.

#### Funktionen
Definiere eine Funktion `fizzbazz` die folgende Bedingungen erfüllt:
Falls eine Zahl durch 3 teilbar ist gebe 'Fizz' aus, falls die Zahl durch 5 teilbar ist gebe 'Bazz' aus, falls sie durch 3 und 5 teilbar ist gebe 'FizzBazz' aus, sonst gebe die Zahl zurück:
```javascript
function fizzbazz(n) {
    if (n % 3 === 0 && n % 5 === 0) return 'FizzBazz';
    if (n % 3 === 0) return 'Fizz';
    if (n % 5 === 0) return 'Bazz';
    return n;
}
```

Definiere eine Funktion `colatz`, die folgende Bedingungen erfüllt:
`colatz` nimmt ein Int `n`, muss größer als 0 sein.
- wenn `n` gerade ist, gib `n / 2` zurück
- wenn `n` ungerade ist, gib `3n + 1` zurück

```javascript
function colatz(n) {
    if (n <= 0) throw new Error("n must be greater than 0");
    return n % 2 === 0 ? n / 2 : 3 * n + 1;
}
```

#### Schleifen
```javascript
let strings = ["Dies", "ist", "eine", "Liste", "von", "mehreren", "Wörtern"];

// Iteriere über die obige Liste
for (let s of strings) {
    console.log(s);
}

// Iteriere danach über sorted(strings)
for (let s of strings.slice().sort()) {
    console.log(s);
}

// Iteriere über reversed(strings)
for (let s of strings.slice().reverse()) {
    console.log(s);
}

// Iteriere über enumerate(strings)
strings.forEach((s, i) => console.log(i, s));
```

#### Timer
Schreibe einen Sekundenzähler(Countdown), der bis zu einer Stopzeit zählt und bei der Hälfte der Zeit anstatt der Zahl "Half way through" ausgibt. Nach Ablauf der Zeit soll noch ein "Puh, we are done! Nice job!" stehen. Du kannst mit `setTimeout` eine Sekunde warten bevor der nächste Schritt ausgeführt wird.

```javascript
function timer(stopTime) {
    let halfTime = Math.floor(stopTime / 2);
    let count = 0;

    let interval = setInterval(() => {
        if (count === halfTime) {
            console.log("Half way through");
        } else if (count >= stopTime) {
            console.log("Puh, we are done! Nice job!");
            clearInterval(interval);
        } else {
            console.log(count);
        }
        count++;
    }, 1000);
}

timer(10);
```

#### Datenauswertung
Die Liste 'test_data' enthält Messwerte mit der Kantenlänge eines Würfels. Allerdings enthält sie auch 'NaN (Not a Number)' - Werte. Als ersten Schritt entferne die NaN Werte und gebe eine neue Liste ohne diese aus.
Schreibe anschließend eine zweite Funktion, die aus den gemessenen Werten die Dichte des Stoffes berechnet und diese mittelt. Aus dem Mittelwert und den einzelnen Werten berechne die Standardabweichung. Die Funktion soll nun die gemittelte Dichte und den dazugehörigen Fehler ausgeben.

```javascript
function clean(data) {
    return data.filter(value => !isNaN(value));
}

function evaluate(data, m) {
    let cleanedData = clean(data);
    let densities = cleanedData.map(r => m / (r ** 3));
    let meanDensity = densities.reduce((sum, value) => sum + value, 0) / densities.length;

    let variance = densities.reduce((sum, value) => sum + ((value - meanDensity) ** 2), 0) / densities.length;
    let stdDev = Math.sqrt(variance);

    return {
        meanDensity: meanDensity,
        error: stdDev
    };
}

let test_data = [1, 2, NaN, 3, 4, NaN, 5];
console.log(evaluate(test_data, 10));
```

Diese Einführung sollte Ihnen einen grundlegenden Überblick über den Umgang mit Listen, Tupel, Schleifen und Funktionen in JavaScript geben!
