# 1.3.2 repairTheStreet

## Lösung

```java
void repairTheStreet() {
    repeat (9) {
        maybeRepair();
        moveForward();
    }
    maybeRepair();
}

void maybeRepair() {
    if (rightIsClear()) {
        turnRight();
        moveForward();
        dropBeeper();
        turnAround();
        moveForward();
        turnRight();
    }
}
```
