# Staus urządzenia
<img width="220" alt="obraz" align="left" src="https://github.com/user-attachments/assets/a81b3409-c0bd-4fa9-9cbc-7a433915e9b0" />

Dioda statusu **STA** sygnalizuje pracę urządzenia, a jej zachowanie można zmienić przy pomocy zmiennej `LedState`. Przez zmiany w konsoli ustawiony jest `tryb 4`.



Status diody STA:

  - **wyłączona** → urządzenie połączone z **Home Assistant**
  - **miganie** przy wysyłaniu subskrypcji/publikacji/stanów → poprawne działanie
  - cykl 1s **ON** / 1s **OFF** → proces łączenia z WiFi 
  - cykl 2s **ON** / 2s **OFF** → proces łączenia z MQTT  


## Tryby diody STA

Dostępne tryby, które można wybrać poprzez zmianę wartości zmiennej `LedState` w [**konsoli**](../../ES_Pinio/Konsola):  


| Wartość | Opis                                                              |
|:-:|:--|
| **0** | Wyłącz użycie LED                                                   |
| **1** | Pokaż stan zasilania¹ na LED (LED włączony, gdy zasilanie włączone) |
| **2** | Pokaż subskrypcje MQTT jako miganie LED                             |
| **3** | Pokaż stan zasilania¹ i subskrypcje MQTT jako miganie LED           |
| **4** | Pokaż publikacje MQTT jako miganie LED                              |
| **5** | Pokaż stan zasilania¹ i publikacje MQTT jako miganie LED            |
| **6** | Pokaż wszystkie wiadomości MQTT jako miganie LED                    |
| **7** | Pokaż stan zasilania¹ i wszystkie wiadomości MQTT jako miganie LED  |

¹ **Pokaż stan zasilania** - przełączenie któregokolwiek wyjścia w stan **ON** powoduje ciągłe świecenie diody 

