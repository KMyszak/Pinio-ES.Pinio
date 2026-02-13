# Status urządzenia

<img width="203" height="249" align="left" alt="obraz" src="https://github.com/user-attachments/assets/a311e24b-7518-4c6c-97aa-9c195ab1cc30" />

Urządzenie domyślnie ma wgrany moduł `status_led.py`, który kontroluje pracę diody statusowej **STA** - użytkownik może go dostosować pod własne preferencje. 


Status diody STA:

  - włączona → urządzenie połączone z Home Assistant
  - cykl 1 s **ON** / 1 s **OFF** → proces łączenia z Wi-Fi
  - cykl 2 s **ON** / 2 s **OFF** → proces łączenia z MQTT 
  - dwa mignięcia co 2 s → uruchomiony Webserver¹ (tryb Access Point)

**¹ Webserver** - uruchamia się, gdy urządzenie ma problemy z połączeniem Wi-Fi lub MQTT.
Umożliwia on sprawdzenie oraz zmianę ustawień, a także zdalny restart urządzenia.



