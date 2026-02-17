# Encje

**Encje** to pojedyncze obiekty reprezentujące urządzenia lub ich funkcje, takie jak czujnik temperatury, przekaźnik czy dioda LED. Każda encja ma swój unikalny identyfikator, stan i właściwości, które mogą być odczytywane lub zmieniane przez system automatyki. 

Dzięki **encjom** można łatwo integrować i kontrolować różne elementy sprzętowe w jednym środowisku.

Dla urządzeń **Pinio** (MicroPython + MQTT) dostępne jest 5 [**encji :material-open-in-new:**](https://www.home-assistant.io/docs/configuration/entities_domains/) (*entities*):

!!! note "Sterowanie"
    **RELAY 1** - Wyjście 1 (GPIO20)  
    **RELAY 2** - Wyjście 2 (GPIO21)

!!! note "Sensory" 
    **IN 1** - Wejście cyfrowe 1 (GPIO18)   
    **IN 2** - Wejście cyfrowe 2 (GPIO19)  
    **1-Wire** - Wejście 1-Wire (bez podłączonego czujnika) 

---

## 1 urządzenie

<img width="200" align="right" alt="obraz" src="https://github.com/user-attachments/assets/50fe0354-e281-44e0-bd41-beda77be7bfe" />

Klikając `1 urządzenie` otworzy się panel MQTT, w którym dostępne są wszystkie encje wraz z możliwością ich edycji oraz szybkiego dodania do dashboardu:

<img width="521" alt="obraz" src="https://github.com/user-attachments/assets/9482097c-1b39-4da0-964b-5f381ee8549f" />

!!! tip ""

    Można w tym miejscu utworzyć automatyzacje, sceny, skrypty lub przejrzeć dziennik danych z urządzenia.

---

## 5 encji

<img width="200" align="right" alt="obraz" src="https://github.com/user-attachments/assets/40ff36ab-02ee-40bb-b005-fb30f37c15ea" />

Klikając `5 encji` otworzy się **Rejestr encji** powiązanych z urządzeniem. Rejestr pokazuje wszystkie powiązane encje, umożliwiając szybki podgląd i zarządzanie funkcjami urządzenia:

<img width="521" alt="obraz" src="https://github.com/user-attachments/assets/e258815b-573b-47a1-bd60-9e3ed5e730d8" />

!!! tip ""

    Można w tym miejscu przejść do ustawień encji klikając na nią, następnie ikonę zębatki.
