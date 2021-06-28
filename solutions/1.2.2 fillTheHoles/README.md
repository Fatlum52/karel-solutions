# 1.2.2 fillTheHoles

## Lösung

```java
void fillTheHoles() {
    repeat (4) {
        moveForward();
        turnRight();
        moveForward();
        dropBeeper();
        turnAround();
        moveForward();
        turnRight();
        moveForward();
    }
}
```
