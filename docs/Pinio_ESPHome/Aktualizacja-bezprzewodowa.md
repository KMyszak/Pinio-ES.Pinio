# Aktualizacja bezprzewodowa

Aktualizacja bezprzewodowa w **ESPHome** odbywa się bezpośrednio z poziomu aplikacji - po zapisaniu zmian w pliku `.YAML` system kompiluje nowy firmware i wysyła go do urządzenia przez Wi-Fi. Cały proces jest automatyczny i nie wymaga ponownego podłączania urządzenia kablem USB.

Upewnij się, że urządzenie jest podłączone do sieci oraz kod `.YAML` jest poprawny - możesz go sprawdzić korzystając z opcji `Validate`:  

<img width="566" height="201" alt="obraz" src="https://github.com/user-attachments/assets/826694a8-e0fc-4245-b235-1c5c5335f479" />

---

## Przeprowadzanie aktualizacji

1. Wybierz na pasku bocznym **ESPHome Builder** (opcja [**Pokaż na pasku bocznym**](Instalacja-dodatku-ESPHome.md)):   

    <img width="230" alt="obraz" src="https://github.com/user-attachments/assets/fead98e2-a8eb-4f5e-adb7-caf5b4bb9e2d" />

2. Rozwiń menu klikając **`⋮`**, następnie kliknij `Install`:  

    <img width="566" height="201" alt="obraz" src="https://github.com/user-attachments/assets/cf30d570-b048-40ab-b9be-123ae6813820" />

3. Wybierz **Wirelessly**:  

    <img width="400" height="265" alt="obraz" src="https://github.com/user-attachments/assets/3bcaf906-cb5d-4bda-9110-14491758e7a8" />

    Cały proces trwa około 5 minut: 

    <img width="567" height="113" alt="obraz" src="https://github.com/user-attachments/assets/43e42ce9-b589-43fc-aa08-0261c797c8dd" />

4. Po zakończonej **instalacji OTA** pojawi się komunikat: 

    <img width="567" height="56" alt="obraz" src="https://github.com/user-attachments/assets/2e1c3e6c-160f-4210-9fa2-b17ac451cd9d" />

5. Po restarcie oraz ponownym załadowaniu konfiguracji urządzenie jest **gotowe do pracy**

