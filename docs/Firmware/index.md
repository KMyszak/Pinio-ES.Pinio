# Firmware

Zakładka **Firmware** prezentuje proces aktualizacji lub instalacji oprogramowania dla dwóch urządzeń: 

- **ES.Pinio** - oparte na **ESP8266**, działające pod kontrolą Tasmota - z jak i bez wbudowanego **konwertera**
- **Pinio** - działające z **Raspberry Pi Pico W 2** z dedykowanym **firmware** napisanym w MicroPythonie

Sekcja przedstawia wymagane narzędzia oraz kolejne etapy instalacji, umożliwiając użytkownikowi prawidłowe przygotowanie i wgranie oprogramowania.

<div class="grid cards" markdown>

- :material-memory:{ .lg .middle } __ES.Pinio__

    Urządzenie **z wbudowanym** konwerterem:

    - przewód microUSB
    - program Tasmotizer
    - obraz Tasmota (`.bin`)

    ---

    Urządzenie **bez wbudowanego** konwertera:

    - zewnętrzny konwerter USB-UART
    - przewody połączeniowe
    - narzędzie esptool
    - obraz Tasmota (`.bin`)
    
    ---

    [:octicons-arrow-right-24: Przejdź do instalacji](ES_Pinio.md)

- :material-code-tags:{ .lg .middle } __Pinio__

    Wymagania:

    - przewód microUSB
    - firmware MicroPython (`.bin`)

    ---

    [:octicons-arrow-right-24: Przejdź do instalacji](Pinio_MicroPython.md)

</div>