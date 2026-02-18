# Podstawowe ustawienia

W kolejnym kroku zostaną ustawione podstawowe parametry urządzenia, w tym wgrany odpowiedni template definiujący układ pinów **GPIO**. Po aktywacji szablonu w sekcji `Module` przypisane zostaną funkcje poszczególnym wyprowadzeniom: 

- dwa wejścia **cyfrowe**
- dwa wyjścia **przekaźnikowe** 
- **czujnik temperatury** DS18x20
- **dioda statusowa** (STA), sygnalizująca pracę urządzenia

Po zapisaniu ustawień **ES.Pinio** automatycznie uruchomi się ponownie i zacznie działać zgodnie z nowym układem **GPIO**.

---

1. Połącz się z urządzeniem wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-przypisanego-ip-do-urzadzenia))
2. Przejdź do `Configuration → Other`:
    <img width="643" height="478" alt="obraz" src="https://github.com/user-attachments/assets/3c10d388-3a8a-4dd2-bdb4-b5d0f06f5062" />

3. Wklej poniższy szablon w miejsce **Template** oraz zaznacz pole **Activate**:
    ```
    {"NAME":"ES.PINIO","GPIO":[1,1,1,1,1,1,0,0,1,1,1,1,1,1],"FLAG":0,"BASE":18}  
    ```
    <img width="317" alt="obraz" src="https://github.com/user-attachments/assets/11c39631-1210-4809-9cc4-a03ad0a94585" />

    !!! note "Upewnij się, że pole **MQTT enable** jest zaznaczone"
    !!! tip "W tym miejscu można zmienić nazwę urządzenia (Device Name) oraz nazwy obu wyjść (przekaźników) *Friendly Name 1* i *Friendly Name 2*"
    
4. Kliknij **Save** - po zapisaniu urządzenie zrestartuje się i użyje nowych ustawień **GPIO**

5. Przejdź do `Configuration → Module`:  
    <img width="643" height="478" alt="obraz" src="https://github.com/user-attachments/assets/1ba02bff-9585-4992-a558-2494f53a0d8e" />

6. Wprowadź:    
    <img width="317" alt="obraz" src="https://github.com/user-attachments/assets/0f135452-61f2-4236-9124-1042230f999e" />

7. Kliknij **Save**, aby zapisać zmiany 
8. Przejdź do zmian w [**Konsoli**](Konsola.md)