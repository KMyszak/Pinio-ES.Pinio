1. Przejdź na stronę główną urządzenia - wpisz jego **adres IP** w przeglądarce lub kliknij `Main Menu`
2. Wybierz opcję `Console`:   

    <img width="315" height="470" alt="obraz" src="https://github.com/user-attachments/assets/5473ac95-cf40-4051-81b0-8eb70c74fe02" />

3. W konsoli wpisz kolejno poniższe komendy (każdą zatwierdź klawiszem **Enter**):

    | Polecenie        | Opis                                                                                                                           |
    |------------------|--------------------------------------------------------------------------------------------------------------------------------|
    | <pre><code>SetOption114 1   </code></pre> | Auto-konfiguracja przycisków w trybie przełącznika                                                    |
    | <pre><code>SwitchMode1 16   </code></pre> | Wysyłanie stanu wejścia 1 do MQTT                                                                     |
    | <pre><code>SwitchMode2 16   </code></pre> | Wysyłanie stanu wejścia 2 do MQTT                                                                     |
    | <pre><code>LedState 4   </code></pre>     | Ustawienie trybu diody LED (STA) - więcej o [trybach :material-open-in-new:](ES.Pinio-‐-Tryby-Pracy)  |
    | <pre><code>Restart 1   </code></pre>      | Reset z zachowaniem ustawień                                                                          |

    !!! Success "Wprowadzone dane w konsoli"

        <img width="700" height="157" alt="obraz" src="https://github.com/user-attachments/assets/e150bdac-4ee3-4bd2-a9b8-45a1d671af46" />

4. Przejdź do ustawień [**MQTT :material-open-in-new:**](Edycja-MQTT.md)
