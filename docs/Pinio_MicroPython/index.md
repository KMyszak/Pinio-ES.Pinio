# Pinio + MicroPython

Urządzenie bazuje na mikrokontrolerze **Raspberry Pi Pico2 W** (RP2350) i może być programowane w MicroPython, CircuitPython lub C/C++, co zapewnia dużą elastyczność dla programistów i hobbystów. 

Dzięki natywnej obsłudze **MQTT**, **PINIO** idealnie nadaje się jako interfejs wykonawczy, statusowy oraz pomiarowy w inteligentnych instalacjach.

## Raspberry Pi Pico 2W

<img width="120" align="left" alt="obraz" src="https://github.com/user-attachments/assets/97c0a89d-6ef3-4842-b0df-7edfab3ce55d" />

**Raspberry Pi Pico 2W** to ulepszona wersja popularnej płytki Pico W, wyposażona w nowszy i wydajniejszy układ RP2350, oferujący więcej mocy obliczeniowej i lepszą efektywność energetyczną. 

Urządzenie posiada zintegrowany moduł Wi-Fi 2.4 GHz oraz obsługę Bluetooth, co znacząco rozszerza jego możliwości komunikacyjne. Pico 2W zapewnia szeroki zestaw interfejsów - `GPIO`, `UART`, `SPI`, `I²C`, `PWM` oraz `ADC` - umożliwiając łatwe podłączenie czujników i układów peryferyjnych. 

Dzięki wsparciu dla MicroPythona, C/C++ i bogatej dokumentacji platforma jest przystępna dla początkujących, ale jednocześnie wystarczająco elastyczna do zastosowań profesjonalnych i **IoT**. 

## Funkcje

Zastosowane komponenty i funkcje gwarantują szerokie zastosowanie w automatyce budynkowej:
 
- **platforma:** możliwość programowania w MicroPython, CircuitPython lub C/C++
- **interfejsy:** 2 wejścia cyfrowe, 2 przekaźniki (2A), wsparcie magistrali 1‑Wire
- **komunikacja:** Wi‑Fi 2,4 GHz, protokół MQTT, integracja z Home Assistant
- **zasilanie:** 12 VDC, bezpieczne złącze o niestandardowym rastrze
- **złącza:** GPIO, terminal‑block, wyjścia na diody statusu i przycisk reset
- **obudowa:** przystosowana do montażu na szynie DIN (TH35)
- **zalety:** lokalne zarządzanie bez chmury, pełna integracja z Home Assistant, otwarta architektura

## Zastosowanie

PINIO wymaga samodzielnego programowania i może być konfigurowane przy użyciu MicroPython, CircuitPython lub C/C++.

Pozwala na tworzenie własnych aplikacji **IoT** i integrację z systemami takimi jak **Home Assistant** oraz **MQTT**, ale wymaga wgrania i dopasowania oprogramowania do indywidualnych potrzeb użytkownika. 

Urządznie znajdzie zastosowanie m.in. w:

- automatyce domowej i lokalnej (po programowaniu własnych funkcji)
- prototypowaniu i testach systemów IoT
- integracji z MQTT i innymi protokołami
- edukacji i nauce programowania mikrokontrolerów

## Wsparcie programisyczne

Do urządzenia dołączony jest przykładowy kod MicroPython, umożliwiający:

- sterowanie przekaźnikami
- odczyt stanów wejść
- obsługę czujników 1-Wire
- komunikację przez MQTT
- integrację z Home Assistant