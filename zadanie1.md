1. Polecenie budowania kontenera

docker buildx build -t skowyrab/pch_labs:zadanie1v5 --sbom=true --provenance=mode=max --push --cache-to=type=registry,mode=max,ref=skowyrab/pch_labs_cache:zad1v2 --cache-from=type=registry,ref=skowyrab/pch_labs_cache:zad1v2 .

2. Polecenie uruchomienia kontenera

docker run -d -p 8080:3000 skowyrab/pch_labs:zadanie1v5

3. Polecenie uzyskania informacji, które serwer zostawił w logach
docker logs f383d443b9ce

4. Polecenie sprawdzające ile warstw ma obraz:
docker history skowyrab/pch_labs:zadanie1v5

5. Działanie aplikacji:
- plik ze zrzutem ekranu przedstawiającym wyświetlenie danych w oknie przeglądarki dołączony jest do repozytorium pod nazwą aplikacja.png

6. Konkurs
- plik ze zrzutem ekranu z oceną CVSS jest dołączony do repozytorium pod nazwą CVSS.png
- Rozmiar obrazu: 42.46MB