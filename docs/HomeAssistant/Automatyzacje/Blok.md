# Blok

Zarówno sekcja `Jeżeli` i `Wykonaj` posiadają własne elementy dodatkowe, nazywane **blokami**.   

**Bloki** umożliwiają tworzenie bardziej złożonych i elastycznych automatyzacji, pozwalając użytkownikowi decydować, **w jaki sposób** system ma oceniać warunki lub wykonywać akcje.

---

## Jeżeli

W sekcji `Jeżeli` dostępne są bloki odpowiadające klasycznym bramkom logicznym:

- **I** (*AND*) – *wszystkie* warunki muszą zostać spełnione
- **Lub** (*OR*) – *przynajmniej jeden* warunek musi być spełniony
- **Nie** (*NOT*) – odwraca wynik warunku (***negacja***)

Bloki te pozwalają łączyć warunki w dowolne, zagnieżdżone struktury logiczne.

!!! example "Przykład złożonej logiki"
    
    **(**A I B**)** Lub **(**C I Nie D**)**    
    Automatyzacja uruchomi się tylko wtedy, gdy spełniony zostanie **cały** pierwszy zestaw **lub** drugi zestaw warunków.

<img width="1026" height="433" alt="obraz" src="https://github.com/user-attachments/assets/540ee9fa-f561-4b30-a047-73a98d98b030" />

### Przykład

Poniżej przykład użycia bloku `LUB`/`OR` gdzie automatyzacja wykona akcję, jeśli spełniony będzie **którykolwiek** z zestawów warunków.

!!! quote ""

    Realizowana jest funkcja:   
    (*Switch1* **OFF** i *Przekaźnik 2* **ON**) LUB (*Wejście 2* **ON** i *Przekaźnik 2* **OFF**) 

<img width="900" alt="obraz" src="https://github.com/user-attachments/assets/554463e9-813e-4623-a22e-2b8dc7432c69" />

---

## Wykonaj

W sekcji `Wykonaj` dostępne są **bloki**, które kontrolują sposób wykonywania akcji, a nie logikę warunków:

<img width="1026" height="802" alt="obraz" src="https://github.com/user-attachments/assets/64dc7ce1-05e2-4fe4-88c6-3ed055294d30" />

### Przykład

Przykład użycia konstruktorów `Powtórzenie` oraz `Opóźnienie`:

!!! quote ""

    *Przekaźnik 1* i *Przekaźnik 2* zostaną przełączone **10 razy**, z **1-sekundowym opóźnieniem** pomiędzy kolejnymi przełączeniami.

<img width="900" alt="obraz" src="https://github.com/user-attachments/assets/52499549-b115-4230-be10-f011a1476519" />
