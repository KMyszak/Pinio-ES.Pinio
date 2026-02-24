# Aktualizacja przez konsolę

Urządzenie można zaktualizować, korzystając z *wbudowanej konsoli* w **web UI Tasmota**, przez **MQTT** lub przy użyciu **web request**.

---

1. Połącz się z urządzeniem wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-adresu-ip-przypisanego-do-urzadzenia))
2. Wybierz opcję `Console`:   

    <img width="315" height="470" alt="obraz" src="https://github.com/user-attachments/assets/5473ac95-cf40-4051-81b0-8eb70c74fe02" />

3. Ustaw adres *URL OTA* za pomocą polecenia `OtaUrl` w konsoli:
    ``` yaml
    OtaUrl http://ota.tasmota.com/tasmota/tasmota.bin
    ```
    <img width="950" height="35" alt="obraz" src="https://github.com/user-attachments/assets/01b426d7-7b85-457f-aab7-88a4a68aae47" />

4. Rozpocznij aktualizację z serwera OTA, wpisując polecenie `Upgrade 1`:
    ``` yaml
    Upgrade 1
    ```
    <img width="950" height="64" alt="obraz" src="https://github.com/user-attachments/assets/deb04f79-3ecd-4e1e-9651-881803e855fd" />

5. Poczekaj na zakończenie procesu aktualizacji, a następnie sprawdź wersję Tasmota w konsoli, używając komendy `Status 2`:
    ``` yaml
    Status 2
    ```
    <img width="950" height="37" alt="obraz" src="https://github.com/user-attachments/assets/a783376d-b2f9-41ac-ab9f-04af6cb292cb" />
