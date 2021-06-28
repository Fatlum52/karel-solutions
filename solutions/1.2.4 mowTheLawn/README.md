# 1.2.4 mowTheLawn

## Lösung

```java
void mowTheLawn() {
    repeat (2) {
        pick();
        turnUpLeft();
        pick();
        turnUpRight();
    }
    pick();
    turnUpLeft();
    pick();
}

void pick() {
    repeat (6) {
        moveForward();
        pickBeeper();
    }
    moveForward();
}

void turnUpLeft() {
    turnLeft();
    moveForward();
    turnLeft();
}

void turnUpRight() {
    turnRight();
    moveForward();
    turnRight();
}
```
