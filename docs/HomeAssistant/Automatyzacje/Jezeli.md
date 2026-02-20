# Jeżeli

W tym miejscu definiowane są dodatkowe `warunki`, które **muszą** być spełnione, aby `wyzwalacze` z sekcji **Kiedy** uruchomiły akcje w części **Wykonaj**.   

Działanie warunków przypomina logikę **bramki AND** - wszystkie warunki muszą być prawdziwe, aby automatyzacja mogła się wykonać.

!!! quote ""

    KIEDY & JEŻELI ⇒ WYKONAJ  

!!! tip ""

    [Dowiedz się więcej na temat warunków :material-open-in-new: ](https://www.home-assistant.io/docs/automation/condition/)      
              
Warunki dodaje się klikając **+ Dodaj warunek**, wybierając typ `Urządzenie` lub `Encja`:

<img width="890" alt="obraz" src="https://github.com/user-attachments/assets/09103462-d023-4660-8f99-34ff5ab83122" />

## Przykład

Przykład przedstawia dwa warianty tego samego warunku zapisane w różny sposób - oba działają **identycznie**:

<img width="728 alt="obraz" src="https://github.com/user-attachments/assets/55cef7b0-3e29-421a-aa0b-e1cdf31290bb" />

## Czas trwania

Można określić, jak długo warunek musi pozostawać spełniony, korzystając z pola **Przez** (**For** / **Czas trwania**). Warunek uznawany jest za prawdziwy dopiero po upływie wskazanego czasu.