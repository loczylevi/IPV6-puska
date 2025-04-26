# IPV6-puska IPV6 cim rövidités

1️⃣ Nullák elhagyása a csoport elején
Egy hexadecimális csoport elején álló nullákat el lehet hagyni.

Példa:
0db8 → db8
0042 → 42

Tehát:

```bash

2001:0db8:0000:0000:0000:ff00:0042:8329

```
így rövidül:

```bash

2001:db8:0:0:0:ff00:42:8329

```

2️⃣ Hosszú nullasorozatok cseréje ::-ra
Az egymást követő nulla csoportok közül csak egy sorozatot lehet ::-ra cserélni a címben, hogy rövidebb legyen.

Példa:
0:0:0 → ::

A fenti cím:

```bash
2001:db8:0:0:0:ff00:42:8329
```
tovább rövidíthető:

```bash
2001:db8::ff00:42:8329
```

👉 Fontos: csak egyetlen :: lehet egy IPv6 címben, mert különben nem lehetne egyértelműen rekonstruálni, hány csoportnyi nulla hiányzik.

