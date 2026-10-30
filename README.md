# britishvalley.pl – strona hodowli Cattery British Valley PL

Strona na GitHub Pages (Jekyll), konto `bestadvice86`, DNS w nazwa.pl (ręczna konfiguracja).

## Edycja treści – panel
Panel: **https://britishvalley.pl/admin/** (Sveltia CMS). Każda zmiana zapisana w panelu to commit w tym repo; strona przebudowuje się w 1–2 minuty.

Co edytuje się w panelu (pliki w `_data/`):
- `mioty.yml` – mioty, kocięta (status: Dostępne / Zapytaj o dostępność / Zarezerwowane / W nowym domu), filmy (link YouTube albo plik MP4),
- `galeria.yml` – przesuwana galeria na górze,
- `koty.yml` – rodzice (samice/samce),
- `strona.yml` – teksty, kroki rezerwacji, kontakt.

Zdjęcia wgrane w panelu trafiają do `img/`, są automatycznie zmniejszane do 1600 px i zapisywane jako WebP. Pliki wideo do 50 MB.

Logowanie: GitHub (token dostępu albo „Sign in with GitHub” przez autoryzator Sveltia na Cloudflare Workers). Osoba edytująca musi mieć prawo zapisu do repo.

## Pliki
- `index.html` – szablon strony (Liquid), treść bierze z `_data/`.
- `admin/` – panel (`config.yml` opisuje pola formularzy).
- `logo.png` – logo hodowli (przezroczyste tło), `favicon.png` – ikona karty.
- `CNAME` – domena.
