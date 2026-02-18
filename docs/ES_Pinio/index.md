# ES.Pinio

To innowacyjne, wszechstronne urządzenie stworzone z myślą o wygodnej, elastycznej i nowoczesnej automatyzacji budynków, które działa **lokalnie**, bez potrzeby korzystania z chmury. 

Moduły cechują się modularnością, otwartą architekturą i łatwą integracją z ekosystemem **Home Assistant** - świetnie sprawdzą się zarówno u elektroników-hobbystów, jak i w poważniejszych projektach automatyki budynkowej.

---

## ESP8266

<img width="100" align="left" alt="obraz" src="https://github.com/user-attachments/assets/8a0cd199-bdbc-4d80-90ab-479d53e1bae6" />

**ES.PINIO** bazuje na popularnym układzie **ESP8266** (ESP-12F), dzięki czemu urządzenie jest kompatybilne z oprogramowaniem **Tasmota**, **ESPHome**, a także pozwala na własny firmware (np. Arduino IDE, PlatformIO, ESP-IDF). 

**ESP8266** w wersji ESP-12F to kompaktowy moduł Wi-Fi, popularny w projektach **IoT** dzięki niskiej cenie i dobrej wydajności. 

Posiada wbudowaną antenę PCB o **lepszym zasięgu** niż wcześniejsze wersje oraz **4 MB** pamięci Flash. Obsługuje tryby **STA**, **AP** i **AP+STA**, umożliwiając zarówno podłączenie do sieci Wi-Fi, jak i tworzenie własnego Access Pointa. 

## Funkcje

Zastosowane komponenty i funkcje gwarantują szerokie zastosowanie w automatyce budynkowej:
 
- **platforma:** natywne wsparcie Tasmota i ESPHome
- **interfejsy:** 2 wejścia cyfrowe, 2 wyjścia przekaźnikowe (obciążalność 2 A), magistrala 1‑Wire
- **komunikacja:** Wi‑Fi 2.4 GHz, protokół MQTT, integracja z Home Assistant
- **zasilanie:** 12 VDC, bezpieczne złącze o niestandardowym rastrze
- **złącza:** GPIO, terminal‑block, wyjścia na diody statusu i przycisk reset
- **obudowa:** przystosowana do montażu na szynie DIN (TH35)
- **wsparcie:** szczegółowa dokumentacja, instrukcja krok-po-kroku podłączenia do MQTT i konfiguracji w&nbsp;Home Assistant

## Zastosowanie

ES.PINIO sprawdzi się doskonale jako rozwiązanie typu *plug&play* do sterowania urządzeniami przez **Home Assistant**, bez potrzeby samodzielnego pisania kodu. 

Obsługuje gotowe otwartoźródłowe oprogramowanie **Tasmota**, dzięki czemu pozwala uruchomić i&nbsp;skonfigurować system z gotowym interfejsem. 

Urządzenie znajdzie zastosowanie m.in. w:

- **automatyce** domowej i lokalnej
- prototypowaniu i testach systemów **IoT**
- integracji z **MQTT**
- **edukacji** i **nauce** programowania mikrokontrolerów
