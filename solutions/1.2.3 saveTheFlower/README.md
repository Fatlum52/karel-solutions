# 1.2.3 saveTheFlower

## Lösung

```java
void saveTheFlower() {
    moveForward();
    pickBeeper();
    repeat (4) {
        turnLeft();
        moveForward();
        moveForward();
        turnRight();
        moveForward();
    }
    dropBeeper();
    repeat (4) {
        moveForward();
        turnRight();
        moveForward();
        moveForward();
        turnLeft();
    }
}
```
