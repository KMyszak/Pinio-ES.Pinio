# Pinio + ESPHome

Urządzenie oparte na **Raspberry Pi Pico W** (RP2040), zaprojektowane z myślą o nowoczesnej, lokalnej **automatyzacji budynków** - bez konieczności korzystania z chmury.

**Pinio** wyróżnia się elastycznością i otwartą architekturą - działając z **ESPHome** - co pozwala na szybką konfigurację i obsługę nawet bez specjalistycznej wiedzy programistycznej.

Moduł idealnie integruje się z ekosystemem **Home Assistant**, umożliwiając tworzenie funkcji wykonawczych, statusowych oraz pomiarowych. Doskonale sprawdza się zarówno w projektach hobbystycznych, jak i w profesjonalnych instalacjach automatyki budynkowej, pozwalając na szybkie uruchomienie automatyki z wykorzystaniem natywnego **ESPHome API** (kod YAML).

---

## Raspberry Pi Pico W

<img width="120" align="left" alt="obraz" src="https://github.com/user-attachments/assets/95632930-a802-40da-9c9a-f1d0e1fafafe" />

**Pinio** bazuje na mikrokontrolerze **Raspberry Pi Pico W** (RP2040), który działa z&nbsp;**ESPHome**, co pozwala na łatwą konfigurację i obsługę nawet bez wiedzy programistycznej.

**Raspberry Pi Pico W** to niewielka, energooszczędna płytka oparta na dwurdzeniowym układzie RP2040, wzbogacona o moduł Wi-Fi 2.4 GHz. Dzięki wbudowanemu Wi-Fi może pełnić rolę prostego serwera lub urządzenia działającego w trybie **Access Point**.  

Dzięki niskiemu poborowi mocy świetnie nadaje się do aplikacji **IoT**, czujników, sterowników oraz prostych urządzeń automatyki. 

<br>

## Funkcje

Zastosowane komponenty i funkcje gwarantują szerokie zastosowanie w automatyce budynkowej:

- **platforma:** natywne wsparcie ESPHome
- **interfejsy:** 2 wejścia cyfrowe, 2 przekaźniki (obciążalność 2 A), magistrala 1‑Wire
- **komunikacja:** Wi‑Fi 2.4 GHz, protokół MQTT, integracja z Home Assistant
- **zasilanie:** 12 VDC, bezpieczne złącze o niestandardowym rastrze
- **złącza:** GPIO, terminal‑block, wyjścia na diody statusu i przycisk reset
- **obudowa:** przystosowana do montażu na szynie DIN (TH35)
- **wsparcie:** przykładowy kod YAML w ESPHome, czytelna dokumentacja, brak ograniczeń licencyjnych

## Zastosowanie

**Pinio** z dodatkiem **ESPHome** doskonale sprawdzi się wszędzie tam, gdzie liczy się niezależność, szybkie przetwarzanie lokalne i prosta konfiguracja - to idealne rozwiązanie dla osób tworzących własne logiki automatyki na bazie Raspberry Pi. 

Obsługuje gotowe oprogramowanie **ESPHome**, dzięki czemu pozwala uruchomić i skonfigurować system z&nbsp;gotowym interfejsem. 

Urządzenie znajdzie zastosowanie m.in. w:

- **automatyce** domowej i lokalnej
- prototypowaniu i testach systemów **IoT**
- integracji z **MQTT**
- **edukacji** i **nauce** programowania mikrokontrolerów