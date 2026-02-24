# Encje

**Encje** to pojedyncze obiekty reprezentujące urządzenia lub ich funkcje, takie jak czujnik temperatury, przekaźnik czy wejście. Każda encja ma swój unikalny identyfikator, stan i właściwości, które mogą być odczytywane lub zmieniane przez system automatyki. 

Dzięki **encjom** można łatwo integrować i kontrolować różne elementy sprzętowe w jednym środowisku.

Dla urządzeń **Pinio** (MicroPython + MQTT) dostępne jest 5 [**encji :material-open-in-new:**](https://www.home-assistant.io/docs/configuration/entities_domains/) (*entities*):

- Sterowanie:
    - **RELAY 1** - Wyjście 1 (`GPIO20`)  
    - **RELAY 2** - Wyjście 2 (`GPIO21`)

- Sensory:
    - **1-Wire** - Wejście 1-Wire (bez podłączonego czujnika) 
    - **IN 1** - Wejście cyfrowe 1 (`GPIO18`)   
    - **IN 2** - Wejście cyfrowe 2 (`GPIO19`) 

---

## Urządzenie

<img width="200" align="right" alt="obraz" src="https://github.com/user-attachments/assets/50fe0354-e281-44e0-bd41-beda77be7bfe" />

Klikając `urządzenie` otworzy się panel **MQTT**, z listą wszystkich urządzeń połączonych z aplikacją.   
Kliknięcie wybranego urządzenia, otworzy kolejny panel, w którym dostępne są **wszystkie encje** wraz z możliwością ich edycji oraz szybkiego dodania do panelu:

<img width="530" alt="obraz" src="https://github.com/user-attachments/assets/9482097c-1b39-4da0-964b-5f381ee8549f" />

!!! tip ""

    Można w tym miejscu utworzyć automatyzacje, sceny, skrypty lub przejrzeć dziennik danych z urządzenia.

---

## Encje

<img width="200" align="right" alt="obraz" src="https://github.com/user-attachments/assets/40ff36ab-02ee-40bb-b005-fb30f37c15ea" />

Klikając `encje` otworzy się **Rejestr encji** powiązanych z aplikacją **MQTT**.    
Rejestr pokazuje wszystkie encje podłączonych wszystkich urządzeń, umożliwiając szybki podgląd i zarządzanie funkcjami **każdego** z nich:

<img width="521" alt="obraz" src="https://github.com/user-attachments/assets/e258815b-573b-47a1-bd60-9e3ed5e730d8" />

!!! tip ""

    Można w tym miejscu przejść do ustawień encji klikając na nią, następnie wybierając ikonę zębatki.
