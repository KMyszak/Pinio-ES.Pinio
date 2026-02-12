# Kilka czujników 1-Wire

Jeśli chcesz korzystać z więcej niż jednego czujnika (tego **SAMEGO** typu np. DS18B20), musisz znać ich adresy. 

1. Podłącz urządzenie do komputera
2. Wybierz na pasku bocznym **ESPHome Builder**:  

    <img width="209" height="98" alt="obraz" src="https://github.com/user-attachments/assets/f078b6cd-35d3-4da9-b244-fdfed223b755" />

3. Przejdź do logów klikając **LOGS**:  

    <img width="403" height="121" alt="obraz" src="https://github.com/user-attachments/assets/040d4be4-e6d8-4913-bd42-ceb8f89de4fa" />

4. Obserwuj dane wyjściowe:

    <img width="700" height="90" alt="obraz" src="https://github.com/user-attachments/assets/24b48e1e-d02e-4dd8-8063-615d52985a1d" />

    !!! success "Wykryte czujniki"

        ESPHome wykryło podłączone dwa czujniki temperatury (DS18B20)  
        
        Każdy z nich ma swój unikalny adres hex (0x...)

5. Zapisz adresy i zamknij konsolę
6. Dodaj czujniki do kodu `.YAML` przechodząc do zakładki **EDIT**:  

    <img width="403" height="121" alt="obraz" src="https://github.com/user-attachments/assets/ca76fba7-03c2-452a-8c5d-e93d956d4488" />

    W miejsce:
    ```
        sensor:
        - platform: dallas_temp         ← typ czujnika (tutaj Dallas np. DS18B20)
        name: "Temperatura"
        one_wire_id: onewirebus1
        update_interval: 60s
    ```
    wprowadź (dodaj adresy wyszukanych czujników z konsoli):
    ```
        sensor:
        - platform: dallas_temp
        name: "Temperatura 1"
        address: 0x1f00000c0699f728     ← adres z konsoli (1 czujnik)
        one_wire_id: onewirebus1
        update_interval: 60s
        - platform: dallas_temp
        name: "Temperatura 2"
        address: 0x4900000c06968f28     ← adres z konsoli (2 czujnik)
        one_wire_id: onewirebus1
        update_interval: 60s
    ```
    !!! info "Postępuj analogicznie z większą liczbą czujników."

7. Kliknij **SAVE**, **INSTALL** i pobierz plik `.uf2` tak jak w pierwszej [konfiguracji](Pierwsza-konfiguracja-ESPHome) lub wgraj przez [OTA](Aktualizacja-bezprzewodowa-(OTA))
8. Przejdź do [**wgrywania**](WGRYWANIE-.YAML) firmware