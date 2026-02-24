# Integracja

Integracja w aplikacji **MQTT** pozwala na połączenie urządzeń z brokerem oraz umożliwia wymianę danych w czasie rzeczywistym. Po dodaniu urządzeń do aplikacji możliwe jest monitorowanie ich stanu, odbiór komunikatów i sterowanie funkcjami urządzeń bezpośrednio z panelu aplikacji. 

Integracja zapewnia spójny przepływ danych między urządzeniami a systemem, a także ułatwia zarządzanie połączeniami **MQTT** w ramach całego środowiska.

---

1. Przejdź na stronę swojego **Home Assistant** (np. *haos.app*)
2. Z menu po lewej stronie wybierz:   
    `Ustawienia → Urządzenia oraz usługi`   
3. Znajdź panel MQTT:

    <img width="281" height="127" alt="obraz" src="https://github.com/user-attachments/assets/4a1ff8f3-be19-40ef-9c28-b40060710f83" />

4. Kliknij ikonę zębatki, następnie `SKONFIGURUJ OPCJE MQTT`:
    
    <img width="719" alt="obraz" src="https://github.com/user-attachments/assets/8e8241fb-2214-42c7-af37-e49248cc0d08" />

5. Uzupełnij pola zmiennymi:  

    !!! info "Zmienne"
        
        W przypadku urządzenia **Pinio z MicroPython** użyj danych z [`config.py`](../Pinio_MicroPython/Edycja-config.md) lub `config.json`, jeśli wcześniej zostały zmienione

    !!! example "Przykładowe ustawienia" 

        <img width="904" height="497" alt="obraz" src="https://github.com/user-attachments/assets/33b0d95d-8fed-4682-b11b-55bc6b491603" />

6. Zapisz konfigurację - jeżeli ustawienia MQTT są identyczne jak w [`config.py`](../Pinio_MicroPython/Edycja-config.md), dodatek automatycznie wykryje urządzenie (jeśli nie zostało wykryte przejdź do [**FAQ**](../FAQ/Pinio-ESPHome.md)):

    <img width="719" alt="obraz" src="https://github.com/user-attachments/assets/cc823a2f-e7e4-4948-a407-6aec2474eca4" />

    !!! info "Dodatkowe ustawienia"

        W panelu dostępna jest zmiana nazwy urządzenia, dodania go do obszaru i zmianę etykiety - kliknij ikonę ołówka. Warto zmienić nazwę teraz, aby uniknąć późniejszych problemów z powodu zmienionych identyfikatorów encji.  
