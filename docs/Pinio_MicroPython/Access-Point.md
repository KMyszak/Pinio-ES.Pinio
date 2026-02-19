# Access Point

Jeśli urządzenie napotka problem z połączeniem z siecią Wi-Fi lub brokerem **MQTT**, automatycznie uruchomi własny **webserver** w trybie *Access Point*.   
Stan ten sygnalizowany jest przez diodę statusową **STA**, która miga **dwukrotnie** co 2 sekundy.

Tryb *Access Point* umożliwia zmianę podstawowych ustawień bez konieczności podłączania urządzenia przez USB - wystarczy połączyć się z jego siecią Wi-Fi:

- **SSID**: `Pinio_{MAC}`
- **Password**: `12345678`

!!! info ""

    Nazwę *Access Pointa* oraz hasło możesz zmienić w pliku ***webserver.py*** w funkcji ***start_ap()***:

    ```
    def start_ap():
        ap.active(False)
        sleep(0.5)
        ap.active(True)
        sleep(0.5)
        mac = hexlify(ap.config('mac')).decode()
        
        essid = f"Pinio_{mac[-6:].upper()}"    ← nazwa Access Pointa
        password = "12345678"                  ← hasło Access Pointa
        ap.config(essid=essid, password=password)
    ```

---

## Łącznie z Access Pointem 

1. Połącz się z siecią Wi-Fi o nazwie **Pinio_{MAC}**   
    Zgodnie z wartościami ustawionymi w `webserver.py`.
2. W przeglądarce wpisz adres `192.168.4.1`:    

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/40c5685c-89e5-4e63-8395-9ac33e414e91" />

3. Wprowadź potrzebne zmiany
4. Kliknij **SAVE**, aby zapisać konfigurację:

    <img width="150" height="110" alt="obraz" src="https://github.com/user-attachments/assets/b7c1a4a7-b0f6-4c38-a43d-be990c718fd9" />

5. Aby zastosować nowe ustawienia kliknij **RESTART** i potwierdź:

    <img width="293" height="110" alt="obraz" src="https://github.com/user-attachments/assets/dc2c6266-413d-484f-b6cd-8909774ae34b" />

6. Urządzenie zrestartuje się i uruchomi z nowymi ustawieniami:

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/2943b70b-18b3-4321-8537-18b2f3729391" />


!!! info "Timeout"

    Jeśli urządzenie nie zostanie skonfigurowane w ciągu 3 minut, uruchomi się ponownie.   
    Wartość tę można zmienić w pliku *webserver.py*.

!!! failure "Dalsze problemy z połączeniem"

    Jeśli po zmianach i restarcie urządzenie nadal nie łączy sie z **MQTT** sprawdź poprawność danych [**użytkownika**](../MQTT/Tworzenie-uzytkownika.md) oraz konfiguracji [**MQTT**](../MQTT/Integracja.md) w **Home Assistant**.


