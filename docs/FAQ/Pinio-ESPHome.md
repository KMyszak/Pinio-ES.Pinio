### Urządzenie nie reaguje lub robi to z opóznieniem

Problemy mogą być spowodowane ustawieniami **routera** lub **Access Pointa** do którego podłączone jest urządzenie.  

**Raspberry Pi Pico W** korzysta z układu Wi-Fi, który:

- wspiera tylko podstawowe Wi-Fi (802.11b/g/n) w paśmie 2.4 GHz 
- nie dokumentuje wsparcia dla:
    - 802.11r - fast roamingu
    - 802.11k - wspomagania w roamingu
    - 802.11v - kierowania klienta przez AP
- obsługuje wyłącznie WPA2-PSK

Aby **zapobiegać** problemom z połączeniem:

- unikaj odległych AP
- wyłącz *AP Isolation* (izolację klientów)
- unikaj zbyt dynamicznych meshy Wi-Fi
- zaleca się aby wszystkie AP miały ten sam SSID, hasło, szyfrowanie i kanały blisko siebie (np. 1, 6, 11)
- jeśli jest możliwość zadbaj o to, aby sieć była niepodzielona - tylko 2.4 GHz
- używaj stałego kanału Wi-Fi

### Wygasła autoryzacja

Jeżeli pojawi się powiadomienie w `Ustawienia`:  

<img width="315" height="78" alt="obraz" src="https://github.com/user-attachments/assets/1550c43a-a2c5-404e-8e8c-fac1b2a7d5b0" />

należy jeszcze raz wprowadzić klucz szyfrujący. Aby pobrać klucz:

1. Z menu po lewej stronie wybierz `ESPHome builder` 
2. Z rozwijanego menu dla urządzenia wybierz **Show API Key**:

    <img width="564" height="238" alt="obraz" src="https://github.com/user-attachments/assets/289e4dd1-7d14-4dba-945f-89f1463b5c01" />

3. Skopiuj klucz

    !!! warning "Klucz na urządzeniu musi się pokrywać z tym w ESPHome builder"

4. Wróć do `Ustawienia` i kliknij na powiadomienie
5. Wklej skopiowany klucz i **ZATWIERDŹ**:

    <img width="457" height="232" alt="obraz" src="https://github.com/user-attachments/assets/87bb3dd4-93d3-488f-8ce6-37215dd385c2" />

    !!! failure "Nieprawidłowy klucz" 
    
        Jeżeli skopiowany klucz jest nieprawidłowy pozostaje zainstalowanie aktualnej konfiguracji .YAML w **ESPHome builder** na urządzenie (najlepiej manualnie) lub konfiguracja całości [**od nowa**](../Pinio_ESPHome/Pierwsza-konfiguracja-ESPHome.md).
