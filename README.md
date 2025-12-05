# AUT24_RobotOchRobotsystem_Projekt
För kursen Robot och Robotsystem HT25

+ Andreas Lindblad
+ Linnea Sundvall
+ Ahmed Mohamed



# Examineringsuppgift – Robotprogrammering

## Uppgiftens mål

Roboten ska flytta produkter från högra plattformen till den vänstra genom en labyrint enligt följande sekvens:

1. Börja i **hempositionen** (ovanför högra plattformen).
2. **Plocka upp** en produkt från den **högra plattformen**.
3. **Gå igenom labyrinten**.
4. **Placera produkten** på den **vänstra plattformen**.
5. **Gå tillbaka** genom labyrinten.
6. Upprepa stegen för varje produkt.
7. När alla produkter är flyttade ska roboten **återvända till hempositionen**.

---

## Plattformar

* Varje plattform har **3 × 5 produkter**.
* Roboten ska arbeta systematiskt enligt förutbestämda positioner (pick/place).
* Ordningen i ramen (frame) är:

  ```
  pick[0], pick[1], pick[2], pick[0]
  place[0], place[1], place[2], place[0]
  ```

---

## Hastigheter och rörelseparametrar

| Situation            | Hastighet | Z-position | Kommentar                       |
| -------------------- | --------- | ---------- | ------------------------------- |
| Monitor speed        | 20        | –          | Övervakningsläge                |
| Gå genom labyrint    | 80        | 55         | Snabb rörelse, höjd över hinder |
| Plocka / Lämna       | 25        | –          | Precision krävs                 |
| Verktygsförskjutning | –         | +110       | I Z-axeln                       |

---

## Koordinater

### Högra plattformen – Pick

| Index   |       X |       Y |      Z |    Rx |      Ry |     Rz |
| :------ | ------: | ------: | -----: | ----: | ------: | -----: |
| pick[0] |  39.252 | 279.681 | 32.010 | 0.000 | 180.000 | -0.013 |
| pick[1] |  39.252 | 229.681 | 32.005 | 0.000 | 180.000 | -0.013 |
| pick[2] | -60.748 | 279.681 | 32.010 | 0.000 | 180.000 | -0.013 |

### Vänstra plattformen – Place

| Index    |       X |        Y |      Z |    Rx |      Ry |      Rz |
| :------- | ------: | -------: | -----: | ----: | ------: | ------: |
| place[0] |  13.745 | -189.407 | 32.000 | 0.000 | 180.000 | -89.840 |
| place[1] |  13.745 | -239.407 | 32.000 | 0.000 | 180.000 | -89.840 |
| place[2] | -86.255 | -189.407 | 32.000 | 0.000 | 180.000 | -89.840 |

---

## Förskjutning

* **Förskjutning:** `25 mm` i både **X** och **Y**.
