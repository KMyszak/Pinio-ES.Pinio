# Zmiana nazwy

Nazwę urządzenia można zmienić bezpośrednio w interfejsie **Home Assistant**.   
Zmiana jest natychmiastowa i automatycznie aktualizuje powiązane encje.

---

## Zmiana przez Home Assistant

1. Przejdź na stronę swojego **Home Assistant** (*haos.app*)
2. Z menu po lewej stronie wybierz:  
    `Ustawienia → Urządzenia oraz usługi → MQTT`

    <img width="263" height="114" alt="obraz" src="https://github.com/user-attachments/assets/28d608bc-524d-490b-b462-616fc66fe16a" />

3. W sekcji **Urządzenia** wybierz moduł, któremu chcesz zmienić nazwę, a następnie kliknij ikonę ołówka - **Edytuj urządzenie**:

    <img width="800" alt="obraz" src="https://github.com/user-attachments/assets/e6e5eb3d-3cba-4529-a6e9-93941933e57b" />

4. Wprowadź nową nazwę i kliknij **Aktualizuj**:

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/fcec8b07-30bb-4a42-bac9-e3fe5ee12115" />

    !!! info "Dodatkowe opcje"

        Możesz również przypisać urządzenie do **Obszaru** oraz nadać mu **Etykiety**, co ułatwia organizację w większych instalacjach.

## Zmiana przez plik

Nazwę można również zmienić bezpośrednio w pliku konfiguracyjnym na urządzeniu **Pinio** (*wersja MicroPython*).  
Zmiana ta zostanie uwzględniona dopiero po **ponownej inicjalizacji** integracji.

1. Uruchom program **Thonny**
2. Podłącz **Pinio** do komputera przez kabel micro-USB
3. Kliknij w prawym dolnym rogu okna i wybierz z listy właściwe urządzenie:

    <img width="344" height="104" alt="k_pinio_1" src="https://github.com/user-attachments/assets/6f237c7e-1fa1-431e-82ff-e6769c3e67df" />

4. W eksploratorze plików po lewej stronie znajdź  i otwórz`mqtt_creator.py`:  

    <img width="220" height="455" alt="obraz" src="https://github.com/user-attachments/assets/27b743a7-67fd-4c60-a5c9-31f4fc3a8fa5" />

    !!! Failure "Brak plików"

        Jeśli nie widzisz żadnych plików, kliknij ikonę 🛑 lub wybierz opcję z menu *Run* → *Stop/Restart backend*:
        
        <img width="443" height="76" alt="obraz" src="https://github.com/user-attachments/assets/ba95bfcc-6982-4c98-aed1-ca798240fff1" />


5. W funkcji `create_mqtt_discovery()` zmień wartość `"name"` w słowniku `device_info`:
```
def create_mqtt_discovery(mac, mqtt_client, action, roms):
        device_info = {
            "identifiers": [mac],
            "name": f"Device {mac.upper()}",    ← zmień nazwę
        }
```

6. Usuń `mac.conf` z plików, aby wymusić ponowną inicjalizację **MQTT**:

    <img width="220" height="455" alt="obraz" src="https://github.com/user-attachments/assets/df66ed59-a861-43e3-b71c-cf492bdbd232" />


