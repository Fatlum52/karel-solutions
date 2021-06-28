# 1.1.3 defuseTwoBombs

## Lösung

```java
void defuseTwoBombs() {
    defuseBomb();
    turnLeft();
    defuseBomb();
}

void defuseBomb() {
    moveNineForward();
    pickBeeper();
    turnAround();
    moveNineForward();
    turnAround();
}

void moveNineForward() {
    repeat (9) {
        moveForward();
    }
}
```
