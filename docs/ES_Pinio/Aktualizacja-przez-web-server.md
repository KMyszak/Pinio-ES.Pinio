# Aktualizacja przez web server

**Tasmota** posiada wbudowany web serwer, który umożliwia bezpośrednią aktualizację firmware bez konieczności używania dodatkowych narzędzi. Poniższe kroki pokazują, jak wgrać najnowszą wersję - po zakończeniu aktualizacji strona web serwera odświeży się i pokaże aktualny stan **GPIO**.

---

1. Połącz się z urządzeniem wpisując jego adres IP w przeglądarce (w razie trudności zajrzyj do [**Problemy**](../FAQ/ES.Pinio.md))
2. Przejdź do `Firmware Upgrade`:  

    <img width="292" height="479" alt="obraz" src="https://github.com/user-attachments/assets/f64de808-4432-4d9c-9289-acd0e9f9db5b" />
    !!! info "URL"
    
        Upewnij się, że URL odnosi się do najnowszej wersji na oficjalnej stronie:

        [https://ota.tasmota.com/tasmota/ :material-open-in-new:](https://ota.tasmota.com/tasmota/)   
    !!! warning "URL najnowszej wersji"

        Domyślny URL powinien aktualizować urządzenie do najnowszej wersji:  
        http://ota.tasmota.com/tasmota/tasmota.bin.gz 
        <img width="900" height="224" alt="obraz" src="https://github.com/user-attachments/assets/0e07bcd9-5430-4a01-b7f3-aec1da2b2348" />

3. Kliknij `Start upgrade` - urządzenie się zrestartuje:    
    <img width="292" height="479" alt="obraz" src="https://github.com/user-attachments/assets/72f6e013-5dd6-4dc9-8a48-95394db462f5" />
 
4. Po pierwszym automatycznym restarcie na stronie głównej pojawi się **MINIMAL firmware**, po drugim zostanie wczytany aktualny stan **GPIO** - aktualizacja jest zakończona.    

    Odświeżenie strony wczyta wszystkie moduły:   
    <img width="900" height="451" alt="obraz" src="https://github.com/user-attachments/assets/9f8db5ef-b914-4634-abc2-0cb2aaddf0fc" />
    !!! tip "Widoczna w dolnej części okna wersja firmware powinna odpowiadać pobranej wersji"