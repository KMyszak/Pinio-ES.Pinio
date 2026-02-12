# Podstawowe ustawienia i GPIO

1. Połącz się z urządzeniem wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**Problemy :material-open-in-new:**](ES.Pinio-problemy))
2. Przejdź do `Configuration → Other`:
    <img width="643" height="478" alt="obraz" src="https://github.com/user-attachments/assets/3c10d388-3a8a-4dd2-bdb4-b5d0f06f5062" />

3. Wklej poniższy szablon w miejsce **Template** oraz zaznacz pole **Activate**:
    ```
    {"NAME":"ES.PINIO","GPIO":[1,1,1,1,1,1,0,0,1,1,1,1,1,1],"FLAG":0,"BASE":18}  
    ```
    <img width="317" height="742" alt="obraz" src="https://github.com/user-attachments/assets/4cab1f12-50f1-472f-9b7c-0f5479145859" />

    !!! note "Upewnij się, że pole **MQTT enable** jest zaznaczone"
    !!! tip "W tym miejscu można zmienić nazwę urządzenia (Device Name) oraz nazwy obu wyjść (przekaźników) *Friendly Name 1* i *Friendly Name 2*"
    
4. Kliknij **Save** - po zapisaniu urządzenie zrestartuje się i użyje nowych ustawień GPIO

5. Przejdź do `Configuration → Module`:  

    <img width="643" height="478" alt="obraz" src="https://github.com/user-attachments/assets/1ba02bff-9585-4992-a558-2494f53a0d8e" />

6. Wprowadź:    

    <img width="317" height="686" alt="obraz" src="https://github.com/user-attachments/assets/75621b1e-e1d6-4cb5-885b-a590bda74a0b" />

7. Kliknij **Save**, aby zapisać zmiany 
8. Przejdź do zmian w [**konsoli :material-open-in-new:**](Konsola.md)