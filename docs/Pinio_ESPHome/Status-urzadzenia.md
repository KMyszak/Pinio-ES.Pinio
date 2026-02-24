# Status urządzenia

<img width="200" align="left" alt="obraz" src="https://github.com/user-attachments/assets/a311e24b-7518-4c6c-97aa-9c195ab1cc30" />

Po poprawnie przeprowadzonych [ustawieniach](Pierwsza-konfiguracja-ESPHome.md#edycja-konfiguracji) dioda statusowa **STA** pracuje w konfiguracji:

  - włączona[^1] - urządzenie połączone z Home Assistant
  - miga co 1 s - ostrzeżenie (np. problem z połączeniem Wi-Fi lub MQTT)
  - miga co 0,5 s - błąd (np. problem z czujnikiem wykryty przez ESPHome)

[^1]: Opcję można zmienić poprzez przełączenie encji *Status LED* w panelu **Home Assistant**. 


!!! info "Dioda statusowa"

    Dioda włączy się ponownie po restarcie urządzenia.  
    Aby *wyłączyć automatyczne zapalanie* diody statusowej STA, należy edytować plik *.YAML*.

!!! tip "Encja Status LED"

    Encję **Status LED** najprościej znaleźć przez wyszukiwarkę w *Rejestrze encji* lub przechodząc do panelu urządzenia: `Ustawienia → Urządzenia oraz usługi → ESPHome → Sterowanie`

    <img width="300" alt="obraz" src="https://github.com/user-attachments/assets/9867cea6-8ac7-4a5e-9d20-58b8c542bcdc" />

---

## Wyłączenie automatycznego zapalania diody STA

1. Wybierz z paska bocznego **ESPHome Builder**:

    <img width="230" alt="obraz" src="https://github.com/user-attachments/assets/fead98e2-a8eb-4f5e-adb7-caf5b4bb9e2d" />

2. Przejdź do edycji kodu klikając **EDIT**:  

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/3531764d-7d58-4168-9e69-c9f6bb7a7bfa" />

3. W sekcji `light` usuń parametr `restore_mode`, który odpowiada za automatyczne włączanie encji po restarcie:
    ``` yaml
    light:
    - platform: status_led
        name: "Status LED"
        pin:
        number: GPIO16     
        inverted: false
        restore_mode: ALWAYS_ON  ←  usuń tę linię
    ```
4. Kliknij w prawym górnym rogu **SAVE**, a następnie **INSTALL**
5. Wybierz **Manual download** lub **Wirelessly**:

    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/6d538c45-59d7-4560-af3b-d1b329fa4226" />

=== "Manual download"

    6\. Wybierz **Manual download**:  
    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/13ece7ce-0c48-469b-8867-c96a428002d1" />

    7\. Pierwsze kompilowanie projektu trwa **około** 5 minut:  
    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/d10554a1-22dc-4579-a910-f2a2130c3e08" />

    8\. Po zakończonej kompilacji kliknij `3. Download project`:      
    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/779b1301-5691-4656-a40f-4a0862e982fb" />

    9\. Wybierz `UF2 factory format`:           
    <img width="320" alt="obraz" src="https://github.com/user-attachments/assets/470bdf1e-43ed-40a7-a809-cb6bdc5fbb17" />

    10\. Przejdź do [**wgrywania**](Wgrywanie-.uf2.md) firmware

=== "Wirelessly"

    6\. Wybierz **Wirelessly**:  
    <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/adf9d6c7-618f-4374-b9e4-370ca8234820" />
    
    7\. Cały proces trwa **około** 5 minut:  
    <img width="567" height="113" alt="obraz" src="https://github.com/user-attachments/assets/43e42ce9-b589-43fc-aa08-0261c797c8dd" />
    
    8\. Po zakończonej **instalacji OTA** pojawi się komunikat:    
    <img width="567" height="56" alt="obraz" src="https://github.com/user-attachments/assets/2e1c3e6c-160f-4210-9fa2-b17ac451cd9d" />

!!! info "Zmiana działania diody STA"

    Po restarcie dioda już nie będzie się automatycznie zapalać - wciąż będzie informować o ostrzeżeniach i&nbsp;błędach.



