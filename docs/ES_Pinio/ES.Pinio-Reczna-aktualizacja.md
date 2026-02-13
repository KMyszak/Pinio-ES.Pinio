# Ręczna aktualizacja

!!! quote "Opcje dla urządzeń ES.Pinio *BEZ* wbudowanego konwertera - wymagany jest *osobny* konwerter USB-UART"

[Rekomendowane połączenie :material-open-in-new:](../../Firmware/ES_Pinio/#__tabbed_2_1):

- wykorzystuje linie sygnałowe konwertera USB–UART (**RX, TX**)  
- zasilanie zapewnia moduł ES.Pinio (**12 VDC**)
- zapobiega ryzyku uszkodzenia układu ESP-12F, które mogłoby nastąpić przy podaniu napięcia wyższego niż 3,3 V na pin zasilania

[Alternatywne połączenie :material-open-in-new:](../../Firmware/ES_Pinio/#__tabbed_2_2):

- wykorzystuje połączenie ES.Pinio ⇄ konwerter USB–UART (**RX, TX, GND** oraz **VCC**)
- należy bezwarunkowo **upewnić się**, że pin `VCC` konwertera podaje **dokładnie** 3,3 V (🛑 **NIE** 5 V)
- niewłaściwe napięcie może trwale uszkodzić układ

---

!!! quote "Dla urządzeń ES.Pinio z wbudowanym konwerterem"

[Wykorzystanie programu Tasmotizer :material-open-in-new:](../../Firmware/ES_Pinio/#__tabbed_1_2):

- wymagane jedynie podpięcie ES.Pinio do komputera przez przewód microUSB oraz dedykowany program
- prosta i intuicyjna obsługa
- dodatkowa możliwość zmiany podstawowych ustawień Tasmota - zmiana ustawień Wi-Fi, MQTT czy backup firmware