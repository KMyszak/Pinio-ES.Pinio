# Edycja config.py

W pliku `config.py` w znajdziesz `default_config` - domyślną konfigurację połączenia Wi-Fi i MQTT:

| Parametr            | Opis                               |
|---------------------|------------------------------------|
| **wifi_ssid**       | Nazwa sieci Wi-Fi                  |
| **wifi_password**   | Hasło do Wi-Fi                     |
| **mqtt_broker**     | Adres IP brokera MQTT              |
| **mqtt_port**       | Port brokera (domyślnie: 1883)     |
| **mqtt_user**       | Nazwa użytkownika MQTT             |
| **mqtt_password**   | Hasło użytkownika MQTT             |
| **lwt_topic**       | Temat wiadomości "birth" i "will"  |
| **discovery_prefix**| Prefiks wykrywania                 |

!!! warning "Po wprowadzonych zmianach USUŃ plik `conifg.json` (jeśli został utworzony) - zostanie on utworzony na nowo z poprawnymi danymi, a kolejne zmiany najlepiej wprowadzać przez `conifg.json`"

!!! info "Wartości powinny być identyczne jak te ustawione w konfiguracji **MQTT** w **Home Assistant**"
