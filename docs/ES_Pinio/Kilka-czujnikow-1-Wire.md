# Kilka identycznych czujników

Oprogramowanie Tasmota automatycznie wykrywa **nowe czujniki** (wybranego typu) po restarcie urządzenia, jeśli są podłączone do magistrali **1-Wire**.

Typ czujnika został wybrany podczas [**konfiguracji**](Podstawowe-ustawienia-i-GPIO.md) w ustawieniach `Module`:  

<img width="320" height="32" alt="obraz" src="https://github.com/user-attachments/assets/9fe54da8-d1d9-41fb-950a-a05f4453faa5" />

---

**Czujniki tego samego typu** należy podłączyć do portu **1-Wire** (1-W). Po restarcie urządzenia (np. przyciskiem *RST*) Tasmota automatycznie wykryje wszystkie podłączone czujniki.

Podłączony **jeden czujnik**:   
    <img width="720" height="147" alt="obraz" src="https://github.com/user-attachments/assets/85f1abae-a336-44d1-bf19-3c5e00b9334a" />

Podłączone **dwa czujniki**:   
    <img width="720" height="147" alt="obraz" src="https://github.com/user-attachments/assets/640302af-092f-426b-bce1-70669643f784" />

!!! info "Identyfikacja czujników"
    
    Każdy czujnik otrzymuje **unikalny identyfikator**, co zmienia jego **nazwę** i **powiązane encje** w systemie.  
    W przypadku kilku identycznych czujników należy je ręcznie dodać lub edytować w dashboardzie, aby zachować spójność i poprawną identyfikację pomiarów.

