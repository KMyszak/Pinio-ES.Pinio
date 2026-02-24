# Wgrywanie firmware

**Raspberry Pi Pico** korzysta z formatu pliku `.uf2`, który umożliwia łatwe wgrywanie firmware metodą *drag-and-drop*.

---

1. Wciśnij i przytrzymaj przycisk `BOOTSEL` na **Raspberry Pi Pico** (*tryb bootloadera*):   

    <img width="450" height="185" alt="obraz" src="https://github.com/user-attachments/assets/45e3f7a5-8e13-4149-ac28-b6af3f6ff1bb" />

2. Podłącz urządzenie do komputera przez kabel Micro-USB (trzymając przycisk)
3. Pojawi się nowy dysk `RPI-RP2`:     

    <img width="345" height="491" alt="5f1a689a-ed49-4164-a533-4cf26efe96d5" src="https://github.com/user-attachments/assets/a248e571-ffb3-49e4-be9d-cfd0f1b52a1f" />

4. Przenieś pobrany plik `.uf2` na dysk **RPI-RP2**
5. **Raspberry Pi Pico W** zrestartuje się automatycznie i zniknie jako dysk USB

    !!! note "Po instalacji"

        Po poprawnym flashowaniu urządzenia powinno być widoczne w **Home Assistant**.

6. W panelu bocznym **Home Assistant** przejdź do:  
    `Ustawienia → Urządzenia oraz usługi → ESPHome`

    <img width="310" alt="obraz" src="https://github.com/user-attachments/assets/85f07072-bb43-41d9-97e6-a2fc11525561" />  

7. **ESPHome** wykryje nowe urządzenie i domyślne 7 encji (*entities*): 

    <img width="310" alt="obraz" src="https://github.com/user-attachments/assets/872ffa1b-f219-4ccd-97a7-269725a2df33" />

---

## Dostępne encje

- Sterowanie:
    - **RELAY 1** - Wyjście przekaźnikowe 1
    - **RELAY 2** - Wyjście przekaźnikowe 2 
    - **STA LED** - Dioda statusowa STA

- Sensory:
    - **Temperature** - Czujnik 1-Wire
    - **IN 1** - Wejście cyfrowe 1 
    - **IN 2** - Wejście cyfrowe 2 
  
- Konfiguracja:
    - **Firmware** -  Panel aktualizacji (encja wyłączona)

!!! info "Widok panelu urządzenia w ESPHome"

    <img width="984" height="817" alt="obraz" src="https://github.com/user-attachments/assets/3172155d-8e89-4771-8042-8b36ee66c7cb" />
