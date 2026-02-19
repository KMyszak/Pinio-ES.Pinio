# Pinio + ESPHome

Urządzenie oparte na **Raspberry Pi Pico W** (RP2040), zaprojektowane z myślą o nowoczesnej, lokalnej **automatyzacji budynków**, bez konieczności korzystania z chmury.

**Pinio** wyróżnia się elastycznością i otwartą architekturą - działa **ESPHome**, co pozwala na szybką konfigurację i obsługę nawet bez specjalistycznej wiedzy programistycznej.

Doskonale integruje się z ekosystemem **Home Assistant**, umożliwiając tworzenie funkcji wykonawczych, statusowych oraz pomiarowych. Sprawdza się zarówno w projektach hobbystycznych, jak i&nbsp;w&nbsp;profesjonalnych instalacjach automatyki budynkowej - z szybkim wdrożeniem dzięki ESPHome API (YAML).

---

## Raspberry Pi Pico W

<img width="100" align="left" alt="obraz" src="https://github.com/user-attachments/assets/95632930-a802-40da-9c9a-f1d0e1fafafe" />

**Raspberry Pi Pico W** to niewielka, energooszczędna płytka oparta na dwurdzeniowym układzie RP2040, wzbogacona o moduł Wi-Fi 2.4 GHz. Dzięki wbudowanemu Wi-Fi może pełnić rolę prostego serwera lub urządzenia działającego w trybie własnego punktu dostępowego (*Access Point*).  

Mikrokontroler działa z **ESPHome**, co pozwala na łatwą konfigurację i obsługę nawet bez zaawansowanej wiedzy programistycznej.

Ze względu na niski pobór mocy doskonale nadaje się do projektów **IoT**, czujników, sterowników i prostych systemów automatyki. 

## Funkcje

- **platforma:** pełna zgodność z ESPHome
- **interfejsy:** 2 wejścia cyfrowe, 2 przekaźniki (obciążalność 2 A), magistrala 1‑Wire
- **komunikacja:** Wi‑Fi 2.4 GHz, protokół MQTT, integracja z Home Assistant
- **zasilanie:** 12 V DC, bezpieczne złącze o niestandardowym rastrze
- **złącza:** GPIO, terminal‑block, wyjścia na diody statusu i przycisk reset
- **obudowa:** przystosowana do montażu na szynie DIN (TH35)
- **wsparcie:** przykładowy kod YAML w ESPHome, czytelna dokumentacja, brak ograniczeń licencyjnych

## Zastosowanie

Moduł z **ESPHome** doskonale sprawdzi się tam, gdzie liczy się niezależność, lokalne przetwarzanie i&nbsp;szybka konfiguracja - idealny do tworzenia własnej logiki automatyki opartej na **Raspberry Pi Pico W**. 

Urządzenie znajdzie zastosowanie m.in. w:

- automatyce domowej i lokalnej
- prototypowaniu i testach systemów IoT
- integracji z MQTT
- edukacji i nauce programowania mikrokontrolerów