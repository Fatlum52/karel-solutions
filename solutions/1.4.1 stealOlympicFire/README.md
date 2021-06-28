# 1.4.1 stealOlympicFire

Karel muss eine Treppe hinaufsteigen. Auf der höchsten Stufe sammelt er einen Beeper auf,
danach läuft er gerade hinunter.

## Lösung

```java
void stealOlympicFire() {
    moveForward();
    repeat (6) {
        turnLeft();
        moveForward();
        turnRight();
        moveForward();
    }
    pickBeeper();
    moveForward();
    turnRight();
    repeat (6) {
        moveForward();
    }
    turnLeft();
    moveForward();
}
```
