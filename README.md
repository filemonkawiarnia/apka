# Filemon — Książeczka zdrowia kotów

Aplikacja PWA (Progressive Web App) — działa jak normalna apka na telefonie,
z dostępem do aparatu, ale bez instalacji ze "store'u". Dane zapisują się
lokalnie w pamięci przeglądarki na danym urządzeniu (localStorage).

## Zawartość

- `index.html` — cała aplikacja (HTML + CSS + JS, bez zależności)
- `manifest.json` — opis apki (ikona, nazwa, kolory)
- `sw.js` — service worker (działanie offline)
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`, `apple-touch-icon.png` — ikony

## 1. Wgranie na GitHub Pages

1. Wejdź na https://github.com i zaloguj się (lub załóż konto — to chwila).
2. Kliknij **New repository** (zielony przycisk w prawym górnym rogu).
   - Nazwa np. `filemon-ksiazeczka`
   - Zaznacz **Public**
   - Kliknij **Create repository**
3. Na stronie nowego repo kliknij **uploading an existing file**
   (albo `Add file` → `Upload files`).
4. Przeciągnij i upuść **wszystkie pliki z tego folderu na raz**
   (index.html, manifest.json, sw.js i 4 pliki ikon).
5. Kliknij **Commit changes** na dole strony.
6. Wejdź w zakładkę **Settings** repozytorium → w menu po lewej **Pages**.
7. W sekcji **Build and deployment** → **Source** wybierz **Deploy from a branch**.
8. Branch: `main`, folder: `/ (root)` → **Save**.
9. Odczekaj 1–2 minuty, odśwież stronę Pages — pojawi się link, np.:
   `https://twoja-nazwa.github.io/filemon-ksiazeczka/`

## 2. Instalacja na telefonie (jako "apka")

### Android (Chrome)
1. Otwórz powyższy link w Chrome.
2. Dotknij menu (trzy punkty w rogu) → **Dodaj do ekranu głównego** /
   **Zainstaluj aplikację**.
3. Na ekranie głównym pojawi się ikona Filemon — otwiera się na pełnym
   ekranie, bez paska adresu, z dostępem do aparatu.

### iPhone (Safari)
1. Otwórz link w **Safari** (musi być Safari, nie Chrome).
2. Dotknij ikony **Udostępnij** (kwadrat ze strzałką w górę).
3. Wybierz **Dodaj do ekranu początkowego**.
4. Potwierdź — ikona Filemon pojawi się na ekranie głównym.

## 3. Ważne informacje o danych

- Dane (karty kotów, zdjęcia, historia medyczna) są zapisywane **lokalnie,
  tylko w tej przeglądarce na tym urządzeniu**. Nie są automatycznie
  współdzielone między telefonami.
- W zakładce **„Dane"** (prawy górny róg apki) jest możliwość:
  - **Eksportu** danych do pliku `.json` (kopia zapasowa / przeniesienie na
    inne urządzenie),
  - **Importu** takiego pliku (np. na innym telefonie).
- Warto regularnie robić eksport jako backup, zwłaszcza przed aktualizacją
  systemu czy zmianą telefonu.
- Jeśli w przyszłości będziecie chcieli, żeby **wszystkie osoby ze
  stowarzyszenia widziały te same dane na żywo**, trzeba dodać wspólną bazę
  w chmurze (np. darmowy Firebase) — to wymaga dodatkowej, jednorazowej
  konfiguracji.

## 4. Aktualizacje aplikacji

Jeśli w przyszłości poprosisz o zmiany w aplikacji, wystarczy zastąpić plik
`index.html` (i ewentualnie inne pliki) nową wersją w tym samym repozytorium
GitHub (Add file → Upload files → ten sam plik, nadpisze stary). Strona
zaktualizuje się automatycznie po odświeżeniu.
