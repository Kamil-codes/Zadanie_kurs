# Chatbot AI z analizą danych
Aplikacja webowa łącząca czat z Claude (Anthropic) z możliwością przesyłania
i analizowania plików CSV, model generuje narracyjne podsumowanie danych
w formie czytelnego raportu HTML.
# Funkcje
- Czat z Claude z obsługą historii rozmowy
- Upload plików CSV i automatyczna analiza z wykresem
- System logowania (hasła hashowane przez bcrypt)
- Rate limiting chroniący przed nadużyciami
- Ochrona przed prompt injection
# Wymagania
- Python 3.10 lub nowszy
- Konto na console.anthropic.com z kluczem API
# Instalacja lokalna
1. Sklonuj repozytorium:
```bash
git clone https://github.com/twoj-login/nazwa-repo.git
cd nazwa-repo
```
2. Stwórz i aktywuj wirtualne środowisko:
```bash
python -m venv venv
source venv/bin/activate
```
3. Zainstaluj zależności:
```bash
pip install -r requirements.txt
```
4. Stwórz plik .env w głównym folderze i uzupełnij:
```
ANTHROPIC_API_KEY=twoj-klucz-tutaj
SECRET_KEY=dowolny-dlugi-losowy-tekst
```
5. Uruchom appkę:
```bash
python app.py
```
6. Otwórz w przeglądarce: http://127.0.0.1:8080
# Zmienne środowiskowe
| Nazwa | Opis | Wymagane |
| -| -| -|
| ANTHROPIC_API_KEY | Klucz API do Claude | Tak |
| SECRET_KEY | Sekret do podpisywania sesji Flaska | Tak |
| PORT | Port appki (ustawiane automatycznie przez platformę) | Nie |
# Struktura projektu
```
app.py główny plik appki (routes, logika)
templates/ szablony HTML (Jinja2)
static/ CSS i wygenerowane raporty
requirements.txt lista zależności Pythona
Procfile instrukcja uruchomienia dla platformy hostingowej
```

# Autor
[Twoje imię / nazwa], projekt stworzony w ramach kursu.