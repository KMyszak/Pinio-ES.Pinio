# Wgrywanie firmware

**Raspberry Pi Pico** korzysta z formatu pliku `.uf2` który służy do łatwego wgrywania oprogramowania metodą *drag-and-drop*.

---

1. Wciśnij i przytrzymaj przycisk `BOOTSEL` na Pico W (*tryb bootloadera*):   
    <img width="450" height="185" alt="obraz" src="https://github.com/user-attachments/assets/45e3f7a5-8e13-4149-ac28-b6af3f6ff1bb" />

2. Podłącz urządzenie do komputera przez kabel microUSB (wciąż trzymając przycisk)
3. Pojawi się nowy dysk `RPI-RP2`:     
    <img width="345" height="491" alt="5f1a689a-ed49-4164-a533-4cf26efe96d5" src="https://github.com/user-attachments/assets/a248e571-ffb3-49e4-be9d-cfd0f1b52a1f" />

4. Przenieś pobrany plik `.uf2` na dysk **RPI-RP2**
5. **Raspberry Pi Pico W** zrestartuje się automatycznie - po chwili zniknie jako dysk USB

    !!! note ""

        Po poprawnym skonfigurowaniu powinno być widoczne w **Home Assistant**

6. Z menu po lewej stronie wybierz:  
    `Ustawienia → Urządzenia oraz usługi → ESPHome`:

    <img width="310" alt="obraz" src="https://github.com/user-attachments/assets/85f07072-bb43-41d9-97e6-a2fc11525561" />  


    ESPHome powinno wykryć 7 encji (entities): 

    <img width="310" alt="obraz" src="https://github.com/user-attachments/assets/872ffa1b-f219-4ccd-97a7-269725a2df33" />

---

## Dostępne encje

Do dyspozycji użytkownika są następujące encje:

- Sterowanie:
    - **Przekaźnik 1** - Wyjście przekaźnikowe 1 (Relay 1)
    - **Przekaźnik 2** - Wyjście przekaźnikowe 2 (Relay 2)
    - **Status LED** - Dioda statusowa STA

- Sensory:
    - **Temperatura** - Czujnik 1-Wire (np. DS18B20)
    - **Wejście 1** - Wejście cyfrowe 1 (IN1)
    - **Wejście 2** - Wejście cyfrowe 2 (IN2)
  
- Konfiguracja:
    - **Firmware** -  Panel aktualizacji (encja wyłączona)

!!! info "Widok panelu urządzenia w ESPHome"

    <img width="896" height="743" alt="obraz" src="https://github.com/user-attachments/assets/65bb78be-2a3b-4b6c-8054-8812780e9eb8" />
