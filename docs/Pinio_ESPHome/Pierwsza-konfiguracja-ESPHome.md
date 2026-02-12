1. Wybierz na pasku bocznym **ESPHome Builder** (jeśli go nie widzisz → [Pokaż na pasku bocznym](ESPHome-Builder)): 
    
    <img width="209" height="98" alt="obraz" src="https://github.com/user-attachments/assets/f078b6cd-35d3-4da9-b244-fdfed223b755" />

2. Kliknij **`+ NEW DEVICE`**: 
    
    <img width="293" height="124" alt="obraz" src="https://github.com/user-attachments/assets/4f2c7f89-8fe2-4a56-8217-097bf8a66dbf" />

3. Kliknij **Continue**
4. Wpisz nową nazwę urządzenia
5. Wybierz konfigurację `Raspberry Pi Pico W`
6. W oknie z `Encryption key` kliknij **SKIP**
7. Nowe urządzenie powinno pojawić się w panelu:

    <img width="371" height="129" alt="obraz" src="https://github.com/user-attachments/assets/3deac809-f62a-423e-a5f0-d0d29f89203a" />

---

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

        W tym miejscu możesz zmienić zmienne `name` dla **wejść** (binary_sensor), **wyjść** (switch) i **czujnika temperatury** (sensor) - wpłynie to na nazwy encji w Home Assistant  

3. Kliknij w prawym górnym rogu **SAVE**, następnie **INSTALL**
4. Wybierz **Manual download**
5. Pierwsze kompilowanie projektu trwa około 5 minut:  

    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/d10554a1-22dc-4579-a910-f2a2130c3e08" />

6. Po zakończonej kompilacji kliknij `3. Download project`:  

    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/779b1301-5691-4656-a40f-4a0862e982fb" />

7. Wybierz `UF2 factory format`:  

    <img width="320" alt="obraz" src="https://github.com/user-attachments/assets/470bdf1e-43ed-40a7-a809-cb6bdc5fbb17" />

8. Przejdź do [**wgrywania**](../../Pinio_ESPHome/Wgrywanie-.uf2) firmware
