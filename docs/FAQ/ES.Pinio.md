# ES.Pinio

!!! tip "W razie problemów z połączeniem lub niestandardowym zachowaniem urządzenia warto zacząć od przywrócenia ustawień domyślnych. Jeśli to nie pomoże - rozważ całkowite wymazanie pamięci flash"

---

## Reset ustawień

### Przywrócenie domyślnej konfiguracji 

!!! info "Jeśli znasz adres IP urządzenia w swojej sieci"

1. Połącz się z **ES.Pinio** wpisując jego **adres IP** w przeglądarce
2. Przejdź do `Configuration`
3. Kliknij **Reset** i potwierdź
4. Przeprowadź ponownie [**konfigurację**](../ES_Pinio/Pierwsze-uruchomienie.md) 

---
### Fast Power Cycle Device Recovery 

!!! warning "Funkcja usuwa WSZYSTKIE ustawienia Tasmota" 

1. Odłącz zasilanie urządzenia na **30 sekund**
2. Włącz i wyłącz urządzenie 6 razy:
    
    !!! note ""
    
        Każde **włączenie**/**wyłączenie** musi nastąpić w odstępie **krótszym niż 10 sekund**.    
        Rekomendowane: ~2 sekundy włączenia i ~2 sekundy wyłączenia.

3. Przy 7 włączeniu urządzenie zresetuje się do ustawień fabrycznych i uruchomi **Access Point**
4. Przeprowadź ponownie [**konfigurację**](../ES_Pinio/Pierwsze-uruchomienie.md#)

---
### Wymazanie pamięci flash przy pomocy narządznia [`esptool`](../Firmware/esptool.md) 

!!! info "Wymagany konwerter USB-UART"

Jeśli reset konfiguracji nie rozwiązuje problemów lub nie możesz połączyć sie z urządzeniem, wykonaj pełne wymazanie pamięci i ponowne wgranie firmware:  

1. Zasil urządzenie **ES.Pinio** i podłącz moduł **ESP-12F** do komputera zgodnie ze schematem: 

    <img width="500" alt="schemat połączenia esp12f bez VCC" src="https://github.com/user-attachments/assets/15ae5c3d-9bca-4254-bc9e-ebec7dd0e90c" />

2. Wprowadź **ESP-12F** w *tryb flashowania*:

    naciśnij jednocześnie **BOOT** i **RST**, następnie puść najpierw **RST**, a potem **BOOT**

3. Otwórz **wiersz poleceń** (CMD) jako **administrator**   
4. Przejdź do folderu z wypakowanym narzędziem `esptool` i obrazem `tamota.bin`
5. Wpisz polecenie do wymazania pamięci flash: 
    ``` 
    esptool.exe -p COMX erase_flash   
    ```
    Następnie wgraj nowy firmware:  
    ```
    esptool.exe -p COMX -b 115200 write_flash --flash_size detect 0x00000 tasmota.bin  
    ```
    gdzie:  
    `COMX` - numer portu COM konwertera USB-UART  
    `tasmota.bin` - plik firmware
6. Zresetuj urządzenie (**RST**)
7. Przeprowadź ponownie [**konfigurację**](../ES_Pinio/Pierwsze-uruchomienie.md)  

---

## Sprawdzenie adresu IP przypisanego do urządzenia

### Jeśli masz dostęp do panelu routera, z którym połączone jest ES.Pinio

1. Zaloguj się do **panelu administratora routera**
2. Przejdź do sekcji odpowiedzialnej za listę urządzeń i ich adresy IP, zwykle:  
    `DHCP → DHCP Client List`
3. Znajdź na liście urządzenie **ES.Pinio** (może być widoczne jako np. `tasmota-6XXXXX-XXX2`)
4. Wpisz jego **adres IP** w przeglądarce (np. `192.168.119.28`)
5. Wprowadź potrzebne zmiany na stronie urządzenia i zapisz ustawienia.

### Urządzenie jest połączone z Home Assistant

1. Z paska bocznego wybierz:  
 `Ustawienia → Urządzenia oraz usługi → Tasmota` i znajdź swoje urządzenie:

    <img width="236" height="245" alt="obraz" src="https://github.com/user-attachments/assets/96222e4d-49e9-4655-ab0e-7404c687187a" />

2. W oknie `Diagnostyka` rozwiń listę `+X wyłączone encje`, znajdź encję **IP**, kliknij ikonę zębatki i&nbsp;zaznacz **Encja włączona** 
3. Poczekaj około **30 sekund** na aktywację encji i odśwież stronę, aby wyświetlić aktualny **adres IP**:
    
    <img width="264" height="373" alt="obraz" src="https://github.com/user-attachments/assets/33362c5a-77e0-4b39-abc6-9095751bd389" />

### Sprawdzenie logów MQTT

1. Z paska bocznego wybierz `Ustawienia → Aplikacje → Mosquitto broker`
2. Wybierz zakładkę `Logi`:
    
    <img width="1139" height="196" alt="obraz" src="https://github.com/user-attachments/assets/a16e7545-6b37-442d-8c38-f5bee74f9f27" />

3. Znajdź logi informujące o połączeniu:

    <img width="528" height="35" alt="obraz" src="https://github.com/user-attachments/assets/9d11719c-1412-4b25-8983-3d70682e408a" />

---

## Inne przypadki

!!! info "Więcej przypadków i rozwiązań"

    Pełna lista najczęściej występujących problemów Tasmoty dostępna jest w oficjalnym FAQ: [**tasmota.github.io/docs/FAQ :material-open-in-new:**](https://tasmota.github.io/docs/FAQ)