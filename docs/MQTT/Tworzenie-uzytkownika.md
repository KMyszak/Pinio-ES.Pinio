# Tworzenie użytkownika

Po zainstalowaniu dodatku należy utworzyć **nowego użytkownika**, który będzie używany do autoryzacji połączeń **MQTT**. W tym celu w ustawieniach dodatku definiuje się nazwę użytkownika oraz hasło, które następnie wykorzystuje się w aplikacjach lub urządzeniach łączących się z brokerem. 

Dzięki temu dostęp do brokera jest **kontrolowany** i **bezpieczny**.

---

1. Przejdź na stronę swojego **Home Assistant** (np. *haos.app*)
2. Z menu po lewej stronie wybierz:  
     `Ustawienia → Aplikacje → Mosquitto broker`
     <img width="750" alt="obraz" src="https://github.com/user-attachments/assets/fdec6d58-f374-4139-a7b4-40b34c8e27bb" />

3. Przejdź do zakładki `Konfiguracja`, w sekcji `Logins` kliknij przycisk **Utwórz**:  

    <img width="750" alt="obraz" src="https://github.com/user-attachments/assets/399f5577-199e-4fb9-a4e4-7ffad22f1ceb" />

4. Wprowadź dane użytkownika i kliknij **Utwórz**:   

    <img width="323" alt="obraz" src="https://github.com/user-attachments/assets/a6082559-72be-470e-a8be-3dfbe14577f5" />

5. Kliknij **Zapisz** - dodatek poprosi o ponowne uruchomienie, zatwierdź klikając **Uruchom ponownie**:   

    <img width="745" alt="obraz" src="https://github.com/user-attachments/assets/1aa3081a-3e64-4332-96db-9812d3948c69" />

    !!! tip ""

        W razie problemów uruchom ponownie cały Home Assistant.  

6. Przejdź do [**Integracja**](Integracja.md)

---

## Tworzenie kolejnego użytkownika

Dodatkowego użytkownika wprowadzamy w identyczny sposób: 

<img width="745" height="185" alt="obraz" src="https://github.com/user-attachments/assets/5ec89328-edef-4505-b9ab-6fc3829ba658" />

!!! question ""

    Pamiętaj o **zapisaniu** zmian.

---

## Tryb YAML

Pliki konfiguracyjne **ESPHome** używają **YAML**, czyli przyjaznego dla człowieka standardu serializacji danych.

**YAML** został zaprojektowany tak, aby był czytelny i łatwy do edycji, ale czasami może sprawiać problemy, zwłaszcza jeśli chodzi o wcięcia - jest nadzbiorem **JSON**, więc składnia **JSON** może być również używana w plikach **YAML**.

Więcej o **YAML** dowiesz sie ze strony [**https://esphome.io/guides/yaml/ :material-open-in-new:**](https://esphome.io/guides/yaml/)

!!! tip ""

    Aby skorzystać z **trybu YAML**, należy rozwinąc menu klikając **`⋮`** w prawym górnym rogu:

    <img width="745" alt="obraz" src="https://github.com/user-attachments/assets/f2370eb1-6170-4288-a510-4053a9cf902a" />