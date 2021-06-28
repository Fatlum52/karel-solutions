# 1.3.1 harvestTheField

## Lösung

```java
void harvestTheField() {
    half();
    turnAround();
    half();
}

void half() {
    pick();
    repeat (2) {
        moveForward();
        moveForward();
        turnLeft();   
    }
    pick();   
}

void pick() {
    repeat (4) {
        moveForward();
        pickBeeper();
        turnRight();
        moveForward();
        turnLeft();
    }
}
```
