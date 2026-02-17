# Wgrywanie Tasmoty
Tasmota to **otwarte oprogramowanie** przeznaczone dla modułów **ESP8266**, które umożliwia sterowanie urządzeniami IoT bez potrzeby korzystania z chmury producenta.

Pozwala na konfigurację przez **przeglądarkę internetową** lub **MQTT**, wspiera szeroką gamę czujników, przekaźników i inteligentnych wtyczek, a jego główną zaletą jest pełna kontrola nad urządzeniem lokalnie.

## Wymagane narzędzia

Płytka występuje w dwóch wersjach: z wbudowanym konwerterem USB–UART lub bez niego.
Od tego zależy, jakie narzędzia będą potrzebne do wgrania firmware:

- **Wersja z wlutowanym konwerterem:** 
    
    - przewód microUSB
    - program [**Tasmotizer**](tasmotizer.md)
    - obraz [**Tasmota**](tasmota.md)

- **Wersja bez wbudowanego konwertera:** 

    - konwerter USB-UART (np. FTDI FT232RL USB)
    - przewody połączeniowe do komunikacji ESP-12F ⇄ konwerter USB-UART
    - oprogramowanie [**esptool**](esptool.md)
    - obraz [**Tasmota**](tasmota.md)

## Procedura instalacji

Sposób wgrywania oprogramowania zależy od typu używanego konwertera:

- **Zewnętrzny konwerter USB-UART:** można zastosować dwie metody:
    - **Rekomendowana:**  zasilanie z wbudowanego stabilizatora płytki - bezpieczne i stabilne
    - **Alternatywna:** zasilanie bezpośrednio z konwertera USB-UART - **WYŁĄCZNIE 3,3 V!**
- **Wlutowany konwerter USB:** firmware można wgrać za pomocą programu Tasmotizer, który automatycznie wykrywa płytkę i przesyła plik MicroPython

=== "Zewnętrzny konwerter"

    Zewnętrzny konwerter pozwala na połączenie płytki bez wbudowanego USB i przesłanie firmware’u. Wybór metody zależy od sposobu zasilania i stabilności połączenia.

    === "Rekomendowana"

        Firmware wgrywa się przy zasilaniu z wbudowanego stabilizatora płytki. Jest to metoda bezpieczna i stabilna, minimalizująca ryzyko uszkodzenia płytki podczas programowania.

        1. Podłącz ES.Pinio do zasilania (12 VDC) oraz ESP-12F do konwertera USB:     
        
            <img width="500" alt="schemat polaczenia esp12f" src="https://github.com/user-attachments/assets/f6a390f1-e84c-42fd-bcd5-89b84aceb9e5" />

            Schemat połączenia:
        
            <img width="500" alt="schemat połączenia esp12f bez VCC" src="https://github.com/user-attachments/assets/15ae5c3d-9bca-4254-bc9e-ebec7dd0e90c" />

        2. Naciśnij i przytrzymaj jednocześnie przyciski **RST** oraz **BOOT** (*tryb flashowania*)
        3. Nie puszczając przycisku **BOOT**, puść przycisk **RST**  
        
            !!! info ""
                
                Świecąca dioda statusowa **STA** oznacza włączenie trybu.
        4. Kliknij menu Start
        5. Wpisz `cmd`
        6. Znajdź `Wiersz polecenia` i wybierz **Uruchom jako administrator**:

            <img width="500" height="489" alt="obraz" src="https://github.com/user-attachments/assets/e7111e0e-9895-40ad-a770-fd5264ca4be9" />

        7. Przejdź do folderu, gdzie znajdują się pliki `esptool.exe` i `tasmota.bin`:  
        Wpisz polecenie `cd`, a następnie ścieżkę do tego folderu, np.:  
        
            `cd C:\Users\chomtech\Desktop\esptool-win64_Tasmota`  

            <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/b357ac43-35bf-4c05-b3d5-6175d4a18cb7" />

        8. Uruchom komendę wgrywania firmware:  
            ```
            esptool.exe -p COMX -b 115200 write_flash --flash_size detect 0x00000 tasmota.bin 
            ```
            gdzie:  
            
            - `COMX` - numer portu szeregowego przypisanego do konwertera USB   
            - `tasmota` - nazwa pliku z firmware  

            Proces flashowania:
            
            <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/46a9ae2e-c0f7-4f69-947f-a7f696f9e67f" />

            Po prawidłowym flashowaniu pojawi się komunikat potwierdzający zakończenie wgrywania:   
            
            <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/c63bac99-92ce-40dc-ad3d-fd114b760731" />

        9. Zresetuj urządzenie klikając przycisk **RST** na urządzeniu.  
        10. Przejdź do dalszej [**konfiguracji**](../ES_Pinio/Pierwsze-uruchomienie.md)    

        !!! info "Problemy"
        
            W razie problemów z ustawieniami lub instalacją przejdź do [Problemy](../FAQ/ES.Pinio-problemy.md)
    
    === "Alternatywna"

        !!! danger "Firmware można wgrać przy zasilaniu bezpośrednio z konwertera, TYLKO przy 3,3 V."
        Ta metoda jest przydatna, gdy wbudowany stabilizator nie jest dostępny, ale wymaga szczególnej ostrożności.

        1. Podłącz ES.Pinio korzystając wyłącznie z konwertera USB:  
        
            !!! warning "Pamiętaj o ustawieniu zworki na konwerterze USB na 3,3 V (VCC)!"
            
            <img width="500" alt="schemat polaczenia esp12f" src="https://github.com/user-attachments/assets/4ed684e4-039e-40bd-a592-69eacc51228b" />

            Schemat połączenia:
            
            <img width="500" alt="schemat polaczenia esp12f" src="https://github.com/user-attachments/assets/7d6f68c6-aaa9-497b-ab0f-df04cc38f336" />

        2. Naciśnij i przytrzymaj jednocześnie przyciski **RST** oraz **BOOT** (tryb flashowania)
        3. Nie puszczając przycisku **BOOT**, puść przycisk **RST**
            
            !!! info ""
                
                Świecąca dioda statusowa **STA** oznacza włączenie trybu.
        4. Kliknij menu Start
        5. Wpisz `cmd`
        6. Znajdź `Wiersz polecenia` i wybierz **Uruchom jako administrator**:

            <img width="500" height="489" alt="obraz" src="https://github.com/user-attachments/assets/e7111e0e-9895-40ad-a770-fd5264ca4be9" />

        7. Przejdź do folderu, gdzie znajdują się pliki `esptool.exe` i `tasmota.bin`:  
        Wpisz polecenie `cd`, a następnie ścieżkę do tego folderu, np.:  
        
            `cd C:\Users\chomtech\Desktop\esptool-win64_Tasmota`  

            <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/b357ac43-35bf-4c05-b3d5-6175d4a18cb7" />

        8. Uruchom komendę wgrywania firmware:  
            ```
            esptool.exe -p COMX -b 115200 write_flash --flash_size detect 0x00000 tasmota.bin 
            ```
            gdzie:  
            
            - `COMX` - numer portu szeregowego przypisanego do konwertera USB   
            - `tasmota` - nazwa pliku z firmware  

            Proces flashowania:
            
            <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/46a9ae2e-c0f7-4f69-947f-a7f696f9e67f" />

            Po prawidłowym flashowaniu pojawi się komunikat potwierdzający zakończenie wgrywania:   
            
            <img width="500" alt="obraz" src="https://github.com/user-attachments/assets/c63bac99-92ce-40dc-ad3d-fd114b760731" />

        9. Zresetuj urządzenie klikając przycisk **RST** na urządzeniu.  
        10. Przejdź do dalszej [**konfiguracji**](../ES_Pinio/Pierwsze-uruchomienie.md)    

        !!! info "Problemy"
        
            W razie problemów z ustawieniami lub instalacją przejdź do [Problemy](../FAQ/ES.Pinio-problemy.md)

=== "Wlutowany konwerter"

    Firmware wgrywa się za pomocą programu **Tasmotizer**, który automatycznie wykrywa płytkę i przesyła obraz **Tasmota**. Metoda jest szybka i wygodna, idealna dla płytek z wbudowanym portem USB, bez konieczności dodatkowego sprzętu.

    1. Podłącz urządzenie przez przewód microUSB do komputera:
        
        <img width="364" height="544" alt="obraz" src="https://github.com/user-attachments/assets/1b4cd00a-52ad-4cc7-978a-2b7ebcb58ed9" />

    2. Otwórz program `Tasmotizer` [(**tasmotizer-1.2.exe**)](../Firmware/tasmotizer.md):
    3. Wybierz odpowiedni port z listy `Select port` (sprawdzenie portu → [COM](../Firmware/PortCOM.md)):
        
        <img width="492" height="460" alt="obraz" src="https://github.com/user-attachments/assets/f53fed15-72a2-47b2-8e58-4e823aa7eef8" />

    4. W sekcji `Select image` wybierz pobrany plik [**tasmota.bin**](../Firmware/tasmota.md):
    
        <img width="492" height="460" alt="obraz" src="https://github.com/user-attachments/assets/f21bdaf8-90fa-49db-9e8c-f1a5c4812a5f" />

    5. Kliknij `Tasmotize!` - rozpocznie się proces flashowania:
    
        <img width="402" height="170" alt="obraz" src="https://github.com/user-attachments/assets/443b04ff-7143-4574-a173-b3d4f62651fd" />
        
        !!! info ""
        
            Dioda **STA** powinna zacząć świecić oraz mrugać dioda na układzie ESP-12F

    6. Po zakończeniu pojawi się informacja:
    
        <img width="301" height="108" alt="obraz" src="https://github.com/user-attachments/assets/ade67d2f-71ac-49eb-99b8-a2ceab9bb66e" />
    7. Urządzenie zostanie zresetowane i uruchomi swój AP, z którym możesz się połączyć celem zmiany ustawień Wi-Fi → [**łączenie z Access Pointem**](../ES_Pinio/Pierwsze-uruchomienie.md)

    !!! tip "Zmiana ustawień przez program"
    
        Ustawienia Wi-Fi (oraz MQTT) można zmienić przez program, wybierając przycisk `Send config`, następnie zaznaczając okienko WiFi, wpisując poprawne dane i klikając przycisk `Save`:
        
        <img width="642" height="375" alt="obraz" src="https://github.com/user-attachments/assets/ed3ca8c1-de72-4da6-88ba-a5617c573807" />
        
        Urządzenie się zrestartuje, a po kilku sekundach można odczytać jego IP klikając przycisk `Get IP`:
        
        <img width="300" height="123" alt="obraz" src="https://github.com/user-attachments/assets/c213f1df-0984-4e74-b100-22ec17327274" />
        
        Dalszą edycję należy przeprowadzić przez przeglądarkę, korzystając z uzyskanego adresu IP → [**Konfiguracja**](../ES_Pinio/Podstawowe-ustawienia-i-GPIO.md)
