# Kilka czujników 1-Wire

Podłączone **nowe** czujniki zostaną dopiero wykryte przy kolejnym utworzeniu integracji przez moduł `mqtt_creator.py`.

---

1. Podłącz urządzenie do komputera przez USB
2. Wczytaj jego pliki w programie, np. przez program [**Thonny :material-open-in-new:**](https://thonny.org/)
3. Usuń plik `mac.conf`
4. Uruchom urządzenie przez kliknięcie `F5` w **Thonny** lub fizyczny przycisk **RST**
5. W programie powinien pojawić się komunikat:

    <img width="409" height="84" alt="obraz" src="https://github.com/user-attachments/assets/eb2773a5-7d06-49e5-9aab-111007ecf407" />

6. Przejdź do zakładki MQTT, w której powinna pojawić się dodatkowa encja:

    <img width="250" alt="obraz" src="https://github.com/user-attachments/assets/5632f11f-efb0-4b3b-a156-a3ca944fd933" />