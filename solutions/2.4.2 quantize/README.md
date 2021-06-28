# 2.4.2 quantize

Karel überprüft für jede Spalte: Liegen auf den ersten 6 Feldern Beeper, wird die ganze Spalte mit Beepern aufgefüllt.
Ansonsten werden alle Beeper der Spalte entfernt.

## Lösung

```java
void quantize() {
    while (frontIsClear()) {
        updateCode();
        turnLeft();
        moveForward();
    }
    updateCode();
}

void updateCode() {
    turnLeft();
    repeat (5) {
        moveForward();
    }
    if (onBeeper()) {
        // Auffüllen
        while (frontIsClear()) {
            moveForward();
            if (!onBeeper()) {
                dropBeeper();
            }
        }
        turnAround();
        while (frontIsClear()) {
            moveForward();
        }
    } else {
        // Entfernen
        turnAround();
        repeat (5) {
            moveForward();
            if (onBeeper()) {
                pickBeeper();
            }
        }
    } 
}
```

## Erklärung

Für jede Spalte wird `updateCode()` ausgeführt. Dort läuft Karel erst bis zum 6. Feld und überprüft, ob dort ein Beeper
liegt oder nicht. Liegt dort ein Beeper, wird die ganze Spalte aufgefüllt und Karel läuft wieder zum Anfang. Ansonsten 
läuft Karel direkt zum Anfang und löscht auf dem Weg alle Beeper.
