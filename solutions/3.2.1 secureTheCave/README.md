# 3.2.1 secureTheCave

## Lösung

```java
void secureTheCave() {
    while (frontIsClear()) {
        column();
        moveForward();
    }
    column();
}

void column() {
    turnLeft();
    walk();
    pick();
    turnRight();
}

void walk() {
    moveForward();
    if (frontIsClear()) {
        walk();
    } else {
        turnAround();
    }
}

void pick() {
    if (onBeeper()) {
        pickBeeper();
        moveForward();
        pick();
        dropBeeper();
        moveForward();
    } else {
        walk();
    }
}
```
