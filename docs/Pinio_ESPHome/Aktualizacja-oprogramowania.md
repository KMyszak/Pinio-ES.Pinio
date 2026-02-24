# Aktualizacja ESPHome

Aktualizację oprogramowania można wykonać na dwa sposoby:

- z poziomu powiadomienia dostępnego `Ustawieniach`
- z poziomu panelu `ESPHome Builder`


=== "Ustawienia"

    1. Z paska bocznego wybierz `Ustawienia` - jeśli dostępna jest aktualizacja, pojawi się powiadomienie:  
    
        <img width="450" alt="obraz" src="https://github.com/user-attachments/assets/11ea11f4-72af-424e-a9c9-a0f78905c677" />
    
    2. Kliknij powiadomienie - zobaczysz okno z informacją o dostępnej wersji:    
        
        <img width="450" alt="obraz" src="https://github.com/user-attachments/assets/77249dc9-d906-41e5-9cd8-b8c787eeee77" />

    3. Kliknij **Aktualizuj**.

        !!! info "Aktualizacja może potrwać kilka minut "

        !!! warning "Problemy z aktualizacją"
        
            Jeżeli aktualizacja nie powiedzie się lub zostanie przerwana - przeprowadź ją przez panel **ESPHome Builder**.

=== "ESPHome Builder"

    1. Wybierz z paska bocznego **ESPHome Builder**: 

        <img width="230" alt="obraz" src="https://github.com/user-attachments/assets/fead98e2-a8eb-4f5e-adb7-caf5b4bb9e2d" />

        ??? failure "Brak skrótu na pasku bocznym?"

            Jeśli nie widzisz skrótu na pasku bocznym:
            
            - przejdź do **konfiguracji**, albo
            - włącz go z poziomu **interejsu użytkownika**

            === "Konfiguracja"
                
                1\. Z lewego paska bocznego wybierz:   
                    `Ustawienia → Aplikacje → ESPHome Builder`

                <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

                2\. Zaznacz opcję **Pokaż na pasku bocznym**:

                <img width="400" alt="obraz" src="https://github.com/user-attachments/assets/c85b76f1-343c-4a04-9d09-4ff0459b5d02" />

            === "Ustawienia aplikacji"

                1\. Z lewego paska bocznego wybierz:   
                    `Ustawienia → Aplikacje → Zainstaluj aplikację`

                2\. Wyszukaj dodatek **ESPHome** i wybierz `ESPHome Device Builder`:   

                <img width="697" height="114" alt="obraz" src="https://github.com/user-attachments/assets/f003fb0b-7fcf-4e66-8383-54edee34ec2d" />  

                3\. Kliknij **Otwórz interfejs użytkownika**

    2. Wybierz urządzenie, które chcesz zaktualizować i kliknij `UPDATE`.   
        Aby zaktualizować **wszystkie urządzenia**, kliknij `UPDATE ALL` (*prawym górny róg*):

        <img width="402" height="129" alt="obraz" src="https://github.com/user-attachments/assets/abc035e8-5510-442a-9e42-14b155e83ff4" />    

    === "UPDATE"

        Po wybraniu jednej pozycji zostanie wyświetlone menu wyboru sposobu instalacji - tak jak przy pierwszym programowaniu:

        - aktualizacja bezprzewodowa → [**Wirelessly**](Aktualizacja-bezprzewodowa.md)
        - aktualizacja manualna → [**Manual download**](Wgrywanie-.uf2.md)
        
        <img width="420" alt="obraz" src="https://github.com/user-attachments/assets/70cd2f33-648b-4888-a6b1-6eed000a9bdb" />

    === "UPDATE ALL"

        1. Wybierz `UPDATE ALL`, aby zaktualizować **wszystkie** skonfigurowane urządzenia:  

            <img width="514" height="57" alt="obraz" src="https://github.com/user-attachments/assets/0a353b95-108d-4391-8686-6f530056df07" />

        2. Pojawi się okno potwierdzenia, kliknij **UPDATE ALL**:

            <img width="230" src="https://github.com/user-attachments/assets/ece46699-b94f-4179-a504-409ccac9d4bb" />
        
        3. Zostanie otworzone okno z logami:   

            <img width="600" alt="obraz" src="https://github.com/user-attachments/assets/5fa1f087-17e7-4ebb-af8a-aa88836c4453" />

        4. Aktualizacja zwykle trwa kilka minut:

            !!! success "Po zakończeniu każdego urządzenia powinien pojawić się status *SUCCESS*"

            <img width="600" alt="obraz" src="https://github.com/user-attachments/assets/88931646-47c5-46ed-b9ef-71df2756a539" />
        
        5. Wszystkie urządzenia są zaktualizowane i gotowe do pracy  

    
