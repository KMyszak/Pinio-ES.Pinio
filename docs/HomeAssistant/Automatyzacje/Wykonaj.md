# Wykonaj 

W tym miejscu znajdują się wszystkie `akcje`, które zostaną wykonane po spełnieniu wyzwalacza z sekcji `Kiedy` oraz - *jeśli zostały zdefiniowane* - wszystkich `warunków` z sekcji `Jeżeli`.

!!! tip ""

    [Dowiedz się więcej na temat warunków :material-open-in-new:](https://www.home-assistant.io/docs/automation/condition/)

---

## Przykład

Poniższy przykład demonstruje wykorzystanie **Elementu konstrukcyjnego** - `Powtórz`, aby wykonać akcje wielokrotnie.

Automatyzacja wykona:

- **10-krotne** przełączenie *RELAY 1* (Przekaźnik 1) oraz *RELAY 2* (Przekaźnik 2)
- z **1-sekundowym opóźnieniem** między kolejnymi cyklami

Powtórzenie (ilość przebiegów) oraz opóźnienie są zdefiniowane wewnątrz elementu `Powtórz`, dzięki czemu całość wykonuje się w pełnej pętli:

<img width="800" alt="obraz" src="https://github.com/user-attachments/assets/b92b78d8-33e9-4791-b09a-fd1ffe9f15b2" />
