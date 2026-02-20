# Tryby automatyzacji

Automatyzacje mogą uruchamiać wiele akcji jednocześnie, a sposób ich działania zależy od wybranego trybu pracy.  
Domyślnie używany jest tryb `Pojedynczy`.  

---

## Dostępne tryby

- **Pojedynczy** - tylko jedna instancja automatyzacji może działać w danym momencie
- **Uruchom ponownie** - nowe wywołanie natychmiast przerwie poprzednią instancję i zacznie automatyzację od początku
- **Kolejkowanie** - każde wywołanie trafia do kolejki i uruchamia się dopiero po zakończeniu poprzedniego   
- **Równoległy** - każde wyzwolenie tworzy oddzielną instancję, działającą jednocześnie z pozostałymi  

!!! note "Schemat działania trybów"

    <div style="text-align:center;">
        <img width="720" height="444" alt="obraz" src="https://github.com/user-attachments/assets/986e66ec-2c63-4458-8f10-6431a5db0092" />
    </div>

## Limity uruchomień

W trybach `Kolejkowanie` i `Równoległy` parametr **Długość kolejki** / **Maksymalna liczba równoległych uruchomień** określa maksymalną liczbę instancji automatyzacji, które mogą być jednocześnie uruchomione lub oczekiwać w kolejce (domyślnie: **10**).

Gdy limit zostanie przekroczony:

- nowe wywołania **nie zostaną dodane** do kolejki ani uruchomione
- w logach pojawi się wpis informujący o **zbyt dużej liczbie aktywnych instancji** 

## Zmiana trybu

1. Przejdź do:  
    `Ustawienia → Automatyzacje oraz sceny`

2. Wybierz zakładkę`Automatyzacje` z górnej belki:

    <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/3d19432f-94c8-431a-ac91-af8af0459b75" />

3. Otwóz wybraną automatyzację i z menu **`⋮`** wybierz opcję `Zmień tryb`:

    <img width="170" alt="obraz" src="https://github.com/user-attachments/assets/e37632b6-d0db-4dc4-abfb-8d0c01860213" />

4. Wybierz odpowiedni tryb i zatwierdź klikając **Zmień tryb**:

    <img width="350" alt="obraz" src="https://github.com/user-attachments/assets/2191413a-85c3-4de8-9a01-51c550509a73" />