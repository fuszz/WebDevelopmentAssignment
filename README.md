# Web Development Final Assignment
Repo containing my team's final assignment on Web Development lecture.

# [PL] Projekt zaliczeniowy z przedmiotu Web Development
W ramach zaliczenia przedmiotu WebDevelopment, zgodnie z ustaleniami z prowadzącym, przygotowaliśmy do oceny projekt realizowany w wolnym czasie w ramach działalności w Studenckim Kole Naukowym Informatyki UMCS. 
Repozytoria projektu są dostępne w organizacji [SKNI](https://github.com/skni-umcs):
- [Backend](https://github.com/skni-umcs/mordorappka-backend)
- [Frontend](https://github.com/skni-umcs/mordappka-web)

  
Projekt został spakowany w kontenery, aby umożliwić Prowadzącemu ocenę pracy. 

# Instrukcja uruchomienia
1. Pobrać plik `docker-compose.yml` z repozytorium.
2. Zainstalować narzędzie `Docker` wraz z poleceniem `docker compose`
3. W folderze, w którym zapisano plik `docker-compose.yml` wywołać komendę `docker compose up`
4. Po ok. 70 sekundach aplikacja powinna pracować prawidłowo.
5. Backend pracuje na gnieździe `localhost:5000`
6. Frontend - na gnieździe `localhost:8080`
7. Baza danych - na gnieździe `localhost:5432`
8. W celu przejrzenia wnętrza bazy danych można zalogować się do niej np. za pomocą narzędzia pgAdmin, login `morda`, hasło `my_secret`

# Nazwa
Pomysł na nazwę pojawił się, kiedy nasi starsi koledzy zaczęli tworzyć alternatywę dla Morii, którą - pod wpływem fascynacji uniwersum Władcy Pierścieni - nazwano Mordorem. Stąd właśnie tytuł MordAppka i nazwa użytkownika w bazie danych - skrót (`morda`). 

# Wykorzystane technologie
## Backend
- SpringBoot – framework do szybkiego tworzenia aplikacji webowych w Javie, oparty na Springu.
- Hibernate – biblioteka ORM mapująca obiekty Java na rekordy w relacyjnych bazach danych.
- LiquiBase – narzędzie do śledzenia, wersjonowania i automatycznego wdrażania zmian w bazie danych.
- Lombok – biblioteka, która automatycznie generuje kod jak gettery, settery czy konstruktory, ograniczając boilerplate.
- Swagger – zestaw narzędzi do automatycznego generowania i testowania dokumentacji REST API. (localhost:5000/api/swagger-ui/index.html)

## Frontend
- TypeScript – nadzbiór JavaScriptu wprowadzający typowanie statyczne i ułatwiający rozwój większych aplikacji.
- React – biblioteka do budowania interfejsów użytkownika, oparta na komponentach i wirtualnym DOM.

## Baza danych
- PostgreSQL - zaawansowany, otwartoźródłowy system zarządzania relacyjnymi bazami danych.
### Struktura bazy danych:
- tabela `faculties` - przechowuje informacje o wydziałach
- tabela `majors` - przechowuje informacje o kierunkach studiów
- tabela `rooms` - przechowuje informacje o salach wykładowych
- tabela `teachers` - przechowuje informacje o nauczycielach akademickich
- tabela `classes` - przechowuje informacje o terminach zajęć 
- tabela `term_groups` - przechowuje informacje o unikatowych grupach zajęciowych. Taka grupa zajęciowa jest rozumiana jako iloczyn semestru i kierunku studiów
- tabela `periods` - przechowuje informacje o semestrach (w sensie chronologicznym)
- tabela `subjects` - przechowuje informacje o przedmiotach wykładowych
### Schemat struktury bazy danych
![image](https://github.com/user-attachments/assets/fde820c6-0564-4726-bf40-65dbe5f3877e)

