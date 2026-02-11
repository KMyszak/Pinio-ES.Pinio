# Status urządzenia

<img width="200" align="left" alt="obraz" src="https://github.com/user-attachments/assets/a311e24b-7518-4c6c-97aa-9c195ab1cc30" />

Na urządzeniu po poprawnie przeprowadzonej [konfiguracji :material-open-in-new:](Pierwsza-konfiguracja-ESPHome#edycja-konfiguracji) dioda statusowa **STA** pracuje w konfiguracji:


Status diody STA: 

  - włączona¹ → urządzenie połączone z Home Assistant
  - miga co 1 s → ostrzeżenie, np. problem z połączeniem Wi-Fi/MQTT
  - miga co 0,5 s → błąd, np. ESPHome wykrył problem z czujnikiem

    ¹ Opcję można zmienić poprzez przełączenie encji Status LED

Encję **Status LED** najprościej znaleźć przez wyszukanie w `Rejestrze encji` lub przechodząc do panelu urządzenia `Ustawienia → Urządzenia oraz usługi → ESPHome` do sekcji **Sterowanie**:  
  
  <img width="292" height="36" alt="obraz" src="https://github.com/user-attachments/assets/888083f3-060c-4e4b-bd82-2f8fba1c5fa4" />


!!! info "Dioda statusowa"

    Dioda włączy się ponownie po zresetowaniu urządzenia. 
    Aby wyłączyć automatyczne zapalanie diody statusowej STA należy edytować plik `.YAML` 

---
## Wyłączenie automatycznego zapalania diody STA

1. Przejdź do `ESPHome Builder` (zakładka w menu po lewej stronie):

    <img width="200" alt="obraz" src="https://github.com/user-attachments/assets/25000b81-d563-45da-8053-3f9dc9ff7174" />

2. Wybierz edycję kodu klikając **EDIT**:  

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/3531764d-7d58-4168-9e69-c9f6bb7a7bfa" />

3. W sekcji `light` usuń parametr `restore_mode`, który odpowiada za automatyczne włączanie encji po restarcie:
    ```
    light:
    - platform: status_led
        name: "Status LED"
        pin:
        number: GPIO16     
        inverted: false
        restore_mode: ALWAYS_ON  ←  usuń tę linię
    ```
4. Kliknij w prawym górnym rogu **SAVE**, następnie **INSTALL**
5. Wybierz [**Manual download**](Pierwsza-konfiguracja-ESPHome#edycja-konfiguracji) lub [**Wirelessly**](Aktualizacja-bezprzewodowa-(OTA))
6. Po restarcie dioda już nie będzie się automatycznie zapalać - wciąż będzie informować o ostrzeżeniach i błedach
