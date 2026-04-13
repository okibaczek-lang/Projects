# Bandit 0 → 9 (OverTheWire)

## Bandit 0 → 1
Cel: Połączenie przez SSH i znalezienie hasła w pliku.

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
```

## Bandit 1 → 2
Cel: Odczyt pliku o nazwie "-"

```bash
cat ./-
```

## Bandit 2 → 3
Cel: Plik z nazwą zawierającą spacje

```bash
cat "spaces in this filename"
```

## Bandit 3 → 4
Cel: Ukryty plik w katalogu

```bash
ls -a
cat .hidden
```

## Bandit 4 → 5
Cel: Znalezienie pliku tekstowego

```bash
ls -a
file ./*
cat ./-file07
```

## Bandit 5 → 6
Cel: Plik o określonym rozmiarze (~1033 bytes)

```bash
find . -type f -size 1033c
```

## Bandit 6 → 7
Cel: Znalezienie pliku w systemie (owner + size)

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```

## Bandit 7 → 8
Cel: Znalezienie hasła przy słowie "millionth"

```bash
grep "millionth" data.txt
```

## Bandit 8 → 9
Cel: Znalezienie unikalnej linii (występuje tylko raz)

```bash
sort data.txt | uniq -u
```
