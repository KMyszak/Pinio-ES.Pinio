1. Podłącz urządzenie przez przewód microUSB do komputera:
> <img width="364" height="544" alt="obraz" src="https://github.com/user-attachments/assets/1b4cd00a-52ad-4cc7-978a-2b7ebcb58ed9" />

2. Otwórz program `Tasmotizer` [(**tasmotizer-1.2.exe**)](https://github.com/chomtech/pinio-docs/wiki/ES.Pinio-wymagane-oprogramowanie#tasmotizer):
3. Wybierz odpowiedni port z listy `Select port` (sprawdzenie portu → [COM](ES.Pinio-wymagane-oprogramowanie#sprawdzenie-portu-com)):
> <img width="492" height="460" alt="obraz" src="https://github.com/user-attachments/assets/f53fed15-72a2-47b2-8e58-4e823aa7eef8" />
4. W sekcji `Select image` wybierz pobrany plik [**tasmota.bin**](ES.Pinio-wymagane-oprogramowanie#tasmota):
> <img width="492" height="460" alt="obraz" src="https://github.com/user-attachments/assets/f21bdaf8-90fa-49db-9e8c-f1a5c4812a5f" />
5. Kliknij `Tasmotize!` - rozpocznie się proces flashowania:
> <img width="402" height="170" alt="obraz" src="https://github.com/user-attachments/assets/443b04ff-7143-4574-a173-b3d4f62651fd" />
>
> Dioda **STA** powinna zacząć świecić oraz mrugać dioda na układzie ESP-12F
6. Po zakończeniu pojawi się informacja:
> <img width="301" height="108" alt="obraz" src="https://github.com/user-attachments/assets/ade67d2f-71ac-49eb-99b8-a2ceab9bb66e" />
7. Urządzenie zostanie zresetowane i uruchomi swój AP, z którym możesz się połączyć celem zmiany ustawień Wi-Fi → [łączenie z AP](Pierwsze-uruchomienie-ES.Pinio)

ℹ️ Ustawienia Wi-Fi (oraz MQTT) można zmienić przez program, wybierając przycisk `Send config`, następnie zaznaczając okienko WiFi, wpisując poprawne dane i klikając przycisk `Save`:
>
> <img width="642" height="375" alt="obraz" src="https://github.com/user-attachments/assets/ed3ca8c1-de72-4da6-88ba-a5617c573807" />
Urządzenie się zrestartuje, a po kilku sekundach można odczytać jego IP klikając przycisk `Get IP`:
> <img width="300" height="123" alt="obraz" src="https://github.com/user-attachments/assets/c213f1df-0984-4e74-b100-22ec17327274" />
>
ℹ️ Dalszą edycję należy przeprowadzić przez przeglądarkę, korzystając z uzyskanego adresu IP → [Konfiguracja](Podstawowe-ustawienia-i-GPIO)
