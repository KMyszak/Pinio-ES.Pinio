# Status urządzenia

<img width="203" alt="obraz" align="left" src="https://github.com/user-attachments/assets/a81b3409-c0bd-4fa9-9cbc-7a433915e9b0" />

Dioda statusowa **STA** sygnalizuje pracę urządzenia, a jej zachowanie można zmienić przy pomocy zmiennej `LedState`. **Domyślnie** w konsoli ustawiony jest tryb `4`.

Status diody STA:

  - **wyłączona** - urządzenie połączone z **Home Assistant**
  - **miganie** przy wysyłaniu subskrypcji/publikacji/stanów - poprawne działanie
  - cykl 1 s **ON** / 1 s **OFF** - proces łączenia z Wi-Fi 
  - cykl 2 s **ON** / 2 s **OFF** - proces łączenia z MQTT  


## Tryby diody STA

Dostępne tryby, które można wybrać poprzez zmianę wartości zmiennej `LedState` w [**konsoli**](Konsola.md):  


| Wartość | Opis                                                                      |
|   :-:   |  :--                                                                      |
|  **0**  | Wyłącz użycie diody STA                                                   |
|  **1**  | Pokaż stan zasilania[^1] (dioda STA włączonona, gdy zasilanie włączone)      |
|  **2**  | Pokaż subskrypcje MQTT jako miganie diody STA                             |
|  **3**  | Pokaż stan zasilania[^1] i subskrypcje MQTT jako miganie diody STA           |
|  **4**  | Pokaż publikacje MQTT jako miganie diody STA                              |
|  **5**  | Pokaż stan zasilania[^1] i publikacje MQTT jako miganie diody STA            |
|  **6**  | Pokaż wszystkie wiadomości MQTT jako miganie diody STA                    |
|  **7**  | Pokaż stan zasilania[^1] i wszystkie wiadomości MQTT jako miganie diody STA  |

[^1]: Przełączenie któregokolwiek wyjścia w stan **ON** powoduje ciągłe świecenie diody STA.

