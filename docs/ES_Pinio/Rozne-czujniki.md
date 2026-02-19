# Różne czujniki

**Tasmota** i moduły **ESP8266** obsługują wiele rodzajów sensorów, co pozwala podłączyć np. temperaturę, wilgotność czy ruch. Jedno wyjście **GPIO** może być przypisane do jednego typu czujnika, dlatego dla wielu różnych czujników należy używać osobnych portów.

---

## Dostępne porty

<img width="250" align="right" alt="gpios" src="https://github.com/user-attachments/assets/eb31f91a-447f-481a-ba9c-d804af1f10f6" />

Aby podłączyć czujniki różnego typu, należy skorzystać z **portów rozszerzeń** oraz dostępnych GPIO:

- `GPIO15` 
- `GPIO2`
- `GPIO0`    

## Ogólne wytyczne

<img width="250" align="left" alt="obraz" src="https://github.com/user-attachments/assets/d139baaf-f411-4184-a5ea-4c3d82606c8a" />

Każde urządzenie posiada **dwa 4-pinowe porty rozszerzeń** z dodatkowymi wyprowadzeniami do szybkiego montażu czujników i innych elementów. 

Przy podłączaniu różnych elementów do pinów `GPIO0`, `GPIO2` i `GPIO15` należy zwrócić uwagę na ich **stan przy starcie urządzenia**, aby ESP-12F uruchomił się poprawnie.

<br>

**Nie** powinno się wymuszać niewłaściwego stanu podczas włączenia zasilania:

1. `GPIO15` → musi być **LOW** przy starcie
2. `GPIO2` → musi być **HIGH** przy starcie
3. `GPIO0` → musi być **HIGH** przy starcie, inaczej ESP-12F wejdzie w tryb *flash*/*bootloader*

### Elementy bezpieczne
- rezystory pull-up/pull-down
- diody LED z rezystorem (jeśli pin jest **HIGH** przy starcie)
- czujniki o wysokiej impedancji (*high-impedance*)

### Elementy niebezpieczne
- bezpośrednio podłączone przekaźniki  
- duże obciążenia zmieniające stan pinu przy starcie
- urządzenia z wewnętrznymi pull-up/pull-down niezgodnymi z wymaganym stanem

## Przykład

Podłączenie dodatkowego czujnika pomiaru temperatury i wilgotności typu **DHT11**:

1. Połącz się z urządzeniem wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-przypisanego-ip-do-urzadzenia))
2. Przejdź do `Configuration → Module` i wybierz dla `GPIO2` opcję **DHT11**:  
    <img width="830" height="561" alt="obraz" src="https://github.com/user-attachments/assets/d558c59d-6d55-44cb-b45b-b8304474b153" />
    
    !!! Warning "Wybierz *GPIO2*, ponieważ *GPIO15* musi być w stanie **LOW** przy starcie. Podłączenie czujnika do *GPIO15* może uniemożliwić uruchomienie urządzenia"

3. Podłącz czujnik w podobny sposób - zwróć uwagę na poprawne podłączenie zasilania czujnika (**GND** oraz **VCC**):  
    <img width="500" height="286" alt="obraz" src="https://github.com/user-attachments/assets/fe7138e2-16dc-43f7-ae08-f81cb6883bf3" />

4. Po poprawnym podłączeniu odczyt powinien pojawić się w interfejsie webowym urządzenia, a nowe encje w **Home Assistant** będą dostępne do dalszej integracji:  
    <img width="750" alt="obraz" src="https://github.com/user-attachments/assets/d8be9b8d-fc15-4115-af2f-0f694ede4e38" />
