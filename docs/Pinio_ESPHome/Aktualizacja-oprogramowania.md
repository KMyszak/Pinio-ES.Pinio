# Aktualizacja ESPHome

Aktualizację oprogramowania można wykonać na dwa sposoby:

- wykorzystując dostępne powiadomienie w `Ustawieniach`
- przez panel `ESPHome Builder`


=== "Ustawienia"

    1. Wybierz na pasku bocznym `Ustawienia` - powinno być widoczne powiadomienie:  
    
        <img width="450" alt="obraz" src="https://github.com/user-attachments/assets/11ea11f4-72af-424e-a9c9-a0f78905c677" />
    
    2. Po kliknięciu pojawi się okno z informacjami odnośnie wersji:  
        
        <img width="450" alt="obraz" src="https://github.com/user-attachments/assets/77249dc9-d906-41e5-9cd8-b8c787eeee77" />

    3. Kliknij **Aktualizuj** - aktualizacja trwa do kilku minut  

        !!! warning "Jeżeli aktualizacja się nie wykona lub napotka na jakiś problem warto ją przeprowadzić przez panel *ESPHome Builder*"

=== "ESPHome Builder"

    1. Wybierz na pasku bocznym **ESPHome Builder**: 

        <img width="230" alt="obraz" src="https://github.com/user-attachments/assets/fead98e2-a8eb-4f5e-adb7-caf5b4bb9e2d" />

        ??? failure "Brak skrótu"

            Jeśli nie widzisz skrótu na pasku bocznym:
            
            - przejdź do **konfiguracji** lub
            - przejdź do **interejsu użytkownika**

            === "Konfiguracja"
                
                1.Z menu po lewej stronie wybierz `Ustawienia → Aplikacje → ESPHome Builder`:

                <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

                2.Zaznacz **Pokaż na pasku bocznym**:

                <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/c85b76f1-343c-4a04-9d09-4ff0459b5d02" />

            === "Ustawienia aplikacji"

                1.Z menu po lewej stronie wybierz:  
                    `Ustawienia → Dodatki → Sklep z dodatkami (ikona koszyka w prawym dolnym rogu)`

                2.Wyszukaj dodatek **ESPHome** i wybierz `ESPHome Device Builder`:   

                <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

                3.Kliknij **Otwórz interfejs użytkownika**

    2. Wybierz urządzenie, które chcesz zaktualizować i kliknij `UPDATE`. Jeżeli chcesz zaktualizować **wszystkie** urządzenia kliknij `UPDATE ALL` (prawy górny róg):

        <img width="402" height="129" alt="obraz" src="https://github.com/user-attachments/assets/abc035e8-5510-442a-9e42-14b155e83ff4" />    

    === "UPDATE"

        W przypadku wyboru jednego urządzenia pojawi się okno z wyborem formy instalacji oprogramowania, tak jak miało to miejsce przy jego pierwszej edycji - należy postępować analogicznie:

        - aktualizacja bezprzewodowa → [Wirelessly :material-open-in-new:](Aktualizacja-bezprzewodowa.md)
        - aktualizacja manualna → [Manual download :material-open-in-new:](Wgrywanie-.uf2.md)
        
        <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/70cd2f33-648b-4888-a6b1-6eed000a9bdb" />

    === "UPDATE ALL"

        Celem aktualzacji wszystkich urządzeń, najwygodniej będzie skorzystać z opcji `UPDATE ALL` w panelu **ESPHome Builder**:

        <img width="514" height="57" alt="obraz" src="https://github.com/user-attachments/assets/0a353b95-108d-4391-8686-6f530056df07" />

        ---

        1. Wybór `UPDATE ALL` spowoduje pojawienie się komunikatu, który należy potwierdzić: 

            <img width="230" src="https://github.com/user-attachments/assets/ece46699-b94f-4179-a504-409ccac9d4bb" />
        
        2. Zostanie otworzone okno z logami:

            <img width="600" alt="obraz" src="https://github.com/user-attachments/assets/5fa1f087-17e7-4ebb-af8a-aa88836c4453" />

        3. Cała aktualizacja trwa do kilku minut, a udany proces powinien zostać zakończony `SUCCESS`:

            <img width="600" alt="obraz" src="https://github.com/user-attachments/assets/88931646-47c5-46ed-b9ef-71df2756a539" />
        
        4. Urządzenia są zaktualizowane i gotowe do pracy

    
