[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-7f7980b617ed060a017424585567c406b6ee15c891e84e1186181d67ecf80aa0.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=15228369)

# Klasa Stop

Zadaniem jest napisanie klasy `Stack` reprezentującej kontener typu stos. Stos jest rodzajem kontenera, na który można odkładać i z którego można pobierać tylko element będący na wierzchu.

## Interfejs publiczny

Klasa stosu powinna implementować następujące funkcje:

- `push(data)` - dodaj dane do stosu
- `pop(num: int|None = None)` - pobierz element ze stosu i go usuwa, jeśli `num > 0`, pobierz `num` elementów jako tuplę, gdzie pierwszy (wierzchni) element stosu jest pierwszym elementem tupli, przykład:
    Stos `s` zawiera elementy:
    ```text
    5 <-- góra stosu
    4
    3
    2
    1
    0
    ```
    zatem:
    ```py
    s.pop(3) == (5, 4, 3)
    ```
- `get(num: int|None = None)` - tak samo jak `pop()` ale pobiera tylko wartości bez usuwania

Oprócz tego klasa powinna implementować funkcje pomocnicze:
- `__len__()`
- `__str__()`
- `__repr__()`

## Konstruktor klasy

Konstruktor powinien przyjmować opcjonalny argument określający typ akceptowanych danych.

1. Jeśli argument nie jest użyty lub jest `None`, stos akceptuje wszystkie typy.
1. Jeśli argument jest typem, stos powinien akceptować tylko dany typ. Funkcja `push` powinna rzucić wyjątek `TypeError` jeśli typ jest błędny.
1. Jeśli argument jest wartością, stos powinien akceptować tylko typ tej wartości. Funkcja `push` powinna rzucić wyjątek `TypeError` jeśli typ jest błędny.

## Dodatkowe

Zarówno klasa jak i i metody klasy powinny posiadać `docstring`.