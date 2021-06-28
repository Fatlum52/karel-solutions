# 3.2.2 layAndRemoveTiles

## Lösung

```java
void layAndRemoveTiles() {
    if (onBeeper()) {
        turnAround();
    } else {
        dropBeeper();
        if (frontIsClear() && !beeperAhead()) {
            moveForward();
            layAndRemoveTiles();
            moveForward();
            pickBeeper();
        } else {
            turnLeft();
            moveForward();
            layAndRemoveTiles();
            moveForward();
            turnRight();
            pickBeeper();
        }
    }
}
```
