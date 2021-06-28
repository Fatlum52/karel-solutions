# 1.3.4 tileTheFloor

## Beschreibung

Karel muss alle Felder mit Beepern belegen. Dazu läuft er am Rand entlang und arbeitet sich immer weiter zur Mitte vor.

## Lösung

```java
void tileTheFloor() {
    repeat (100) {
        dropBeeper();
        if (!frontIsClear() || beeperAhead()) {
            turnLeft();
        }
        moveForward();
    }
}
```

## Erklärung

Karel muss alle Felder besuchen, also wird die Schleife `100` mal ausgeführt. Im Schleifenrumpf wird ein Beeper gelegt.
Sollte Karel an einer Wand stehen, muss er sich nach links drehen. Liegt vor ihm ein Beeper, hat er einen Ring fertig 
und kann den nächsten Ring beginnen. In jedem Fall geht Karol ein Feld weiter.
