# 42-Snowcrash

Projet introductif à la sécurité en informatique, Snow Crash a pour but de faire découvrir la sécurité dans différents sous-domaines, avec une approche orientée développeur. Vous allez vous familiariser avec plusieurs langages (ASM/perl/php..), développer une certaine logique pour comprendre des programmes inconnus, et ainsi prendre conscience des problèmes liés à de simples erreurs de programmation

> The project ressources (ISO and subject) are avaible at the 42 school. This project is composed of 14 levels, each one contains a security breach that gives you access to the next level.

## Resources

### Used exploits

- **Return-to-libc** (replacing the RET addr in stack)
- **Buffer overflows** with unsecure `gets`, `strcat` and `strcpy`
- **Format string attacks**
- Exploits in binaries behaviour
- Bad use of casted values

### Programs

- `r2`: disassembly ([doc](https://radare.gitbooks.io/radare2book/visual_mode/intro.html))
- `gdb`: runtime debugging and disassembly
- `readelf`
- `ltrace`
- `python` scripting
- `John the ripper`
- `wireshark`, `tshark`
- others: `netstat`, `top`, `getfacl`, `ltrace`, `strace`

### Skills

Doing this project I learned about:

- Analysing binaries
- Injecting code using unprotected inputs/parameters
- Usecure system calls such as `access`

---

⚠️ ⚠️ ⚠️ ⚠️ ⚠️ ⚠️ ⚠️ ⚠️ ⚠️ ⚠️

    level00 : Déchiffrage code caesar
    level01 : /etc/passwd attack - John The Ripper
    level02 : Analyse de flux TCP sur un fichier pcap - Wireshark
    level03 : Modification du PATH - binaire appel 'system'
    level04 : Exploit script perl
    level05 : cron execute tous les binaires d'un dossier
    level06 : Faille modifier "e" des REGEX php
    level07 : Injection par une varible d'environnement
    level08 : Bypass d'un check dans le code par un lien symbolique
    level09 : Reverse de hash
    level10 : Race condition entre access et open
    level11 : Faille via io.popen dans un script lua
    level12 : Faille via un subshell dans un script perl
    level13 : Modifier valeur de retour d;une fonction avec GDB
    level14 : Exploiter getflag
