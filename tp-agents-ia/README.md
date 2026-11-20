# tp-agents-ia

Petit projet Java (Maven, JUnit 5) utilisé pour le TP « agents IA » du module Qualité logicielle.

- `src/test/java/MoyenneTest.java` : 4 tests qui attendent une classe `Moyenne` (méthodes `calculer` et `mention`).
- `src/main/java/Main.java` : petit programme qui utilise `Moyenne`.
- Il n'y a volontairement **pas** de `Moyenne.java` : c'est l'agent IA (n8n + Ollama) qui l'écrit, sur la branche `agent-ia`.
- `annexes/` : la solution de référence `Moyenne.java` (hors du projet, non compilée).
- `.github/workflows/ci.yml` : lance `mvn -B test` à chaque push.
- `.github/workflows/deploy.yml` : lancé à la main (ou par n8n) ; il compile, teste et construit l'image Docker.

Le premier pipeline CI est rouge (cannot find symbol ... class Moyenne) : c'est normal.
