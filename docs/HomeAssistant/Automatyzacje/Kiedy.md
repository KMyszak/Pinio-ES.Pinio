# Kiedy

W tym miejscu deklarowane są `wyzwalacze` - elementy, które uruchamiają automatyzację. Jeżeli którykolwiek wyzwalacz zostanie spełniony, automatyzacja przejdzie do sekcji **Wykonaj**, o ile w części **Jeżeli** nie ma dodatkowych warunków blokujących wykonanie.

Jeśli dodasz wiele wyzwalaczy, automatyzacja uruchomi się, gdy **którykolwiek z nich** zostanie spełniony - działanie analogiczne do bramki **OR**.

!!! tip ""

    [Dowiedz się więcej na temat wyzwalaczy :material-open-in-new:](https://www.home-assistant.io/docs/automation/trigger/) 

## Przykład

Zmiana stanu **Wejście 1** *LUB* **Wejście 2** utrzymująca się przez **3 sekundy** spowoduje spełnienie wyzwalacza i przejście do sekcji `Wykonaj`:

<img width="800" alt="obraz" src="https://github.com/user-attachments/assets/30c41b58-f541-4963-9d15-2a6ebda06616" />
    
!!! warning "Poprawny wybór wyzwalacza"
    Należy zwrócić uwagę na właściwą formę wyzwalacza - prawidłowy dobór **warunku**.  
    W przykładzie użyto opcji `zmieni się stan lub atrybut`, co oznacza, że automatyzacja może uruchomić się również wtedy, gdy encja po starcie systemu zmieni stan z **niedostępna** na **on**/**off**.

## Sprawdzenie działania warunku

Po aktywacji `warunku`, w górnej części okna szczegółów automatyzacji pojawi się belka **WYZWOLONY**, dzięki czemu łatwo potwierdzić, że akcja została uruchomiona:

<img width="800" alt="obraz" src="https://github.com/user-attachments/assets/11ac8a73-4546-49d5-ba95-ebd31487ecb0" />

