# Kilka czujników

Podłączone **nowe** czujniki zostaną dopiero wykryte przy kolejnym utworzeniu integracji przez moduł `mqtt_creator.py`.

---

1. Podłącz urządzenie do komputera przez kabel Micro-USB
2. Otwórz jego pliki w programie, np. przez [**Thonny :material-open-in-new:**](https://thonny.org/)
3. Usuń plik `mac.conf`   
 
    !!! info "Plik zostanie wygenerowany ponownie przy starcie urządzenia"    

4. Uruchom urządzenie ponownie - klikając `F5` w **Thonny** lub naciskajac fizyczny przycisk **RST**
5. W konsoli programu powinien pojawić się komunikat:

    <img width="409" height="84" alt="obraz" src="https://github.com/user-attachments/assets/eb2773a5-7d06-49e5-9aab-111007ecf407" />

6. Przejdź w **Home Assistant** do zakładki **MQTT**, w której powinna pojawić się dodatkowa encja z&nbsp;nowego czujnika:

    <img width="250" alt="obraz" src="https://github.com/user-attachments/assets/5632f11f-efb0-4b3b-a156-a3ca944fd933" />