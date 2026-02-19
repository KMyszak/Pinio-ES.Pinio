# Aktualizacja przez plik lokalny

Aktualizacja firmware może zostać przeprowadzona przy użyciu lokalnego pliku `.bin` pobranego wcześniej z oficjalnej strony **Tasmota**. Producent udostępnia różne warianty oprogramowania, w tym wersję **uniwersalną**, **minimalną** czy zoptymalizowaną pod **urządzenia z wyświetlaczem**.   

Wersja standardowa oferowana jest w wielu opcjach językowych, a w razie potrzeby dostępne są również wcześniejsze wydania.

## Wersja minimal

<img width="220" align="right" alt="obraz" src="https://github.com/user-attachments/assets/4b95e8dd-6578-4820-b68a-0f44ca2c95e3" />

Aby **zaktualizować** urządzenie z pliku lokalnego, musi ono mieć wgrany firmware w wersji `MINIMAL` - wynika to z ograniczonej pamięci dostępnej w urządzeniu.

Wersja `MINIMAL` zajmuje znacznie mniej miejsca niż docelowy firmware, dzięki czemu urządzenie jest w stanie przeprowadzić aktualizację w&nbsp;dwóch etapach.

<br>

!!! info "Funkcjonalność"
    
    Warto pamiętać, że *MINIMAL* **nie posiada pełnej funkcjonalności** - służy jedynie jako tymczasowy tryb umożliwiający aktualizację.   
    Po instalacji właściwego firmware, parametry i ustawienia urządzenia zostają zachowane.

## Instalacja

1. Pobierz wersję `MINIMAL`:

    !!! info "OTA" 
    
        Można ją również wgrać przez [OTA](Aktualizacja-przez-web-server.md) wklejając w miejsce **OTA Url**:  

        *http://ota.tasmota.com/tasmota/tasmota-minimal.bin.gz*

2. Połącz się z urządzeniem wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-przypisanego-ip-do-urzadzenia))
3. Przejdź do `Firmware Upgrade`:  
    <img width="292" height="479" alt="obraz" src="https://github.com/user-attachments/assets/f64de808-4432-4d9c-9289-acd0e9f9db5b" />

4. Wgraj wersję `MINIMAL firmware` wybierając plik w sekcji `Use file upload` i klikając **Start upgrade**:
    <img width="292" height="539" alt="obraz" src="https://github.com/user-attachments/assets/94b06f4b-64da-47dd-819c-90a16a7c63b6" />

5. Po poprawnym flashowaniu powinno pojawić się następujące okno:   
    <img width="292" height="361" alt="obraz" src="https://github.com/user-attachments/assets/1ec2419b-c090-44dd-8a8d-86aee908bcd8" />

6. Po restarcie przejdź ponownie do `Firmware Upgrade`:  
    <img width="292" height="329" alt="obraz" src="https://github.com/user-attachments/assets/0ab3d77b-6e8b-4e5d-89d2-dba93bc3c5c3" />

7. W sekcji `Use file upload` wybierz docelowy plik firmware i kliknij **Start upgrade**:   
    <img width="292" height="591" alt="obraz" src="https://github.com/user-attachments/assets/d0e01337-5901-42a6-a26e-99ab8ad847af" />

8. Po poprawnym flashowaniu powinny zostać załadowane **wszystkie** moduły:   
    <img width="292" height="467" alt="obraz" src="https://github.com/user-attachments/assets/499b7f31-972a-4c4e-aa10-b50569e4aa6c" />

!!! success "Aktualizacja zakończona"

    Urządzenie zostało pomyślnie zaktualizowane - widoczna w dolnej części okna wersja firmware powinna odpowiadać pobranej wersji.