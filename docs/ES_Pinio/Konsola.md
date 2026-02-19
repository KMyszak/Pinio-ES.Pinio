# Konsola

Po zakończeniu konfiguracji modułu i przypisaniu funkcji **GPIO** należy wprowadzić w konsoli Tasmoty kilka poleceń niezbędnych do poprawnego działania urządzenia. Komendy aktywują obsługę wejść, integrację z **MQTT** oraz konfigurują zachowanie diody statusowej (STA). 

Po wykonaniu poleceń urządzenie automatycznie się zrestartuje i zacznie działać zgodnie z wprowadzoną konfiguracją.

---

1. Połącz się z urządzeniem, wpisując jego **adres IP** w przeglądarce (w razie trudności zajrzyj do [**FAQ**](../FAQ/ES.Pinio.md#sprawdzenie-przypisanego-ip-do-urzadzenia))
2. Wybierz opcję `Console`:   
    <img width="315" height="470" alt="obraz" src="https://github.com/user-attachments/assets/5473ac95-cf40-4051-81b0-8eb70c74fe02" />

3. W konsoli wpisz kolejno poniższe komendy, zatwierdzjąc każdą klawiszem **Enter**:

    | Polecenie        | Opis                                                                                                                                              |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | <pre><code>SetOption114 1   </code></pre> | Auto-konfiguracja przycisków w trybie przełącznika                                                                       |
    | <pre><code>SwitchMode1 16   </code></pre> | Wysyłanie stanu wejścia 1 do MQTT                                                                                        |
    | <pre><code>SwitchMode2 16   </code></pre> | Wysyłanie stanu wejścia 2 do MQTT                                                                                        |
    | <pre><code>LedState 4   </code></pre>     | Konfiguracja diody statusowej (STA) - więcej o [**trybach**](Status-urzadzenia.md#tryby-diody-sta)                       |
    | <pre><code>Restart 1   </code></pre>      | Urządzenie uruchomi się ponownie, zachowując wszystkie ustawienia                                                        |
              
    !!! Success "Wprowadzone komendy w konsoli"

        <img width="700" height="157" alt="obraz" src="https://github.com/user-attachments/assets/e150bdac-4ee3-4bd2-a9b8-45a1d671af46" />

4. Przejdź do ustawień [**MQTT**](Edycja-MQTT.md)
