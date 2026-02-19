# Backup ustawień

**Tasmota** umożliwia wykonanie kopii zapasowej konfiguracji urządzenia poprzez web UI. Backup zapisuje wszystkie **ustawienia**, **GPIO**, **template** i **konfigurację MQTT**, aby można je było łatwo przywrócić w tym samym lub innym urządzeniu.

---

## Tworzenie Backupu

1. Połącz się z urządzeniem, wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-przypisanego-ip-do-urzadzenia))
2. Przejdź do `Configuration` i kliknij `Backup`:  
    <img width="643" height="659" alt="obraz" src="https://github.com/user-attachments/assets/acef971e-61bc-42c8-bce9-37f6e4b0c9c9" />

3. Zostanie pobrany plik backupu `.dmp`:   
    <img width="438" height="90" alt="obraz" src="https://github.com/user-attachments/assets/9c015ff5-914f-4d7a-b083-dc7349fce4aa" />

---

## Przywrócenie backupu

1. Połącz się z urządzeniem, wpisując jego **adres IP** w przeglądarce
2. Przejdź do `Configuration → Restore`:  
    <img width="643" height="659" alt="obraz" src="https://github.com/user-attachments/assets/6cc35296-c846-4935-9630-e8a31a5316f8" />

3. Wybierz odpowiedni plik backupu `.dmp` i kliknij **Start restore**:   
    <img width="317" alt="obraz" src="https://github.com/user-attachments/assets/179dc3b7-2b3d-455e-bf15-d4148722a846" />
    
4. Po poprawnym zakończeniu procesu pojawi się komunikat:
    <img width="317" alt="499364558-39430a16-5a88-42b0-81b3-67de6410770e" src="https://github.com/user-attachments/assets/3c8dcdb2-e858-4819-9fe3-6dad6a507a7e" />
