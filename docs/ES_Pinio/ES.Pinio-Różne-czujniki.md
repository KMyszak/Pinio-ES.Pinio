# Różne czujniki

## Dostępne porty

Aby podłączyć czujniki różnego typu należy skorzystać z **portów rozszerzeń** oraz dostępnych GPIO:

- `GIPO15` 
- `GPIO2`
- `GPIO0`    

<img width="360" height="222" alt="gpios" src="https://github.com/user-attachments/assets/eb31f91a-447f-481a-ba9c-d804af1f10f6" />
    
---

## Zalecnia

Dla każdego urządzenia są przygotowane 2 porty, każdy z nich ma dostępne 4 piny: 

<img width="500" height="361" alt="obraz" src="https://github.com/user-attachments/assets/0e623a33-c352-4421-a106-4d1b1598bc19" />

Przy połączeniu należy mieć na uwadze kilka kwestii, ponieważ można podłączać inne elementy do `GPIO0`, `GPIO2` i `GPIO15`, ale trzeba uważać na ich stan przy starcie, żeby ESP-12F w ogóle się uruchomił:

1. Nie powinno się wymuszać niewłaściwego stanu podczas włączenia zasilania:

    - `GPIO15` → musi być **LOW** przy starcie, inaczej ESP-12F nie wystartuje
    - `GPIO2` → musi być **HIGH** przy starcie, inaczej ESP-12F nie wystartuje
    - `GPIO0` → musi być **HIGH** przy starcie, inaczej ESP-12F wejdzie w tryb flash/bootloader

2. Dopuszczalne są elementy, które nie wymuszają stanu **odwrotnego** jaki pin musi mieć przy starcie:

    - rezystory (pull-up/pull-down)
    - dioda LED z rezystorem (jeśli pin jest **HIGH** przy starcie)
    - czujniki, które mają wejście *high-impedance* (nie wpływają na stan)

3. Niebezpieczne elementy:

    - przekaźniki sterowane bezpośrednio z pinu, które mogą wprowadzić **LOW** lub **HIGH** w momencie zasilania
    - duże obciążenia, które mogą ściągnąć pin do niewłaściwego stanu
    - mają wewnętrzne pull-upy lub pull-downy niezgodne z wymaganym stanem

---

## Przykład

Przykład podłączenia dodatkowego czujnika pomiaru temperatury i wilgotności typu DHT11:

1. Połącz się z urządzeniem wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [Problemy :material-open-in-new:](ES.Pinio-problemy.md))
2. Przejdź do `Configuration → Module` i wybierz dla `GPIO2` opcję **DHT11**:  

    <img width="830" height="561" alt="obraz" src="https://github.com/user-attachments/assets/d558c59d-6d55-44cb-b45b-b8304474b153" />
    
    !!! Warning "Wybór `GPIO2`, ponieważ dla `GPIO15` urządzenie nie wystartuje - sensor podaje stan **HIGH**."

3. Podłącz czujnik w podobny sposób, zwróć uwagę na poprawne podłączenie zasilania czujnika (**GND** or **VCC**):  

    <img width="500" height="286" alt="obraz" src="https://github.com/user-attachments/assets/fe7138e2-16dc-43f7-ae08-f81cb6883bf3" />

4. Przy poprawnym podłączeniu powinien pojawić się odczyt na stronie czytnika oraz nowe encje w **Home Assistant**:  

    <img width="704" height="241" alt="obraz" src="https://github.com/user-attachments/assets/d8be9b8d-fc15-4115-af2f-0f694ede4e38" />
