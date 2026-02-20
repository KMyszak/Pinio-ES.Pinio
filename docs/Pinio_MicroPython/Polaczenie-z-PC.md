# Połączenie z komputerem

**Raspberry Pi Pico 2W** łączy się z komputerem za pomocą standardowego kabla micro‑USB, który **musi obsługiwać transmisję danych** (nie może to być wyłącznie kabel zasilający).   
Do odczytu, edycji oraz wgrywania plików na płytkę zalecane jest użycie środowiska [**Thonny IDE :material-open-in-new:**](https://thonny.org/).

---

1. Uruchom program **Thonny**
2. Podłącz **Pinio** do komputera przez kabel micro-USB
3. Kliknij w prawym dolnym rogu okna i wybierz z listy właściwe urządzenie: 

    <img width="344" height="104" alt="k_pinio_1" src="https://github.com/user-attachments/assets/6f237c7e-1fa1-431e-82ff-e6769c3e67df" />

4. W eksploratorze plików po lewej stronie znajdź i otwórz `config.py`:    

    <img width="204" height="460" alt="obraz" src="https://github.com/user-attachments/assets/85e848cf-6c22-4672-a750-b3ab805dce20" />
  
    !!! Failure "Brak plików"
    
        Jeśli nie widzisz żadnych plików, kliknij ikonę 🛑 lub wybierz opcję z menu *Run* → *Stop/Restart backend*:

        <img width="443" height="76" alt="obraz" src="https://github.com/user-attachments/assets/ba95bfcc-6982-4c98-aed1-ca798240fff1" />

5. Przejdź do sekcji [**Edycja config.py**](Edycja-config.md)