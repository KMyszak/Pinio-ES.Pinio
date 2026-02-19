# Edycja config.py

W pliku `config.py` znajduje się słownik `default_config`, który przechowuje **domyślną konfigurację** połączenia Wi‑Fi i MQTT.

Parametry te zostaną zapisane do config.json po pierwszym uruchomieniu urządzenia.

---

| Parametr            | Opis                               |
|---------------------|------------------------------------|
| **wifi_ssid**       | Nazwa sieci Wi-Fi                  |
| **wifi_password**   | Hasło do Wi-Fi                     |
| **mqtt_broker**     | Adres IP brokera MQTT              |
| **mqtt_port**       | Port brokera (domyślnie: 1883)     |
| **mqtt_user**       | Nazwa użytkownika MQTT             |
| **mqtt_password**   | Hasło użytkownika MQTT             |
| **lwt_topic**       | Temat wiadomości *birth i *will*   |
| **discovery_prefix**| Prefiks wykrywania                 |

!!! warning "Plik *config.json*"

    Po wprowadzeniu zmian usuń plik *conifg.json* (jeśli istnieje).  
    Zostanie on utworzony ponownie przy starcie urządzenia - już z aktualnymi danymi.    
    Kolejne zmiany najlepiej wprowadzać właśnie w pliku `config.json`.   

!!! info "Zmienne"

    Wartości zmiennych powinny być **identyczne** z tymi ustawionymi w integracji **MQTT** w **Home Assistant**
