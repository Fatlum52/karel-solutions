# 2.1.3 cleanTheTunnels

## Lösungen

```java
void cleanTheTunnels() {
  repeat (9) {
    clean();
    moveForward();
  }
  clean();
}
  
void clean() {
  if (onBeeper()) {
    turnLeft();
    pickBeeper();
    while (beeperAhead()) {
      moveForward();
      pickBeeper();
    }
    turnAround();
    while (frontIsClear()) {
      moveForward();
    }
    turnLeft();
  }
}
```


## Erklärung

Für jede Spalte wird die Funktion `clean()` aufgerufen.
Dort wird erst mit `if (onBeeper())` überprüft, ob überhaupt ein Beeper in der Spalte liegt.
Falls Ja, werden alle Beeper aufgehoben, bis `beeperAhead()` nicht mehr erfüllt ist. Letztendlich läuft man wieder
bis zur unteren Wand zurück und führt mit der nächsten Spalte fort.
