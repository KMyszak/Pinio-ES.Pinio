# Aktywacja sceny

Aby korzystać ze stworzonych scen, należy utworzyć **automatyzację**.  
W przykładzie zostały wykorzystane dwie sceny bazujące na dostępnych encjach urządzenia (*RELAY 1* oraz *RELAY 2*):   

- **włączająca** oba przekaźniki urządzenia Pinio (*Przełączniki ON*)
- **wyłączająca** oba przekaźniki urządzenia Pinio (*Przełączniki OFF*) 

<img width="679" height="478" alt="obraz" src="https://github.com/user-attachments/assets/a9898bd1-ff14-458f-b82a-bfd872e3f02a" />

---

## Aktywacja

1. Przejdź na stronę swojego **Home Assistant** (np. *haos.app*)
2. Z paska bocznego wybierz:  
    `Ustawienia → Automatyzacje oraz sceny`
3. Wybierz `Automatyzacje` z górnej belki:
     <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/3d19432f-94c8-431a-ac91-af8af0459b75" />

4. W prawym dolnym rogu kliknij `+ Utwórz automatyzację`
5. Wybierz opcję **Utwórz nową automatyzację**

     <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/3bc81279-f569-4d68-aa6e-3d5a723ebfe8" />

6. Zapisz wprowadzone zmiany klikając **ZAPISZ**

---

## Przykład 

Aktywacja wejścia *IN 1* włącza scenę **Przełączniki ON** - *aktywuje* przekaźniki *RELAY 1* oraz *RELAY 2*   
Aktywacja wejścia *IN 2* włącza scenę **Przełączniki OFF** - *dezaktywuje* przekaźniki *RELAY 1* oraz *RELAY 2*

<img width="750" alt="obraz" src="https://github.com/user-attachments/assets/d966c30e-ccbe-4392-a413-249cb35fc31f" />