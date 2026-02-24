# Ręczna aktualizacja

!!! quote "Aktualizacja dla urządzeń ES.Pinio *BEZ* wbudowanego konwertera wymaga *osobnego* konwertera USB-UART"

[**Rekomendowane połączenie**](../Firmware/ES_Pinio.md#__tabbed_2_1)

- wykorzystuje linie sygnałowe konwertera USB-UART (**RX, TX**)  
- zasilanie zapewnia moduł **ES.Pinio** (**12 V DC**)
- zapobiega ryzyku uszkodzenia układu **ESP-12F**, które mogłoby nastąpić przy podaniu napięcia **wyższego niż 3,3 V**

[**Alternatywne połączenie**](../Firmware/ES_Pinio.md#__tabbed_2_2)

- wykorzystuje połączenie **ES.Pinio** ⇄ konwerter USB-UART (**RX, TX, GND** oraz **VCC**)
- należy bezwarunkowo **upewnić się**, że pin `VCC` konwertera podaje **DOKŁADNIE 3,3 V**
- niewłaściwe napięcie może **trwale uszkodzić układ**

---

!!! quote "Aktualizacja dla urządzeń ES.Pinio z wbudowanym konwerterem"

[**Wykorzystanie programu Tasmotizer**](../Firmware/ES_Pinio.md#__tabbed_1_2)

- wymagane **jedynie** podpięcie **ES.Pinio** przez przewód Micro-USB
- dedykowany program **Tasmotizer**
- możliwość zmiany podstawowych ustawień **Tasmota** w programie