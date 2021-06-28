# 1.1.1 obtainArtefact

## Lösung

```java
void obtainArtifact() {
  turnRight();
  moveForward();
  turnLeft();
  repeat (3) {
    moveForward();
  }
  turnLeft();
  moveForward();
  pickBeeper();
  moveForward();
  turnLeft();
  repeat (3) {
    moveForward();
  }
  turnLeft();
  moveForward();
  dropBeeper();
}
```
