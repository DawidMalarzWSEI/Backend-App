# System Recenzji

Projekt zaliczeniowy składa się z kilku mikroserwisów, napisanych w C# z użyciem architektury Onion. Aplikacja umożliwia użytkownikom dodawanie recenzji oraz komentarzy.

Onion Architecture, znana również jako Hexagonal Architecture lub Ports and Adapters Architecture, jest wzorcem architektonicznym, który promuje modularność, łatwość testowania i odizolowanie różnych warstw aplikacji. Opiera się na zasadzie odwróconej zależności, gdzie najbardziej wewnętrzne warstwy zawierają najważniejszą logikę biznesową, a zewnętrzne warstwy dostarczają interfejsy do komunikacji z innymi modułami.


## Wymagania

1. Docker
2. Docker-compose

## Instalacja

1. Sklonuj repozytorium
```
git clone https://github.com/DawidMalarzWSEI/Backend-App.git
```
2. Przejdź do katalogu głównego projektu
```
cd Backend-App
```
3. Zbuduj obrazy Docker
```
docker-compose build
```
4. Uruchom kontenery
```
docker-compose up
```

## Usługi

Model aplikacji mikroserwisowej dla bloga składa się z następujących usług:

1. Usługa uwierzytelniania: Odpowiedzialna za uwierzytelnianie i autoryzację użytkowników.
2. Usługa recenzji: Zarządza tworzeniem, pobieraniem i zarządzaniem recenzjami.
3. Usługa komentarzy: Zarządza komentarzami przypisanymi do recenzji.

## Wykorzystane technologie

Aplikacja jest budowana przy użyciu następujących technologii:
- Docker: Platforma konteneryzacji służąca do pakowania komponentów aplikacji.
- MongoDB: Baza danych NoSQL używana do przechowywania wpisów na blogu, komentarzy i informacji o użytkownikach.
- .NET 6: Wieloplatformowy framework do budowania mikroserwisów i interfejsów API.
- Nginx: Serwer sieciowy używany jako odwrócona proxy do obsługi routingu i równoważenia obciążenia między mikroserwisami.
- RabbitMQ: Broker wiadomości używany do asynchronicznej komunikacji między mikroserwisami.

## Dokumentacja

Każdy mikroserwis posiada dokumentację Swagger, która umożliwia szybkie i łatwe zrozumienie API. Możesz ją zobaczyć, otwierając odpowiednią stronę na odpowiednim porcie (zakres od 5000 do 5005).

Przykładowo, aby otworzyć dokumentację dla serwisu na porcie 5005, otwórz przeglądarkę i wprowadź następujący adres: [https://localhost:5005/swagger/index.html](https://localhost:5005/swagger/index.html)
