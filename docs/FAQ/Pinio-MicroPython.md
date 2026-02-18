### Urządzenie lub jego encje nie są wykrywane przez MQTT

Jeżeli dane z `config.py`/`config.json` są poprawne zajrzyj do konsoli dodatku **MQTT**:   

1. Z menu po lewej stronie wybierz `Ustawienia → Dodatki → Mosquitto broker` i przejdź do zakładki **Logi**:
    
    <img width="680" alt="obraz" src="https://github.com/user-attachments/assets/f9ebe8fd-d0d9-4618-af19-5c7e242d3a74" />

    Jeżeli urządzenie jest widoczne w logach należy usunąć plik `mac.conf` z urządzenia (zostanie on utworzony ponownie, przez co konfiguracja encji zostanie załadowna ponownie):

    <img width="680" alt="obraz" src="https://github.com/user-attachments/assets/1117142b-35c7-4e46-8765-4c6ab9181c2a" />

2. Uruchom program **Thonny**
3. Podłącz **Pinio** do komputera przez kabel microUSB
4. Kliknij LPM w prawym dolnym rogu okna i wybierz z listy:

    <img width="344" height="104" alt="k_pinio_1" src="https://github.com/user-attachments/assets/6f237c7e-1fa1-431e-82ff-e6769c3e67df" />

5. W eksploratorze plików po lewej stronie znajdź i usuń `mac.conf`:  
    <img width="253" height="464" alt="obraz" src="https://github.com/user-attachments/assets/d58f1023-665f-41d8-a555-279ea1bcb606" />

    !!! Failure ""
    
        Jeśli nie widzisz żadnych plików, kliknij ikonę 🛑 lub wybierz opcję z zakładki `Run → Stop/Restart backend`:

        <img width="443" height="76" alt="obraz" src="https://github.com/user-attachments/assets/ba95bfcc-6982-4c98-aed1-ca798240fff1" />

6. Uruchom urządzenie - kliknij `F5` w programie lub przycisk `RST` na płytce
7. Powinny pojawić się logi:

    <img width="266" height="57" alt="obraz" src="https://github.com/user-attachments/assets/31c934e0-9fa8-4baa-a956-3aecf09b4d22" />

8. Po restarcie urządzenie powinno być poprawnie wykrywane przez **MQTT**
