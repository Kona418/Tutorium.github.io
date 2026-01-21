---
title: Kontrollstrukturen
parent: Programmierung 1
nav_order: 2
layout: default
---

## Main Class
```java
package src;

// EXERCISES – KONTROLLSTRUKTUREN
public class KontrollstrukturenExercises {

    public static void main(String[] args) {

        // AUFGABE 1:
        // - Schreibe eine Methode "istPositiv".
        // - Parameter: eine ganze Zahl.
        // - Ausgabe:
        //   * "Zahl ist positiv"
        //   * "Zahl ist negativ"
        //   * "Zahl ist null"
        istPositiv(10);
        istPositiv(-5);
        istPositiv(0);


        // AUFGABE 2:
        // - Schreibe eine Methode "istGerade".
        // - Parameter: eine ganze Zahl.
        // - Ausgabe: "gerade" oder "ungerade".
        istGerade(4);
        istGerade(7);


        // AUFGABE 3:
        // - Schreibe eine Methode "noteBewerten".
        // - Parameter: note (int von 1–6).
        // - Ausgabe mit if/else:
        //   1–2 → "sehr gut / gut"
        //   3–4 → "befriedigend / ausreichend"
        //   5–6 → "nicht bestanden"
        noteBewerten(2);
        noteBewerten(4);
        noteBewerten(6);


        // AUFGABE 4:
        // - Schreibe eine Methode "zugangErlaubt".
        // - Parameter:
        //   * alter (int)
        //   * hatAusweis (boolean)
        // - Zugang erlaubt, wenn:
        //   * alter >= 18 UND hatAusweis == true
        zugangErlaubt(20, true);
        zugangErlaubt(16, true);


        // AUFGABE 5:
        // - Schreibe eine Methode "rabattBerechnen".
        // - Parameter: preis (double).
        // - Wenn preis >= 100 → 10% Rabatt
        // - Sonst kein Rabatt
        // - Ausgabe des Endpreises
        rabattBerechnen(150.0);
        rabattBerechnen(50.0);


        // ======================================
        // SWITCH / CASE
        // ======================================

        // AUFGABE 6:
        // - Schreibe eine Methode "wochentagName".
        // - Parameter: tag (int von 1–7).
        // - Verwende switch/case.
        // - Ausgabe: Name des Wochentags.
        wochentagName(1);
        wochentagName(5);
        wochentagName(7);


        // AUFGABE 7:
        // - Schreibe eine Methode "studiengangName".
        // - Parameter: studiengangCode (char).
        // - switch/case:
        //   'I' → Informatik
        //   'B' → BWL
        //   'M' → Maschinenbau
        //   default → Unbekannt
        studiengangName('I');
        studiengangName('B');
        studiengangName('X');


        // AUFGABE 8:
        // - Schreibe eine Methode "ampelStatus".
        // - Parameter: farbe (String).
        // - switch/case:
        //   "rot" → "Stopp"
        //   "gelb" → "Achtung"
        //   "grün" → "Fahren"
        ampelStatus("rot");
        ampelStatus("grün");


        // ======================================
        // KOMBINATIONSAUFGABEN
        // ======================================

        // Kombi-AUFGABE 9:
        // - Schreibe eine Methode "pruefeStudent".
        // - Parameter:
        //   * alter (int)
        //   * eingeschrieben (boolean)
        // - Ausgabe:
        //   * "Student volljährig"
        //   * "Student minderjährig"
        //   * "Keine Einschreibung"
        pruefeStudent(22, true);
        pruefeStudent(17, true);
        pruefeStudent(25, false);


        // Kombi-AUFGABE 10:
        // - Schreibe eine Methode "kategoriePreis".
        // - Parameter:
        //   * kategorie (char)
        //   * grundpreis (double)
        // - switch/case:
        //   'A' → +0€
        //   'B' → +10€
        //   'C' → +20€
        // - Ausgabe des Endpreises
        kategoriePreis('A', 50.0);
        kategoriePreis('C', 50.0);


        // BONUS-AUFGABE 11 zum TERNARY OPERATOR:
        // - Schreibe eine Methode "bewerteAlterKurz".
        // - Parameter: alter (int)
        // - Rückgabe: String
        //     * "volljährig" wenn alter >= 18
        //     * sonst "minderjährig"
        // - Verwende den ternary operator! Die Methode enthält nur eine Zeile Code.
        String alter1 = getAltersangabe(20);
        String alter2 = getAltersangabe(15);

        System.out.println("Person 1 ist + " + alter1);
        System.out.println("Person 2 ist + " + alter2);


        // BONUS-AUFGABE 12 zum TERNARY OPERATOR:
        // - Schreibe eine Methode "ticketStatus".
        // - Parameter:
        //   * hatTicket (boolean)
        // - Verwende den ternary operator! Die Methode hat nur eine Zeile Code.
        // - Die Methode soll folgendes in der Konsole ausgeben:
        //   * "Ticket vorhanden" wenn true
        //   * "Kein Ticket" wenn false
        ticketStatus(true);
        ticketStatus(false);
    }


    // =====================
    // METHODEN
    // =====================



}
```

## Git Branch
```console
git checkout semester1/kontrollstrukturen
```

## Lösung Kontrollstrukturen

<details>
    <summary>
        Lösung
    </summary>
<div class="my-code-container">
    <h2>MainSolution Class</h2>
    {% highlight java %}package src;

// EXERCISES – KONTROLLSTRUKTUREN
public class KontrollstrukturenSolutions {

    public static void main(String[] args) {

        // AUFGABE 1:
        // - Schreibe eine Methode "istPositiv".
        // - Parameter: eine ganze Zahl.
        // - Ausgabe:
        //   * "Zahl ist positiv"
        //   * "Zahl ist negativ"
        //   * "Zahl ist null"
        istPositiv(10);
        istPositiv(-5);
        istPositiv(0);


        // AUFGABE 2:
        // - Schreibe eine Methode "istGerade".
        // - Parameter: eine ganze Zahl.
        // - Ausgabe: "gerade" oder "ungerade".
        istGerade(4);
        istGerade(7);


        // AUFGABE 3:
        // - Schreibe eine Methode "noteBewerten".
        // - Parameter: note (int von 1–6).
        // - Ausgabe mit if/else:
        //   1–2 → "sehr gut / gut"
        //   3–4 → "befriedigend / ausreichend"
        //   5–6 → "nicht bestanden"
        noteBewerten(2);
        noteBewerten(4);
        noteBewerten(6);


        // AUFGABE 4:
        // - Schreibe eine Methode "zugangErlaubt".
        // - Parameter:
        //   * alter (int)
        //   * hatAusweis (boolean)
        // - Zugang erlaubt, wenn:
        //   * alter >= 18 UND hatAusweis == true
        zugangErlaubt(20, true);
        zugangErlaubt(16, true);


        // AUFGABE 5:
        // - Schreibe eine Methode "rabattBerechnen".
        // - Parameter: preis (double).
        // - Wenn preis >= 100 → 10% Rabatt
        // - Sonst kein Rabatt
        // - Ausgabe des Endpreises
        rabattBerechnen(150.0);
        rabattBerechnen(50.0);


        // ======================================
        // SWITCH / CASE
        // ======================================

        // AUFGABE 6:
        // - Schreibe eine Methode "wochentagName".
        // - Parameter: tag (int von 1–7).
        // - Verwende switch/case.
        // - Ausgabe: Name des Wochentags.
        wochentagName(1);
        wochentagName(5);
        wochentagName(7);


        // AUFGABE 7:
        // - Schreibe eine Methode "studiengangName".
        // - Parameter: studiengangCode (char).
        // - switch/case:
        //   'I' → Informatik
        //   'B' → BWL
        //   'M' → Maschinenbau
        //   default → Unbekannt
        studiengangName('I');
        studiengangName('B');
        studiengangName('X');


        // AUFGABE 8:
        // - Schreibe eine Methode "ampelStatus".
        // - Parameter: farbe (String).
        // - switch/case:
        //   "rot" → "Stopp"
        //   "gelb" → "Achtung"
        //   "grün" → "Fahren"
        ampelStatus("rot");
        ampelStatus("grün");


        // ======================================
        // KOMBINATIONSAUFGABEN
        // ======================================

        // Kombi-AUFGABE 9:
        // - Schreibe eine Methode "pruefeStudent".
        // - Parameter:
        //   * alter (int)
        //   * eingeschrieben (boolean)
        // - Ausgabe:
        //   * "Student volljährig"
        //   * "Student minderjährig"
        //   * "Keine Einschreibung"
        pruefeStudent(22, true);
        pruefeStudent(17, true);
        pruefeStudent(25, false);


        // Kombi-AUFGABE 10:
        // - Schreibe eine Methode "kategoriePreis".
        // - Parameter:
        //   * kategorie (char)
        //   * grundpreis (double)
        // - switch/case:
        //   'A' → +0€
        //   'B' → +10€
        //   'C' → +20€
        // - Ausgabe des Endpreises
        kategoriePreis('A', 50.0);
        kategoriePreis('C', 50.0);


        // BONUS-AUFGABE 11 zum TERNARY OPERATOR:
            // - Schreibe eine Methode "bewerteAlterKurz".
            // - Parameter: alter (int)
            // - Rückgabe: String
            //     * "volljährig" wenn alter >= 18
            //     * sonst "minderjährig"
            // - Verwende den ternary operator! Die Methode enthält nur eine Zeile Code.
        String alter1 = getAltersangabe(20);
        String alter2 = getAltersangabe(15);

        System.out.println("Person 1 ist + " + alter1);
        System.out.println("Person 2 ist + " + alter2);


        // BONUS-AUFGABE 12 zum TERNARY OPERATOR:
            // - Schreibe eine Methode "ticketStatus".
            // - Parameter:
            //   * hatTicket (boolean)
            // - Verwende den ternary operator! Die Methode hat nur eine Zeile Code.
            // - Die Methode soll folgendes in der Konsole ausgeben:
            //   * "Ticket vorhanden" wenn true
            //   * "Kein Ticket" wenn false
        ticketStatus(true);
        ticketStatus(false);
    }


    // =====================
    // METHODEN
    // =====================

    public static void istPositiv(int zahl) {
        if (zahl > 0) {
            System.out.println("Zahl ist positiv");
        } else if (zahl < 0) {
            System.out.println("Zahl ist negativ");
        } else {
            System.out.println("Zahl ist null");
        }
    }

    public static void istGerade(int zahl) {
        if (zahl % 2 == 0) {
            System.out.println("gerade");
        } else {
            System.out.println("ungerade");
        }
    }

    public static void noteBewerten(int note) {
        if (note <= 2) {
            System.out.println("sehr gut / gut");
        } else if (note <= 4) {
            System.out.println("befriedigend / ausreichend");
        } else {
            System.out.println("nicht bestanden");
        }
    }

    public static void zugangErlaubt(int alter, boolean hatAusweis) {
        if (alter >= 18 && hatAusweis) {
            System.out.println("Zugang erlaubt");
        } else {
            System.out.println("Zugang verweigert");
        }
    }

    public static void rabattBerechnen(double preis) {
        if (preis >= 100) {
            preis = preis * 0.9;
        }
        System.out.println("Endpreis: " + preis + "€");
    }

    public static void wochentagName(int tag) {
        switch (tag) {
            case 1:
                System.out.println("Montag");
                break;
            case 2:
                System.out.println("Dienstag");
                break;
            case 3:
                System.out.println("Mittwoch");
                break;
            case 4:
                System.out.println("Donnerstag");
                break;
            case 5:
                System.out.println("Freitag");
                break;
            case 6:
                System.out.println("Samstag");
                break;
            case 7:
                System.out.println("Sonntag");
                break;
            default:
                System.out.println("Ungültiger Tag");
        }
    }

    public static void studiengangName(char code) {
        switch (code) {
            case 'I':
                System.out.println("Informatik");
                break;
            case 'B':
                System.out.println("BWL");
                break;
            case 'M':
                System.out.println("Maschinenbau");
                break;
            default:
                System.out.println("Unbekannter Studiengang");
        }
    }

    public static void ampelStatus(String farbe) {
        switch (farbe) {
            case "rot":
                System.out.println("Stopp");
                break;
            case "gelb":
                System.out.println("Achtung");
                break;
            case "grün":
                System.out.println("Fahren");
                break;
            default:
                System.out.println("Unbekannte Farbe");
        }
    }

    public static void pruefeStudent(int alter, boolean eingeschrieben) {
        if (!eingeschrieben) {
            System.out.println("Keine Einschreibung");
        } else if (alter >= 18) {
            System.out.println("Student volljährig");
        } else {
            System.out.println("Student minderjährig");
        }
    }

    public static void kategoriePreis(char kategorie, double grundpreis) {
        switch (kategorie) {
            case 'A':
                System.out.println("Endpreis: " + grundpreis + "€");
                break;
            case 'B':
                System.out.println("Endpreis: " + (grundpreis + 10) + "€");
                break;
            case 'C':
                System.out.println("Endpreis: " + (grundpreis + 20) + "€");
                break;
            default:
                System.out.println("Ungültige Kategorie");
        }
    }

    public static String getAltersangabe(int alter) {
        return (alter >= 18) ? "volljährig" : "minderjährig";
    }

    public static void ticketStatus(boolean hatTicket) {
        System.out.println(hatTicket ? "Ticket vorhanden" : "Kein Ticket");
    }
}{% endhighlight %}
</div>
</details>
