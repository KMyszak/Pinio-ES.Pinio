# Edycja MQTT

Kolejnym krokiem jest konfiguracja połączenia z brokerem **MQTT**. Użytkownik musi wprowadzić wszystkie niezbędne dane, aby urządzenie mogło prawidłowo wysyłać i odbierać komunikaty: 

- **adres IP** i **port** brokera
- **nazwę** użytkownika oraz **hasło** 

---

1. Przejdź do `Configuration → MQTT`:  
    <img width="648" height="478" alt="obraz" src="https://github.com/user-attachments/assets/b154d347-8953-4638-b1db-d42d79757206" />

2. Zmień parametry według własnych ustawień brokera:

    | Parametr      | Opis                                                                                                                                             |
    |---------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Host**      | IP twojego brokera MQTT                                                                                                                          |
    | **Port**      | Port brokera MQTT (domyślnie ustawiony na 1883)                                                                                                  |
    | **Client**    | Unikalny identyfikator urządzenia - w 99% przypadków można zostawić domyślną wartość                                                             |
    | **User**      | Nazwa użytkownika do uwierzytelnienia w brokerze MQTT                                                                                            |
    | **Password**  | Hasło do uwierzytelnienia w brokerze MQTT                                                                                                        |
    | **Topic**     | Unikalny temat identyfikujący twoje urządzenie (np. `hallswitch`, `kitchen-light`) - zaleca się użycie jednego słowa                             |
    | **FullTopic** | Pełna definicja tematu - zmień ją, jeśli chcesz korzystać z wielopoziomowych tematów dla swoich urządzeń, np. `lights/%prefix%/%topic%/`. Więcej informacji dla [**FullTopic :material-open-in-new:**](https://tasmota.github.io/docs/MQTT/#mqtt-topic-definition)                                                  |

    #### Przykładowe ustawienia

    <img width="320" height="596" alt="obraz" src="https://github.com/user-attachments/assets/37bb805e-13ce-48c7-8206-493b391af172" />

3. Kliknij **Save**
4. Zaloguj się do **Home Assistant** (`https://twoja_domena.haos.app`)
5. Przejdź do `Ustawienia → Urządzenia oraz usługi` - urządzenie powinno zostać wykryte:  
    <img width="320" alt="obraz" src="https://github.com/user-attachments/assets/d71c4048-de15-4bd0-9bba-5509704003ac" />

6. Kliknij **UTWÓRZ**, następnie **ZATWIERDŹ** 
7. Po odświeżeniu strony, jeżeli wszystko zostało poprawnie ustawione, **Home Assistant** automatycznie wykryje **15 dostępnych encji**, które możesz wykorzystać w dalszej integracji:      
    <img width="750" alt="obraz" src="https://github.com/user-attachments/assets/27e5273d-8288-4129-8555-369648d65f29" />

    !!! info ""
        
        W tym miejscu można zmienić **nazwę urządzenia**, **etykietę** oraz **przypisać do obszaru** klikając ikonę ołówka:  
            
        <img width="406" height="293" alt="d4ffaaa2-284d-4d37-9539-a3ef6e255ee5" src="https://github.com/user-attachments/assets/fa7f868b-f303-4a18-9dd3-52ed9c879dc9" />
