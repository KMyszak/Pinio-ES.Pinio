# Access Point

Jeśli urządzenie napotka problem z połączeniem z siecią Wi-Fi lub brokerem **MQTT**, automatycznie uruchomi własny **webserver** w trybie Access Point - dioda statusowa STA migająca **dwa razy** co 2 sekundy.  

Umożliwia on zmianę podstawowych ustawień bez konieczności fizycznego połączenia z urządzeniem - przez połączenie z AP (korzystając z Wi-Fi):  

```
   SSID = Pinio_{MAC}      # Nazwa utworzonego Access Pointa (MAC urządzenia)
   password = 12345678     # Hasło do logowania
```
!!! info ""

    Obie zmienne można zmienić w pliku `webserver.py` w funkcji `start_ap()`:

    ```
    ∙∙∙
    def start_ap():
        ap.active(False)
        sleep(0.5)
        ap.active(True)
        sleep(0.5)
        mac = hexlify(ap.config('mac')).decode()
        
        essid = f"Pinio_{mac[-6:].upper()}"    ← nazwa Access Pointa
        password = "12345678"                  ← hasło Access Pointa
        ap.config(essid=essid, password=password)
    ∙∙∙
    ```

---

## Łącznie z Access Pointem 

1. Połącz się z siecią Wi-Fi o nazwie **Pinio_{MAC}** (SSID i hasło z pliku `webserver.py`)
2. W przeglądarce wpisz adres `192.168.4.1`:    

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/40c5685c-89e5-4e63-8395-9ac33e414e91" />

3. Wprowadź odpowiednie zmiany
4. Kliknij przycisk **SAVE**, aby je zapisać:

    <img width="150" height="110" alt="obraz" src="https://github.com/user-attachments/assets/b7c1a4a7-b0f6-4c38-a43d-be990c718fd9" />

5. Aby zastosować nowe ustawienia kliknij **RESTART** i zatwierdź:

    <img width="293" height="110" alt="obraz" src="https://github.com/user-attachments/assets/dc2c6266-413d-484f-b6cd-8909774ae34b" />

6. Urządzenie się zrestartuje i uruchomi ze zmienionymi ustawieniami:

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/2943b70b-18b3-4321-8537-18b2f3729391" />


!!! info "Jeśli nie nastąpi połączenie z urządzeniem, zresetuje się ono po 3 minutach (wartość można zmienić w module *webserver.py*)"

!!! failure "Jeśli po zmianach i restarcie urządzenie dalej poprawnie nie łączy sie z MQTT sprawdź poprawność zmiennych z danymi [użytkownika](../MQTT/Tworzenie-uzytkownika.md) i [MQTT](../MQTT/Integracja.md)"


