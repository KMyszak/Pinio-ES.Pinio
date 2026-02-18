# Kiedy

W tym miejscu deklarowane są `wyzwalacze` - elementy, które uruchamiają automatyzację - jeżeli zostanie spełniony wyzwalacz, wykona się przypisana mu **akcja** (**Wykonaj**) automatyzacji (jeśli nie ma dodatkowych **warunków** w **Jeżeli**).  

Można przypisać kilka warunków i akcja zostanie wykonana, jeżeli **jeden** z warunków zostanie spełniony - działanie zbliżone do bramki OR.  

!!! tip ""

    [Dowiedz się więcej na temat wyzwalaczy :material-open-in-new:](https://www.home-assistant.io/docs/automation/trigger/) 

## Przykład

Zmiana stanu **Wejście 1** *LUB* **Wejście 2** przez **3 sekundy** spowoduje aktywację warunku i przejście do `Wykonaj`:

<img width="800" alt="obraz" src="https://github.com/user-attachments/assets/30c41b58-f541-4963-9d15-2a6ebda06616" />
    
!!! warning "Wybór warunku"
    Należy pamiętać o poprawnym doborze **warunku** (formie jego wyzwolenia), ponieważ w przykładzie jest *zmieni się stan lub atrybut*, przez co automatyzacja może zostać wywołana przez samo podłączenie urządzenia do zasilania, gdyż encja *zmieni stan* z **niedostępnej** na **on/off**.

## Sprawdzenie działania warunku

Można w prosty sposób sprawdzić czy `warunek` został spełniony, ponieważ po aktywacji powinna pojawić się belka `WYZWOLONY`: 

<img width="800" alt="obraz" src="https://github.com/user-attachments/assets/11ac8a73-4546-49d5-ba95-ebd31487ecb0" />

