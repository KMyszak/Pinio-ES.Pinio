# Kilka czujników

Jeśli chcesz korzystać z więcej niż jednego czujnika **tego samego typu** (np. DS18B20), musisz znać ich **unikalne adresy**. 

---

1. Wybierz z paska bocznego **ESPHome Builder**:  

    <img width="230" alt="obraz" src="https://github.com/user-attachments/assets/fead98e2-a8eb-4f5e-adb7-caf5b4bb9e2d" />

    ??? failure "Brak skrótu na pasku bocznym?"

        Jeśli nie widzisz skrótu na pasku bocznym:
        
        - przejdź do **konfiguracji**, albo
        - włącz go z poziomu **interejsu użytkownika**

        === "Konfiguracja"
            
            1\. Z lewego paska bocznego wybierz:   
                `Ustawienia → Aplikacje → ESPHome Builder`

            <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

            2\. Zaznacz opcję **Pokaż na pasku bocznym**:

            <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/c85b76f1-343c-4a04-9d09-4ff0459b5d02" />

        === "Ustawienia aplikacji"

            1\. Z lewego paska bocznego wybierz:   
                `Ustawienia → Aplikacje → Zainstaluj aplikację`

            2\. Wyszukaj dodatek **ESPHome** i wybierz `ESPHome Device Builder`:   

            <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

            3\. Kliknij **Otwórz interfejs użytkownika**

2. Przejdź do logów klikając **LOGS**:  

    <img width="403" height="121" alt="obraz" src="https://github.com/user-attachments/assets/040d4be4-e6d8-4913-bd42-ceb8f89de4fa" />

3. Obserwuj dane wyjściowe:

    <img width="700" height="90" alt="obraz" src="https://github.com/user-attachments/assets/955246cf-d666-4021-b693-3d4f0eda3554" />

    !!! success "Wykryte czujniki"

        ESPHome wykryło dwa czujniki DS18B20.     
        Każdy ma unikalny adres hex w formie `0x...`.

4. **Zapisz** adresy i zamknij konsolę
5. Dodaj czujniki do kodu `.YAML` przechodząc do zakładki **EDIT**:  

    <img width="403" height="121" alt="obraz" src="https://github.com/user-attachments/assets/ca76fba7-03c2-452a-8c5d-e93d956d4488" />

    W miejsce:
    ``` yaml
        sensor:
        - platform: dallas_temp         ← typ czujnika (tutaj Dallas np. DS18B20)
        name: "Temperatura"
        one_wire_id: onewirebus1
        update_interval: 60s
    ```
    wprowadź (dodaj adresy wyszukanych czujników z konsoli):
    ``` yaml
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
    !!! info "Masz więcej czujników?"

        Dodaj kolejne wpisy analogicznie - każdy z własnym adresem.

6. Kliknij **SAVE** w prawym górnym rogu, następnie **INSTALL**
7. Wybierz **Manual download**
8. Poczekaj na kompilację (pierwsza trwa ok. 5 min):  
    <img width="420 alt="obraz" src="https://github.com/user-attachments/assets/d860d512-1b22-40d6-9ff3-68f653e40272" />

9. Po kompilacji kliknij **3. Download project**:  
    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/049db2e9-1d0e-4d71-80da-c670d105f53f" />

10. Wybierz `UF2 factory format`:  
    <img width="320" alt="obraz" src="https://github.com/user-attachments/assets/1fd1055a-a028-4160-9c42-97f6f0261cbd" />

11. Przejdź do [**wgrywania**](Wgrywanie-.uf2.md) firmware