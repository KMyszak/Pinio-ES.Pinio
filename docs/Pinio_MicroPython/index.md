# Pinio + MicroPython

Urządzenie bazuje na mikrokontrolerze **Raspberry Pi Pico2 W** (RP2350), może być programowane w&nbsp;MicroPythonie, CircuitPythonie lub C/C++ co zapewnia dużą elastyczność dla programistów i&nbsp;hobbystów. 

Dzięki natywnej obsłudze **MQTT**, **Pinio** idealnie nadaje się jako interfejs wykonawczy, statusowy oraz pomiarowy w inteligentnych instalacjach.

---

## Raspberry Pi Pico 2W

<img width="100" align="left" alt="obraz" src="https://github.com/user-attachments/assets/97c0a89d-6ef3-4842-b0df-7edfab3ce55d" />

**Raspberry Pi Pico 2W** to ulepszona wersja popularnej płytki **Pico W**, wyposażona w&nbsp;nowszy i wydajniejszy układ, oferujący więcej mocy obliczeniowej i lepszą efektywność energetyczną. 

Urządzenie posiada zintegrowany moduł Wi-Fi 2.4 GHz oraz obsługę Bluetooth, co znacząco rozszerza jego możliwości komunikacyjne.

Dzięki wsparciu dla popularnych języków programowania i bogatej dokumentacji platforma jest przystępna dla początkujących, ale jednocześnie wystarczająco elastyczna do zastosowań profesjonalnych. 

## Funkcje
 
- **platforma:** programowanie w MicroPythonie, CircuitPythonie lub C/C++
- **interfejsy:** 2 wejścia cyfrowe, 2 przekaźniki (obciążalność 2 A), magistrala 1‑Wire
- **komunikacja:** Wi‑Fi 2.4 GHz, protokół MQTT, integracja z Home Assistant
- **zasilanie:** 12 V DC, bezpieczne złącze o niestandardowym rastrze
- **złącza:** GPIO, terminal‑block, wyjścia na diody statusu i przycisk reset
- **obudowa:** przystosowana do montażu na szynie DIN (TH35)
- **wsparcie:** dołączony kod MicroPython

## Zastosowanie

**Pinio** pozwala na tworzenie własnych aplikacji **IoT** i integrację z systemami takimi jak **Home Assistant** oraz **MQTT**, ale wymaga wgrania i dopasowania oprogramowania do indywidualnych potrzeb użytkownika. 

Urządzenie znajdzie zastosowanie m.in. w:

- automatyce domowej i lokalnej (po zaimplementowaniu własnych funkcji)
- prototypowaniu i testach systemów IoT
- integracji z MQTT
- edukacji i nauce programowania mikrokontrolerów

## Wsparcie programistyczne

Do urządzenia dołączony jest przykładowy kod MicroPython, umożliwiający:

- sterowanie przekaźnikami
- odczyt stanów wejść
- obsługę czujników 1-Wire
- komunikację przez MQTT
- integrację z Home Assistant