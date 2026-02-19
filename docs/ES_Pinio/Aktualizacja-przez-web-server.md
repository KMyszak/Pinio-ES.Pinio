# Aktualizacja przez web server

**Tasmota** posiada wbudowany web serwer, który umożliwia bezpośrednią aktualizację oprogramowania (firmware) bez konieczności używania dodatkowych narzędzi. Poniższe kroki pokazują, jak wgrać najnowszą wersję.

---

1. Połącz się z urządzeniem, wpisując jego adres **IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-przypisanego-ip-do-urzadzenia))
2. Przejdź do `Firmware Upgrade`:  

    <img width="292" height="479" alt="obraz" src="https://github.com/user-attachments/assets/f64de808-4432-4d9c-9289-acd0e9f9db5b" />
    !!! info "URL"
    
        Upewnij się, że podany URL wskazuje najnowszą wersję firmware na oficjalnej stronie Tasmota:

        [https://ota.tasmota.com/tasmota/ :material-open-in-new:](https://ota.tasmota.com/tasmota/)   
    !!! warning "URL najnowszej wersji"

        Domyślny URL aktualizuje urządzenie do najnowszej wersji:   
        ***http://ota.tasmota.com/tasmota/tasmota.bin.gz***
        
        <img width="900" height="224" alt="obraz" src="https://github.com/user-attachments/assets/0e07bcd9-5430-4a01-b7f3-aec1da2b2348" />

3. Kliknij **Start upgrade** - urządzenie się zrestartuje:    
    <img width="292" height="479" alt="obraz" src="https://github.com/user-attachments/assets/72f6e013-5dd6-4dc9-8a48-95394db462f5" />
 
4. Po automatycznym restarcie strona główna pokaże **MINIMAL firmware**, a po kolejnym restarcie zostanie wczytany aktualny stan wyprowadzeń GPIO, co oznacza zakończenie aktualizacji.   

    Odświeżenie strony spowoduje wczytanie wszystkich modułów: 
    <img width="900" height="451" alt="obraz" src="https://github.com/user-attachments/assets/9f8db5ef-b914-4634-abc2-0cb2aaddf0fc" />
    !!! tip "Weryfikacja wersji"
    
        Widoczna w dolnej części okna ***wersja firmware*** powinna odpowiadać pobranej wersji.