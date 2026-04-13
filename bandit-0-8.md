Bandit 0 → 1

Cel: Połączenie przez SSH i znalezienie hasła w pliku.

Połączenie:
ssh bandit0@bandit.labs.overthewire.org -p 2220
Rozwiązanie:
ls
cat readme
Bandit 1 → 2

Cel: Odczyt pliku o nazwie -

Rozwiązanie:
cat ./-
Bandit 2 → 3

Cel: Plik z nazwą zawierającą spacje

Rozwiązanie:
cat "spaces in this filename"
Bandit 3 → 4

Cel: Ukryty plik w katalogu

Rozwiązanie:
ls -a
cat .hidden
Bandit 4 → 5

Cel: Znalezienie pliku typu tekstowego

Rozwiązanie:
file ./*
cat ./file07
Bandit 5 → 6

Cel: Plik o określonych właściwościach (human-readable, ~1033 bytes)

Rozwiązanie:
find . -type f -size 1033c
cat ./maybehere07/.file2
Bandit 6 → 7

Cel: Znalezienie pliku w systemie spełniającego warunki (owner, size)

Rozwiązanie:
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
Bandit 7 → 8

Cel: Znalezienie hasła obok słowa „millionth”

Rozwiązanie:
grep "millionth" data.txt
Bandit 8 → 9

Cel: Znalezienie unikalnej linii (występuje tylko raz)

Rozwiązanie:
sort data.txt | uniq -u
