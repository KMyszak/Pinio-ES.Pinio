# MQTT

## Czym jest MQTT?

**MQTT (Message Queuing Telemetry Transport)** to lekki protokół komunikacyjny stworzony z myślą o urządzeniach IoT - małych, energooszczędnych i często działających w niestabilnych sieciach.

Działa w modelu **publish/subscribe**:

- urządzenia **publikują** dane na określonych "tematach" (*topics*)
- inne urządzenia lub aplikacje **subskrybują** te tematy, aby odbierać wiadomości

---

## Jak to działa w praktyce?

- urządzenie nawiązuje połączenie z siecią Wi-Fi
- łączy się z serwerem MQTT (tzw. *brokerem*)
- **publikuje** dane (np. temperaturę) na określony topic
- **nasłuchuje** poleceń wysyłanych na inny topic

---

## Dlaczego MQTT?

- bardzo niskie zużycie danych
- dobrze działa w niestabilnych sieciach
- obsługuje dwukierunkową komunikację między urządzeniem a chmurą
- kompatybilny z popularnymi brokerami, m.in. Mosquitto

!!! tip ""

    Dowiedz się więcej, czym jest MQTT z artykułów [**MQTT Essentials :material-open-in-new:**](https://www.hivemq.com/mqtt/)