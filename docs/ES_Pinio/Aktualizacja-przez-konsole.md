# Aktualizacja przez konsolę

Urządzenie można zaktualizować za pomocą **MQTT**, **web request** lub **Konsoli** w web UI.

---

1. Przejdź na stronę główną urządzenia - wpisz jego **adres IP** w przeglądarce lub kliknij `Main Menu`
2. Wybierz opcję `Console`:   
    <img width="315" height="470" alt="obraz" src="https://github.com/user-attachments/assets/5473ac95-cf40-4051-81b0-8eb70c74fe02" />

3. Ustaw adres OTA za pomocą polecenia `OtaUrl`:
    ```
    OtaUrl http://ota.tasmota.com/tasmota/tasmota.bin
    ```
    <img width="950" height="35" alt="obraz" src="https://github.com/user-attachments/assets/01b426d7-7b85-457f-aab7-88a4a68aae47" />

4. Rozpozcznij aktualizację z serwera OTA:
    ```
    Upgrade 1
    ```
    <img width="950" height="64" alt="obraz" src="https://github.com/user-attachments/assets/deb04f79-3ecd-4e1e-9651-881803e855fd" />

5. Poczekaj na zakończenie procesu aktualizacji, a następnie sprawdź wersję Tasmota. W konsoli możesz użyć komendy `Status 2`:
    ```
    Status 2
    ```
    <img width="950" height="37" alt="obraz" src="https://github.com/user-attachments/assets/a783376d-b2f9-41ac-ab9f-04af6cb292cb" />
