d# 🐧 Linux na Windows – všetky možnosti

Tento repozitár obsahuje prehľad rôznych spôsobov, ako používať Linux na Windows – od jednoduchých riešení pre začiatočníkov až po pokročilé nástroje pre developerov.

---

## 🔹 1. WSL (Windows Subsystem for Linux)

### Popis:

WSL umožňuje spúšťať Linux priamo vo Windows bez potreby virtuálneho stroja.

### Inštalácia:

```bash
wsl --install
```

### Výhody:

* Rýchle a jednoduché
* Nízka spotreba výkonu
* Ideálne na programovanie

### Nevýhody:

* Obmedzené GUI

---

## 🔹 2. Virtuálny stroj (VirtualBox / VMware)

### Popis:

Linux beží ako samostatný systém vo virtuálnom prostredí.

### Výhody:

* Plnohodnotný Linux (GUI)
* Bez zásahu do hlavného systému

### Nevýhody:

* Vyššia spotreba RAM a CPU
* Pomalšie

---

## 🔹 3. Dual Boot

### Popis:

Pri štarte počítača si vyberáš medzi Windows a Linux.

### Výhody:

* Maximálny výkon
* Plný Linux systém

### Nevýhody:

* Zložitejšia inštalácia
* Riziko pri práci s diskami

---

## 🔹 4. Live USB

### Popis:

Linux spustíš z USB bez inštalácie.

### Výhody:

* Bezpečné testovanie
* Žiadne zmeny na disku

### Nevýhody:

* Pomalšie
* Dočasné riešenie

---

## 🔹 5. Docker

### Popis:

Spúšťanie Linux prostredí pomocou kontajnerov.

### Príklad:

```bash
docker run -it ubuntu bash
```

### Výhody:

* Veľmi rýchle
* Ideálne pre DevOps

### Nevýhody:

* Nie je to plný OS

---

## 🔹 6. Cloud Linux (AWS, GCP)

### Popis:

Linux beží na vzdialenom serveri v cloude.

### Výhody:

* Vysoký výkon
* Prístup odkiaľkoľvek

### Nevýhody:

* Vyžaduje internet
* Môže byť platené

---

## 🔹 7. Remote Linux (SSH, RDP)

### Popis:

Pripojenie k inému Linux počítaču na diaľku.

### Výhody:

* Nepotrebuješ výkonný PC
* Reálny Linux systém

---

## 🔹 8. Cygwin / MinGW

### Popis:

Unix-like prostredie vo Windows.

### Výhody:

* Jednoduché
* Rýchle

### Nevýhody:

* Nie je to skutočný Linux

---

## 🔹 9. MSYS2

### Popis:

Moderné vývojové prostredie s balíčkovacím systémom.

### Výhody:

* Pacman (ako Arch Linux)
* Veľa nástrojov pre developerov

---

## 🔹 10. Linux v prehliadači

### Popis:

Linux spustený online bez inštalácie.

Stačí otvoriť prehliadač a počkať chvíľu

Pomalý ale za to jedoduchý postup
### Výhody:

* Okamžité použitie
* Bez inštalácie

### Nevýhody:

* Pomalé
* Limitované

### Príklad:
JSLinux
---

## 🔹 11. OpenSSH (Windows terminál)

### Popis:

Používanie Linux príkazov a pripojenie na servery cez SSH.

### Výhody:

* Jednoduché
* Už súčasť Windows

---

## 🧠 Odporúčania

| Použitie      | Odporúčanie                |
| ------------- | -------------------------- |
| Začiatočník   | WSL                        |
| Programovanie | WSL + Docker               |
| Plný Linux    | VirtualBox alebo Dual Boot |
| Testovanie    | Live USB                   |
| Server        | Cloud                      |

---

## 📌 Záver

Čo by som ja odproúčal je obyčajný emulátor v prehliadači:

* učenie Linuxu
* programovanie
* základy
* experimentovanie

---

