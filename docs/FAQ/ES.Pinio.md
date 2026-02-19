# ES.Pinio

!!! tip "W razie problemów z połączeniem się lub dziwnym zachowaniem urządzenia, warto zacząć od przywrócenia ustawień domyślnych lub - jeśli to nie pomoże - całkowitego wymazania pamięci flash"

---

## Reset ustawień

### Przywrócenie domyślnej konfiguracji (jeśli znasz IP urządzenia w sieci)
1. Połącz się z urządzeniem **ES.Pinio** wpisując jego **adres IP** w przeglądarce
2. Przejdź do `Configuration`
3. Kliknij **Reset** i potwierdź
4. Przeprowadź [**konfigurację**](../ES_Pinio/Pierwsze-uruchomienie.md) od nowa

---
### Fast Power Cycle Device Recovery (reset do ustawień fabrycznych)

!!! warning "Funkcja kasuje WSZYSTKIE ustawienia Tasmota" 

1. Odłącz całkowicie zasilanie urządzenia na 30 sekund
2. Włącz i wyłącz urządzenie 6 razy:
    
    !!! info "Każde włącz/wyłącz powinno mieć odstęp mniejszy niż 10 sekund między zmianami stanu. Zalecane jest około 2 sekund włączenia i 2 sekund wyłączenia."

3. Przy 7 włączeniu urządzenie zresetuje się do ustawień fabrycznych i uruchomi **Access Point**
4. Przeprowadź [**konfigurację**](../ES_Pinio/Pierwsze-uruchomienie.md#) od nowa

---
### Wymazanie pamięci flash przy pomocy narządznia [`esptool`](../Firmware/esptool.md) (*wymagany konwerter USB-UART*)
Jeśli reset konfiguracji nie rozwiązuje problemów lub nie możesz połączyć sie z urządzeniem, pozostaje wymazanie całej pamięci flash i ponowne wgranie firmware:  

1. Zasil płytkę **ES.Pinio** i podłącz **ESP-12F** do komputera zgodnie ze schematem: 

    <img width="500" alt="schemat połączenia esp12f bez VCC" src="https://github.com/user-attachments/assets/15ae5c3d-9bca-4254-bc9e-ebec7dd0e90c" />

2. Wprowadź **ESP-12F** w *tryb flashowania*:

    naciśnij jednocześnie **BOOT** i **RST**, następnie puść najpierw **RST**, a potem **BOOT**

3. Otwórz **wiersz poleceń** (CMD) jako **administrator**   
4. Przejdź do folderu z wypakowanym narzędziem `esptool` 
5. Wpisz polecenie do wymazania pamięci flash: 
    ``` 
    esptool.exe -p COMX erase_flash   
    ```
    Następnie wgraj nowy firmware:  
    ```
    esptool.exe -p COMX -b 115200 write_flash --flash_size detect 0x00000 tasmota.bin  
    ```
    gdzie:  
    `COMX` - numer portu szeregowego przypisanego do konwertera USB   
    `tasmota` - nazwa pliku z firmware
6. Zresetuj urządzenie (przycisk **RST**)
7. Przejdź do [**konfiguracji**](../ES_Pinio/Pierwsze-uruchomienie.md)  

---

## Sprawdzenie przypisanego IP do urządzenia

### Masz dostęp do ustawień routera do którego jest podłączone ES.Pinio

1. Zaloguj się do panelu administratora routera
2. Znajdź zakładkę odpowiedzialną za przypisywanie **adresu IP** urządzeniom podłączonym do routera:  
    `DHCP → DHCP Client List`
3. Wyszukaj urządzenie ES.Pinio (np. tasmota-6XXXXX-XXX2)
4. Wpisz jego **adres IP** w przeglądarce (np. 192.168.119.28)
5. Zmień i zapisz ustawienia na stronie

### Urządzenie jest połączone z Home Assistant

1. Przejdź do `Ustawienia → Urządzenia oraz usługi → Tasmota` i wybierz urządzenie:

    <img width="236" height="245" alt="obraz" src="https://github.com/user-attachments/assets/96222e4d-49e9-4655-ab0e-7404c687187a" />

2. W oknie `Diagnostyka` rozwiń `+X wyłączone encje`, wybierz **IP**, kliknij ikonę zębatki i zaznacz **Encja włączona** 
3. Poczekaj 30 sekund na włączenie encji i odśwież stronę:
    
    <img width="264" height="373" alt="obraz" src="https://github.com/user-attachments/assets/33362c5a-77e0-4b39-abc6-9095751bd389" />

### Sprawdzenie logów MQTT

1. Przejdź do `Ustawienia → Dodatki → Mosquitto broker`
2. Wybierz zakładkę `Logi`:
    
    <img width="876" height="144" alt="obraz" src="https://github.com/user-attachments/assets/41536762-8366-44de-b22e-55a64759592f" />

3. Znajdź logi informujące o połączeniu:

    <img width="528" height="35" alt="obraz" src="https://github.com/user-attachments/assets/9d11719c-1412-4b25-8983-3d70682e408a" />

---

## Inne przypadki

!!! info "Więcej przypadków i rozwiązań"

    Szczegółowa lista często występujących problemów Tasmoty dostępna jest w oficjalnym FAQ: [**tasmota.github.io/docs/FAQ :material-open-in-new:**](https://tasmota.github.io/docs/FAQ)