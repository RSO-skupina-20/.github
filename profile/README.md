# Tehnična dokumentacija: Sistem za upravljanje dogodkov

## 1. Opis projekta
Organizacija večjih dogodkov je zahteven proces, ki vključuje iskanje prostih prostorov, usklajevanje urnikov in obveščanje udeležencev. Tradicionalni pristopi pogosto vodijo v zmedo in napake. Da bi to odpravili, smo razvili oblačno aplikacijo za avtomatizacijo in centralizacijo procesov načrtovanja ter upravljanja dogodkov. 

### Ključne funkcionalnosti
- **Za uporabnike:** Pregled razpoložljivih prostorov, ustvarjanje dogodkov, urejanje agend, obveščanje gostov.
- **Za lastnike prostorov:** Upravljanje razpoložljivih prostorov.
- **Prednosti:** Povečana produktivnost, zmanjšanje zmede, poenostavljen proces organizacije dogodkov.

---

## 2. Ogrodja in razvojno okolje
Za razvoj uporabljamo naslednje tehnologije:
- **Zaledje:** JavaEE z ogrodjem KumuluzEE
- **Podatkovna baza:** PostgreSQL
- **Kontejnerizacija:** Docker
- **Orkestracija:** Kubernetes
- **Gostovanje:** Microsoft Azure 
- **Razvojno okolje:** IntelliJ IDEA
- **Testiranje in sodelovanje:** Postman in GitHub

---

## 3. Arhitektura sistema
Aplikacija je razdeljena na štiri mikrostoritve, ki bodo komunicirale prek protokolov REST in gRPC. Shema arhitekture vključuje:
- **Ločene baze za vsako mikrostoritev.**
- **API vmesnike za komunikacijo med mikrostoritvami.**
- **DTO in entitete za prenos in prilagoditev podatkov.**
- **Zrna in izjeme za obdelavo podatkov znotraj storitev.**

---

## 4. Prenos podatkov
- **Entitete:** Dostop do podatkovne baze.
- **DTO (Data Transfer Objects):** Prilagoditev in obdelava podatkov za API-je.
- **API in storitve:** Upravljanje podatkovne logike in komunikacije z drugimi mikrostoritvami.
- **Kafka:** Za prenos email sporočila med 2 mikrostoritvama
