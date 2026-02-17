# Dodanie urządzenia

Po poprawnej konfiguracji w aplikacji **MQTT**, urządzenie powinno zostać automatycznie wykryte i pojawić się w panelu aplikacji. Jeśli automatyczne wykrycie nie powiedzie się, konieczne jest ręczne dodanie urządzenia, wybierając odpowiedni szablon. 

Dzięki temu urządzenie może w pełni komunikować się z brokerem i przesyłać dane w czasie rzeczywistym.

---

1. Przejdź na stronę swojego **Home Assistant** (np. *haos.app*)
2. Z menu po lewej stronie wybierz:   
`Ustawienia → Urządzenia oraz usługi`   
3. Pojawi się okienko (jeśli go nie widzisz przejdź do [Brak wykrytego urządzenia](#brak-wykrytego-urzadzenia)):   

    <img width="290" height="220" alt="obraz" src="https://github.com/user-attachments/assets/a96888fb-e4f7-43eb-95d4-74bb958f03a7" />    
    
4. Kliknij **UTWÓRZ**, **ZATWIERDŹ**  
5. Przejdź do [**Integracja**](Integracja.md)     

---

## Brak wykrytego urządzenia

1. Z menu po lewej stronie wybierz:   
`Ustawienia → Urządzenia oraz usługi`
2. W prawym dolnym rogu kliknij **`+ DODAJ INTEGRACJĘ`**
3. Wpisz `MQTT` i wybierz:

    <img width="430" height="181" alt="obraz" src="https://github.com/user-attachments/assets/77fac4c9-ec23-4957-9105-c41e7933e0fb" />

4. Z listy wybierz `MQTT`:

    <img width="429" height="431" alt="obraz" src="https://github.com/user-attachments/assets/82809594-6990-4664-a65e-2abc92b341e0" />

5. Wybierz `Use the offcial Mosquitto MQTT Broker add-on`:

    <img width="378" height="197" alt="obraz" src="https://github.com/user-attachments/assets/a2f0225d-496e-4c24-8a47-8d60d8418016" />

6. Przejdź do [**Integracja**](Integracja.md)

