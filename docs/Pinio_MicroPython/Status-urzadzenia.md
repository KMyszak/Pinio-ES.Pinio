# Status urządzenia

<img width="203" height="249" align="left" alt="obraz" src="https://github.com/user-attachments/assets/a311e24b-7518-4c6c-97aa-9c195ab1cc30" />

Urządzenie domyślnie posiada wgrany moduł `status_led.py`, który odpowiada za pracę diody statusowej **STA**. Moduł ten można dostosować do własnych potrzeb, modyfikując sposób sygnalizacji. 


Status diody STA:

  - włączona - urządzenie połączone z Home Assistant
  - cykl 1 s **ON** / 1 s **OFF** - łączenie z Wi-Fi
  - cykl 2 s **ON** / 2 s **OFF** - łączenie z MQTT 
  - dwa mignięcia co 2 s - uruchomiony Webserver (tryb *Access Point*)¹

---

**¹ Webserver** uruchamia się automatycznie, gdy urządzenie  napotka problem z połączeniem Wi-Fi lub MQTT.
Umożliwia on sprawdzenie konfiguracji, wprowadzenie zmian oraz wykonanie zdalnego restartu urządzenia.



