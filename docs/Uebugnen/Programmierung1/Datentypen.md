---
title: Datentypen
parent: Programmierung 1
nav_order: 1
layout: default
---

## Main Class
```java
package src;


// EXERCISES
// Die System.out.println() statements dienen der Überprüfung des Ergebnisses und müssen nicht verändert werden.


public class Main {
    public static void main(String[] args) {
        // AUFGABE 1:
        // - Lege eine Variable "anzahlStudenten" mit passendem Datentyp an.
        // - Die Variable soll die Zahl 120 speichern.


        System.out.println("anzahlStudenten: " + anzahlStudenten);


        // AUFGABE 2:
        // - Lege drei Variablen mit ganzzahligem Wert an: "jahr", "monat", "tag"
        // - Speichere das Datum 21.01.2026 darin (jahr=2026, monat=1, tag=21).


        System.out.println("Datum: " + tag + "." + monat + "." + jahr);


        // AUFGABE 3:
        // - Lege eine Variable "preis" mit passendem Datentyp an.
        // - Speichere den Wert 19.99 darin.


        System.out.println("Preis: " + preis + "€");

        // AUFGABE 4:
        // - Lege zwei Variablen mit passendem Datentyp an: "temperaturMorgens" und "temperaturAbends".
        // - Speichere 7.5 und 12.0 darin (als float).


        System.out.println("Die Temperatur beträgt morgens " + temperaturMorgens + " Grad und abends " + temperaturAbends + " Grad");


        // AUFGABE 5:
        // - Lege eine Variable "istEingeschrieben" it passendem Datentyp an.
        // - Setze sie auf true.


        System.out.println("Der Student ist eingeschrieben: " + (istEingeschrieben ? "true" : "false"));

        // AUFGABE 6:
        // - Lege zwei Variablen mit passendem Datentyp an: "hatAusweis" und "hatTicket".
        // - Setze "hatAusweis" auf true und "hatTicket" auf false.


        System.out.println("Ich habe meinen Ausweis dabei: " + (hatAusweis ? "true" : "false"));
        System.out.println("Ich habe ein Ticket: " + (hatTicket ? "true" : "false"));


        // AUFGABE 7:
        // - Lege eine Variable "initial" vom mit passendem Datentyp an.
        // - Speichere den Anfangsbuchstaben deines Namens darin (z.B. 'A').


        System.out.println("Anfangsbuchstabe: " + initial);


        // AUFGABE 8:
        // - Lege zwei Variablen mit passendem Datentyp an an: "antwort" und "trennzeichen".
        // - Setze "antwort" auf 'J' (für Ja) und "trennzeichen" auf ';'


        System.out.println("Antwort: " + antwort + trennzeichen);


        // AUFGABE 9:
        // - Lege eine Variable "vorname" mit passendem Datentyp an.
        // - Speichere deinen Vornamen und Nachnamen darin.


        System.out.println("Name: " + vorname + " " + nachname);


        // AUFGABE 10:
        // - Lege zwei Variablen mit passendem Datentyp an: "stadt" und "land".
        // - Speichere deine Heimatstadt und Land darin.


        System.out.println("Ich kome aus " + stadt + ", " + land);


        // ======================================
        // KOMBINATIONSAUFGABEN (etwas schwerer)
        // ======================================

        // Kombi-AUFGABE 11:
        // - Lege Variablen an, die zusammen eine "Studentenkarte" beschreiben:
        //   * "name" (z.B. "Samira Becker")
        //   * "matrikelnummer" (z.B. 472901)
        //   * "gueltig" (true/false)
        //   * "studiengangCode" (z.B. 'I' für Informatik)
        // - Setze passende Beispielwerte ein (du darfst die Beispiele nehmen).


        System.out.println("NAME: " + name);
        System.out.println("MATRIKELNUMMER: " + matrikelnummer);
        System.out.println("GÜLTIG: " + (gueltig ? "ja" : "nein"));
        System.out.println("STUDIENGANG CODE: " + studiengangCode);


        // Kombi-AUFGABE 12:
        // - Lege Variablen an, die eine "Messung" beschreiben:
        //   * "sensorName" (z.B. "SENSOR-3")
        //   * "messwert" (z.B. 0.875)
        //   * "einheit" (z.B. 'C' für Celsius)
        // - Setze passende Beispielwerte ein.


        System.out.println(sensorName + " misst " + messwert + " " + einheit);
    }
}
```

## Git Branch
```console
git checkout semester1/datatypes
```

## Lösung Datentypen

<details>
    <summary>
        Lösung
    </summary>
<div class="my-code-container">
    <h2>MainSolution Class</h2>
    {% highlight java %}package src;


// EXERCISES
public class Main {
    public static void main(String[] args) {
        // AUFGABE 1:
        // - Lege eine Variable "anzahlStudenten" mit passendem Datentyp an.
        // - Die Variable soll die Zahl 120 speichern.
        int anzahlStudenten = 120;

        System.out.println("anzahlStudenten: " + anzahlStudenten);


        // AUFGABE 2:
        // - Lege drei Variablen mit ganzzahligem Wert an: "jahr", "monat", "tag"
        // - Speichere das Datum 21.01.2026 darin (jahr=2026, monat=1, tag=21).
        int jahr = 2026;
        int monat = 1;
        int tag = 21;

        System.out.println("Datum: " + tag + "." + monat + "." + jahr);


        // AUFGABE 3:
        // - Lege eine Variable "preis" mit passendem Datentyp an.
        // - Speichere den Wert 19.99 darin.
        double preis = 19.99;

        System.out.println("Preis: " + preis + "€");

        // AUFGABE 4:
        // - Lege zwei Variablen mit passendem Datentyp an: "temperaturMorgens" und "temperaturAbends".
        // - Speichere 7.5 und 12.0 darin (als float).
        double temperaturMorgens = 7.5;
        double temperaturAbends = 12.0;

        System.out.println("Die Temperatur beträgt morgens " + temperaturMorgens + " Grad und abends " + temperaturAbends + " Grad");


        // AUFGABE 5:
        // - Lege eine Variable "istEingeschrieben" it passendem Datentyp an.
        // - Setze sie auf true.
        boolean istEingeschrieben = true;

        System.out.println("Der Student ist eingeschrieben: " + (istEingeschrieben ? "true" : "false"));

        // AUFGABE 6:
        // - Lege zwei Variablen mit passendem Datentyp an: "hatAusweis" und "hatTicket".
        // - Setze "hatAusweis" auf true und "hatTicket" auf false.
        boolean hatAusweis = true;
        boolean hatTicket = false;

        System.out.println("Ich habe meinen Ausweis dabei: " + (hatAusweis ? "true" : "false"));
        System.out.println("Ich habe ein Ticket: " + (hatTicket ? "true" : "false"));


        // AUFGABE 7:
        // - Lege eine Variable "initial" vom mit passendem Datentyp an.
        // - Speichere den Anfangsbuchstaben deines Namens darin (z.B. 'A').
        char initial = 'A';

        System.out.println("Anfangsbuchstabe: " + initial);


        // AUFGABE 8:
        // - Lege zwei Variablen mit passendem Datentyp an an: "antwort" und "trennzeichen".
        // - Setze "antwort" auf 'J' (für Ja) und "trennzeichen" auf ';'
        char antwort = 'J';
        char trennzeichen = ';';

        System.out.println("Antwort: " + antwort + trennzeichen);


        // AUFGABE 9:
        // - Lege eine Variable "vorname" mit passendem Datentyp an.
        // - Speichere deinen Vornamen und Nachnamen darin.
        String vorname = "Vorname";
        String nachname = "Nachname";

        System.out.println("Name: " + vorname + " " + nachname);


        // AUFGABE 10:
        // - Lege zwei Variablen mit passendem Datentyp an: "stadt" und "land".
        // - Speichere deine Heimatstadt und Land darin.
        String stadt = "Nordpol City";
        String land = "Nordpol";

        System.out.println("Ich kome aus " + stadt + ", " + land);


        // ======================================
        // KOMBINATIONSAUFGABEN (etwas schwerer)
        // ======================================

        // Kombi-AUFGABE 11:
        // - Lege Variablen an, die zusammen eine "Studentenkarte" beschreiben:
        //   * "name" (z.B. "Samira Becker")
        //   * "matrikelnummer" (z.B. 472901)
        //   * "gueltig" (true/false)
        //   * "studiengangCode" (z.B. 'I' für Informatik)
        // - Setze passende Beispielwerte ein (du darfst die Beispiele nehmen).
        String name = "Name";
        int matrikelnummer = 1234;
        boolean gueltig = true;
        char studiengangCode = 'I';

        System.out.println("NAME: " + name);
        System.out.println("MATRIKELNUMMER: " + matrikelnummer);
        System.out.println("GÜLTIG: " + (gueltig ? "ja" : "nein"));
        System.out.println("STUDIENGANG CODE: " + studiengangCode);


        // Kombi-AUFGABE 12:
        // - Lege Variablen an, die eine "Messung" beschreiben:
        //   * "sensorName" (z.B. "SENSOR-3")
        //   * "messwert" (z.B. 0.875)
        //   * "einheit" (z.B. 'C' für Celsius)
        // - Setze passende Beispielwerte ein.
        String sensorName = "SENSOR-3";
        double messwert = 0.05;
        char einheit = 'C';

        System.out.println(sensorName + " misst " + messwert + " " + einheit);
    }
}{% endhighlight %}
</div>
</details>
