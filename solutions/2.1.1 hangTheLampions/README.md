# 2.1.1 hangTheLampions

Für jede Spalte muss Karel einen Beeper aufheben und ihn am anderen Ende wieder platzieren.

**Hinweis:** while-Schleifen können jetzt verwendet werden.

## Lösung

```java
void hangTheLampions() {
    while (onBeeper()) {
        turnLeft();
        pickBeeper();
        while (frontIsClear()) {
            moveForward();
        }
        dropBeeper();
        turnAround();
        while (frontIsClear()) {
            moveForward();
        }
        turnLeft();
        if (frontIsClear()) {
            moveForward();   
        }
    }
}
```
