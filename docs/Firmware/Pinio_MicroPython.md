# Instalacja MicroPythona

Instalacja MicroPythona pozwala przekształcić płytkę **Pinio** w pełni programowalne urządzenie **IoT**. Dzięki temu można uruchamiać własne skrypty w języku Python i integrować urządzenia z różnymi systemami automatyki.

## Wymagane narzędzia

Do instalacji potrzebne są podstawowe narzędzia, które pozwolą na połączenie i wgranie firmware’u na płytkę - ważne jest, aby przewód USB był sprawny, a komputer miał zainstalowane sterowniki dla danego modułu:

- **przewód microUSB** - zapewnia połączenie płytki z komputerem
- **pobrany firmware MicroPython** - plik `.bin` ze strony producenta, zgodny z modułem Raspberry Pi Pico 2 W

## Instalacja

Proces instalacji dzieli się na kilka prostych kroków, które należy wykonać w odpowiedniej kolejności.

### Pobranie firmware

Firmware MicroPython można pobrać ze strony oficjalnej lub z repozytorium producenta modułu.
Warto upewnić się, że wersja firmware jest zgodna z Twoim modułem i wspiera wszystkie potrzebne funkcje.

1. Przejdź na stronę:  

    [https://micropython.org/download/RPI_PICO2_W/ :material-open-in-new:](https://micropython.org/download/RPI_PICO2_W/)

2. Pobierz najnowszy plik `.uf2` z sekcji **Releases**:  

    <img width="334" height="99" alt="obraz" src="https://github.com/user-attachments/assets/27953d6c-61e8-4479-83e8-8d77a1ccd30f" />

### Wgranie firmware

Wgranie firmware polega na przesłaniu pobranego pliku na pamięć urządzenia **Raspberry Pi Pico 2 W**. Po poprawnym wgraniu, **MicroPython** jest gotowy do pracy, a płytka pojawia się jako nowy interfejs dla IDE.

1. Wciśnij i przytrzymaj przycisk **BOOTSEL** na **Raspberry Pi Pico 2 W** (*tryb bootloadera*):  

    <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/8d6245bb-65b1-460b-a608-1ac14e944baf" />

2. Wciąż trzymając przycisk podłącz urządzenie do komputera przez USB
3. Pojawi się nowy dysk `RP2350`:  

    <img width="300" alt="obraz" src="https://github.com/user-attachments/assets/a23618db-b7ba-44a4-b909-d60ae6ff265a" />

4. Przenieś pobrany plik `.uf2` na dysk **RP2350**
5. **Raspberry Pi Pico 2 W** zrestartuje się automatycznie - po chwili zniknie jako dysk USB
6. Przejdź do dalszej [**konfiguracji**](../../Pinio_MicroPython/Polaczenie-z-PC)