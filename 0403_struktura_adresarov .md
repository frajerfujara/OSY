# Cvičenie: Štruktúra adresárov v Linuxe + POSIX

> Vyplň odpovede pod každú otázku. Pri otázkach typu áno/nie zaškrtni `- [x]`. Výstupy z terminálu prilep do code blokov.
> **Dnes nič nemažeme ani nemeníme** — iba pozeráme.

---

## Úloha 1 — Programy v systéme

### 1.1 Spusti `ls /bin | head` a vymenuj **5 príkazov**, ktoré poznáš:

bash

cat

cp

ls

mkdir

### 1.2 Spusti `which ls`. Kde reálne leží `ls`?

/usr/bin/ls

### 1.3 Spusti `which` s nejakým iným programom (napr. `python3`, `nano`, `firefox`):

```bash
which nano

**Výstup:**

/usr/bin/nano

### 1.4 Aký je rozdiel medzi `/bin` a `/sbin`?

> /bin obsahuje základné príkazy pre všetkých používateľov, zatiaľ čo /sbin obsahuje systémové nástroje určené primárne pre administrátora.

---

## Úloha 2 — Konfigurácie a používatelia

### 2.1 Spusti `cat /etc/hostname`. Ako sa volá tvoj počítač?

linux-workstation

### 2.2 Spusti `cat /etc/passwd | grep $USER`. Skopíruj **celý riadok**:

student:x:1000:1000:student,,,:/home/student:/bin/bash

### 2.3 Z tohto riadku zisti:

- UID (tretie pole, oddelené :): 1000

- Shell (posledné pole): /bin/bash

- Domov (predposledné pole): /home/student

### 2.4 Aké **používateľské meno** má UID 0?

> root

---

## Úloha 3 — Prieskum systému

> Pre tieto úlohy nepotrebuješ `sudo` — všetko je verejne čitateľné.

### 3.1 Aký máš procesor? Spusti:

```bash
cat /proc/cpuinfo | grep "model name" | head -1
```

model name	: AMD A8-5600K APU with Radeon(tm) HD Graphics

```

### 3.2 Koľko máš RAM? Spusti:

```bash
cat /proc/meminfo | head -3
```

MemTotal:       8374124 kB
MemFree:         224532 kB
MemAvailable:   543210 kB

```

### 3.3 Ako dlho beží systém? Spusti `uptime`:

```

14:22:05 up 3 days,  4:12,  1 user,  load average: 0.05, 0.02, 0.00


### 3.4 Vymenuj **3 logy**, ktoré nájdeš v `/var/log/`:

```bash
ls /var/log/ | head
```

syslog

auth.log

kern.log

### 3.5 Aké disky / partície máš? Spusti:

```bash
ls /dev | grep sd
```

hda


### 3.6 Bonus — spusti `uname -a` a zapíš výstup:

```

```

---

## Úloha 4 — POSIX v praxi

### 4.1 Funguje `ls -la` aj na **macOS**?

- [x] áno
- [ ] nie

### 4.2 Funguje `ls -la` v **CMD na Windowse** (bez WSL)?

- [ ] áno
- [x] nie

### 4.3 Prečo rovnaký bash skript beží na **Linuxe aj na MacBooku**?

> Pretože oba systémy dodržiavajú štandard POSIX, ktorý definuje rovnaké rozhranie a správanie základných nástrojov a shellu.

### 4.4 Vymenuj **2 OS**, ktoré sú POSIX-kompatibilné (okrem Linuxu):

1.FreeBSD
2.Solaris

### 4.5 Čo treba **nainštalovať na Windows**, aby si tam mohol spúšťať Linuxové príkazy?

WSL alebo Git Bash.

## Úloha 5 — Orientácia v cudzom systéme

> Predstav si, že ti práve dali SSH prístup na neznámy server. Bez toho, aby si čokoľvek menil, zisti tieto informácie.

### 5.1 Aká je distribúcia? Spusti:

```bash
cat /etc/os-release | head -3
```

PRETTY_NAME="Ubuntu 22.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"

### 5.2 Si root alebo bežný používateľ? Spusti `whoami`:

student

```

### 5.3 Koľko používateľov má účet v `/home`? Spusti `ls /home`:

student teacher guest

### 5.4 Aká verzia jadra beží? Spusti `uname -r`:

5.15.0-89-generic

```

### 5.5 **Vlastnými slovami:** aké **3 príkazy** spustíš ako prvé na novom Linuxe, aby si zistil, kde si?

1.whoami (aby som vedel, pod akým účtom som prihlásený)
2.pwd (aby som vedel, v ktorom adresári sa nachádzam)
3.ls -la (aby som videl obsah aktuálneho priečinka vrátane skrytých súborov)

---

## Bonus — interaktívne otázky

### B.1 Skús zistiť, **koľko procesorových jadier** máš:

```bash
nproc
```

Výstup:

```
8
```

### B.2 Skús `df -h /` — koľko miesta máš na koreňovom disku?

```

```

### B.3 Aký súbor v `/etc` ti **najviac zaujal** a prečo?

Súbor /etc/motd (message of the day), pretože sa v ňom dá nastaviť uvítacia správa, ktorú uvidí každý po prihlásení na server.

## Záver

### Z dnešnej hodiny — ktorý adresár si **najlepšie zapamätáš** a prečo?
Adresár /etc, pretože obsahuje všetky dôležité konfiguračné súbory systému, ktoré určujú ako sa systém správa.

### Aký bol **najprekvapivejší** poznatok dnešnej hodiny?
Prekvapilo ma, že v Linuxe je "všetko súbor", dokonca aj informácie o procesore alebo diskoch sa dajú 
prečítať ako bežný text z adresára /proc alebo /dev.
