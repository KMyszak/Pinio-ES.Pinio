# Tryby automatyzacji

Automatyzacje pozwalają uruchamiać wiele akcji jednocześnie, a ich zachowanie zależy od wybranego **trybu pracy**. **Domyślnie** aktywny jest tryb `Pojedynczy`.  

---

## Dostępne tryby

- **Pojedynczy** - kolejne wywołanie **nie rozpocznie** nowej automatyzacji, a system wygeneruje ostrzeżenie  
- **Uruchom ponownie** - zatrzymuje poprzednią instancję i natychmiast uruchamia automatyzację od nowa  
- **Kolejkowanie** - każde wywołanie trafia do kolejki i zostanie uruchomione dopiero po zakończeniu poprzednich   
- **Równoległy** - każde wywołanie uruchamia nową instancję automatyzacji, działającą równolegle z pozostałymi  

!!! info "Schemat działania trybów"

    <img width="545" height="319" alt="obraz" src="https://github.com/user-attachments/assets/9feb29d7-fccc-4a66-ae4a-43c807d71792" />

---

## Limity uruchmień

W trybach `Kolejkowanie` i `Równoległy` parametr **Długość kolejki** / **Maksymalna liczba równoległych uruchomień** określa maksymalną liczbę instancji automatyzacji, które mogą być jednocześnie uruchomione lub oczekiwać w kolejce (domyślnie 10).

Po przekroczeniu limitu system zapisze wpis w logach, informujący o zbyt dużej liczbie wywołań.   

---

## Zmiana trybu

1. Przejdź do:  
    `Ustawienia → Automatyzacje oraz sceny`

2. Wybierz `Automatyzacje` z górnej belki:

    <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/3d19432f-94c8-431a-ac91-af8af0459b75" />

3. Wybierz docelową automatyzację i z rozwijanego menu **`⋮`** wybierz `Zmień tryb`:

    <img width="170" alt="obraz" src="https://github.com/user-attachments/assets/e37632b6-d0db-4dc4-abfb-8d0c01860213" />

4. Wybierz tryb i zatwierdź klikając **Zmień tryb**:

    <img width="350" alt="obraz" src="https://github.com/user-attachments/assets/2191413a-85c3-4de8-9a01-51c550509a73" />