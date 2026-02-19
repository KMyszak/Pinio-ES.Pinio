# Pierwsza konfiguracja

Pierwsza konfiguracja polega na utworzeniu nowego urządzenia w dodatku **ESPHome**, przypisaniu mu nazwy i przygotowaniu podstawowego pliku `.YAML`.   
Następnie urządzenie łączy się z siecią Wi‑Fi po wgraniu firmware staje się widoczne w **Home Assistant**. 

---

## Dodanie urządzenia

1. Wybierz z paska bocznego **ESPHome Builder**: 

    <img width="230" alt="obraz" src="https://github.com/user-attachments/assets/fead98e2-a8eb-4f5e-adb7-caf5b4bb9e2d" />

    ??? failure "Brak skrótu na pasku bocznym?"

        Jeśli nie widzisz skrótu na pasku bocznym:
        
        - przejdź do **konfiguracji** lub
        - przejdź do **interejsu użytkownika**

        === "Konfiguracja"
            
            1.Z menu po lewej stronie wybierz `Ustawienia → Aplikacje → ESPHome Builder`:

            <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

            2.Zaznacz **Pokaż na pasku bocznym**:

            <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/c85b76f1-343c-4a04-9d09-4ff0459b5d02" />

        === "Ustawienia aplikacji"

            1.Z menu po lewej stronie wybierz:  
                `Ustawienia → Aplikacje → Zainstaluj aplikację`

            2.Wyszukaj dodatek **ESPHome** i wybierz `ESPHome Device Builder`:   

            <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

            3.Kliknij **Otwórz interfejs użytkownika**

2. Kliknij **+ NEW DEVICE**: 

    <img width="293" height="124" alt="obraz" src="https://github.com/user-attachments/assets/4f2c7f89-8fe2-4a56-8217-097bf8a66dbf" />

3. Kliknij **Continue**
4. Wpisz nową nazwę urządzenia
5. Wybierz konfigurację `Raspberry Pi Pico W`
6. W oknie z `Encryption key` kliknij **SKIP**
7. Nowe urządzenie powinno pojawić się w panelu:

    <img width="371" height="129" alt="obraz" src="https://github.com/user-attachments/assets/3deac809-f62a-423e-a5f0-d0d29f89203a" />

## Edycja konfiguracji

1. Przejdź do edycji klikając **EDIT**:  
    <img width="371" height="129" alt="obraz" src="https://github.com/user-attachments/assets/ed969c22-e043-43eb-b0fa-cc2ba651247b" />

2. Dodaj kod do pliku `.yaml`:
    ```
    one_wire:
    - platform: gpio
        pin: GPIO17
        id: onewirebus1
    sensor:
    - platform: dallas_temp               
        name: "Temperature"
        one_wire_id: onewirebus1
        update_interval: 60s               # interwał odświeżania temperatury (1-Wire)
    binary_sensor:
    - platform: gpio
        name: "IN 1"
        id: in1
        pin:
        number: GPIO18
        mode: INPUT_PULLUP
        inverted: true
    - platform: gpio
        name: "IN 2"
        id: in2
        pin:
        number: GPIO19
        mode: INPUT_PULLUP
        inverted: true
    switch:
    - platform: gpio
        pin: GPIO20
        name: "RELAY 1"
        id: out1
        restore_mode: RESTORE_DEFAULT_OFF  # przywraca poprzedni stan (sprzed ~30 sekund)  
                                           # jeśli się nie uda, ustawiany jest stan OFF
    - platform: gpio                 
        pin: GPIO21
        name: "RELAY 2"
        id: out2
        restore_mode: RESTORE_DEFAULT_OFF  # przywraca poprzedni stan (sprzed ~30 sekund) 
                                           # jeśli się nie uda, ustawiany jest stan OFF
    light:
    - platform: status_led
        name: "STA LED"
        id: sta_led 
        pin:
        number: GPIO16     
        inverted: false
        restore_mode: ALWAYS_ON             # zawsze włączona dioda STA po restarcie
    ```

    !!! info "Nazwy"

        W tym miejscu możesz zmienić zmienne *name* dla **wejść** (binary_sensor), **wyjść** (switch) i **czujnika temperatury** (sensor) - wpłynie to na nazwy encji w Home Assistant.  

3. Kliknij w prawym górnym rogu **SAVE**, następnie **INSTALL**
4. Wybierz **Manual download**
5. Pierwsze kompilowanie projektu trwa około 5 minut:  
    <img width="420 alt="obraz" src="https://github.com/user-attachments/assets/d860d512-1b22-40d6-9ff3-68f653e40272" />

6. Po zakończonej kompilacji kliknij ***3. Download project***:  
    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/049db2e9-1d0e-4d71-80da-c670d105f53f" />

7. Wybierz `UF2 factory format`:  
    <img width="320" alt="obraz" src="https://github.com/user-attachments/assets/1fd1055a-a028-4160-9c42-97f6f0261cbd" />

8. Przejdź do [**wgrywania**](Wgrywanie-.uf2.md) firmware
