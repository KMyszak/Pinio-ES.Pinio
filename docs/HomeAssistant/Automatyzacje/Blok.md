# Blok

Zarówno `Jeżeli` i `Wykonaj` posiadają własne elementy dodatkowe zwane **blokami**.

---

## Jeżeli

W sekcji `Jeżeli` dostępne są dodatkowe funkcje działające jak bramki logiczne (AND, OR, NOT).  
Pozwalają one budować bardziej złożone warunki, na przykład:

!!! quote ""

    (warunek A i warunek B) LUB (warunek C)  
    (A AND B) OR (C AND NOT D)

<img width="1026" height="433" alt="obraz" src="https://github.com/user-attachments/assets/540ee9fa-f561-4b30-a047-73a98d98b030" />

### Przykład

Zastosowanie konstruktora `LUB/OR`:

!!! quote ""

    Realizowana jest funkcja [Switch1 **OFF** i Przekaźnik 2 **ON**] LUB [Wejście 2 **ON** i Przekaźnik 2 **OFF**]: 

<img width="900" alt="obraz" src="https://github.com/user-attachments/assets/554463e9-813e-4623-a22e-2b8dc7432c69" />

---

## Wykonaj

W sekcji `Wykonaj` dostępne są funkcje, które umożliwiają modyfikowanie sposobu wykonywania akcji - takie jak **opóźnienia**, **powtórzenia** czy **sekwencje**:

<img width="1026" height="802" alt="obraz" src="https://github.com/user-attachments/assets/64dc7ce1-05e2-4fe4-88c6-3ed055294d30" />

### Przykład

Przykład użycia konstruktorów `Powtórzenie` oraz `Opóźnienie`:

!!! quote ""

    Przekaźniki 1 i 2 w urządzeniu Pinio zostają przełączone **10 razy**, z **jednosekundową przerwą** pomiędzy przełączeniami.

<img width="900" alt="obraz" src="https://github.com/user-attachments/assets/52499549-b115-4230-be10-f011a1476519" />
