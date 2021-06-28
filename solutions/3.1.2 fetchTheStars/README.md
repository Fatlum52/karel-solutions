# 3.1.2 fetchTheStars

## Lösung

```java
void fetchTheStars() {
    while (frontIsClear()) {
        column();
        moveForward();
    }
    column();
}

void column() {
    turnLeft();
    walkAndPick();
    dropBeeper();
    turnLeft();
}

void walkAndPick() {
    if (frontIsClear()) {
        moveForward();
        walkAndPick();
        moveForward();
    } else {
        pickBeeper();
        turnAround();   
    }
}
```
