# Programowanie Obiektowe
## Wstęp
### Zasady Zaliczania
- jedna nieobecność dozwolona
- oceniane postępy na każdym laboratorium, na podstawie repozytorium
- Terminy konsultacji podane na stronie Wydziału
### Literatura
- *Django 3. Praktyczne tworzenie aplikacji sieciowych. Wydanie III* Autor: Antonio Melé
- *Python. Instrukcje dla programisty. Wydanie II* Autor: Eric Matthes

## Program Laboratoriów
### Laboratorium 1
**Wstęp do pythona**
1. Instalacja Python 3.10 - [https://www.python.org/downloads/](https://www.python.org/downloads/)
2.  W celu wprowadzenia do korzystania z Pythona:
Do przerobienia tematy:
    - [od Python Introduction do Python Datatypes](
https://www.programiz.com/python-programming/first-program)

### Laboratorium 2
**Wstęp do programowania obiektowego**
1. Korzystanie z GIT i GitHUB
    - Zrób QuickStart: [quickstart](https://docs.github.com/en/get-started/quickstart)
    - Załóż repo na kod o nazwie po-laboratorium-2122
2. Powtórka - [OOP w Pythonie](https://www.programiz.com/python-programming/object-oriented-programming)
3. Zainstaluj Python w Visual Studio Code:     
   * https://code.visualstudio.com/docs/setup/setup-overview  
   * https://code.visualstudio.com/docs/python/python-tutorial
   * https://code.visualstudio.com/docs/python/environments     
4. Python w [writualnym środowisku](https://realpython.com/python-virtual-environments-a-primer/)
5. Wstęp do [Django](https://docs.djangoproject.com/en/4.0/intro/tutorial01/)

### Laboratorium 3
**Obiekty, modele, bazy danych i ORMs**  
Rozwiń swój projekt z Laboratorium 2 o dwa podstawowe obiekty: pytania i ankiety.  
1. Podążaj za krokami opisanymi: [Modele Django](https://docs.djangoproject.com/en/4.0/intro/tutorial02/)
Zaktualizuj repozytorium po-laboratorium-2122 z wynikami pracy.  


### Laboratorium 4
**Protokół HTTP, Widoki**  
Część teoretyczna: protokół HTTP - podstawa internetu  
Obejrzyj: [HTTP Crash Course & Exploration](https://www.youtube.com/watch?v=iYM2zFP3Zn0&ab_channel=TraversyMedia)
Część praktyczna:  
W aplikacji, warstwa odpowiedzialna za prezentację naszych modeli obiektowych nazywana jest widokiem (ang. view).
W przypadku aplikacji webowych, taki widok jest to zwykle strona w formacie HTML.  
Wykonaj ćwiczenia tutorialu Django: [Tworzenie widoków](https://docs.djangoproject.com/en/4.0/intro/tutorial03/)  
Zadanie Domowe:  
Utwórz swoję aplikacje Django w projekcie kursu. Temat aplikacji jest dowolny. Aplikacja musi zawierać przynajmniej trzy modele powiązane ze sobą przez:  
* [klucz obcy](https://docs.djangoproject.com/en/4.0/ref/models/fields/#foreignkey)
* [relacje wiele do wielu](https://docs.djangoproject.com/en/4.0/ref/models/fields/#manytomanyfield) 
   
Zaprezentuj modele na widoku admina.

Przykład zadania domowego:
Książka kucharska, zawierająca trzy modele: typ posiłku (śniadanie, obiad, kolacja), danie, składnik.  
`typ_posilku` składa się z dwóch pól:
```
ID (primary key)
Name 
```

`danie` składa się z pól:
```
ID (primary key)
Name
typ_posilku - klucz obcy
przepis - string
składniki - relacja wiele do wiele do składników
```

`składniki` składa się z pól:
```
ID  (primary key)
Nazwa
```

### Laboratorium 5
**Metoda HTTP Post, Formularze, Tworzenie obiektów**  
Część teoretyczna:  
[Różnica pomiędzy GET (podstawowa metoda sieci WEB) a PUT i POST.](https://www.freecodecamp.org/news/http-request-methods-explained/)

Część praktyczna:  
Do aplikacji ankieterskiej zostanie dodany formularz do rejestracji odpowiedzi. Umożliwia on wysłanie metody POST i przekazanie danych ze strony HTML do zapisania.
[Prosty formularz w Django](https://docs.djangoproject.com/en/4.0/intro/tutorial04/)

Praca własna:  
Bazując na wiedzy z Laboratorium 4 dodaj widoki do trzech modeli z własnej aplikacji. Widok powinien być zampowany do URL postaci `/nazwamodelu` i za pomocą menadżera obiektów wywoływać metodę `NazwaModelu.objects.all()` i wyświetlać stronę prezentującą wszystkie rekordy bazy danych w postaci tabeli. Do wyświetlenia strony skorzystaj z mechanizmy `templates`

### Laboratorium 6
**Moduł admin Django jako praktyczny przykład zastosowania dziedziczenia w programowaniu obiektowym**

Część teoretyczna:   
[Dziedziczenie i polimorfizm w python](https://www.youtube.com/watch?v=C2QfkDcQ5MU&ab_channel=KylieYing)  

Część praktyczna:  
Do modeli aplikacji ankieterskiej dodamy indywidualny interfejs zarządzania (admin).
Do modyfikacji sposobu wyświetlania modeli zastosujemy dziedczenie po klasach modułu `django.contrib.admin`

Praca własna:   
Bazując na wiedzy z laboratorium 5, przygotuj formularze do dodawania obiektów do Twojej aplikacji  
Bazując na wiedzy z Laboratorium 4 dodaj widoki do trzech modeli z własnej aplikacji. Widok powinien być zamapowany do URL postaci `/nazwamodelu` i za pomocą menadżera obiektów wywoływać metodę `NazwaModelu.objects.all()` i wyświetlać stronę prezentującą wszystkie rekordy bazy danych w postaci tabeli. Do wyświetlenia strony skorzystaj z mechanizmu `templates`
