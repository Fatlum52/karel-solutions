# 2.1.2 followTheSeeds

Karel muss alle Beeper einsammeln.

## Lösungen

```java
void followTheSeeds() {
    while (beeperAhead()) {
        moveForward();
        pickBeeper();
        if (!beeperAhead()) {
            turnLeft();
        }
    }
}
```
