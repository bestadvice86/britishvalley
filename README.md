# britishvalley.pl – strona hodowli Cattery British Valley PL

Statyczna strona (jeden plik `index.html`) hostowana na GitHub Pages, konto `bestadvice86`, DNS w nazwa.pl. Ten sam układ co oferta.jagodowa.com.

## Pliki
- `index.html` – cała strona. Miejsca do uzupełnienia mają klasę `uzupelnij` (żółte tło). Przed publikacją nie może zostać żadne.
- `logo.svg` – logo **tymczasowe**. Podmienić na oryginalne logo hodowli (kot z jednej linii z okładki FB) w wersji SVG lub PNG od Gosi. W `index.html` znak w nagłówku i hero też trzeba wtedy zamienić na `<img src="logo.svg">`.
- `img/` (do utworzenia przy pierwszych zdjęciach) – zdjęcia kotów. Format JPG lub WebP, dłuższy bok około 1200 px, do około 300 KB na plik.
- `CNAME` – domena dla GitHub Pages.

## Wdrożenie
1. GitHub, konto bestadvice86: nowe repozytorium `britishvalley` (publiczne), wgrać zawartość folderu.
2. Settings → Pages → Source: *Deploy from a branch*, gałąź `main`, folder `/ (root)`.
3. Custom domain: `britishvalley.pl`. Najlepiej wcześniej zweryfikować domenę w ustawieniach konta (Settings → Pages → Verified domains, rekord TXT), co chroni przed przejęciem domeny.
4. Po wydaniu certyfikatu (do kilkudziesięciu minut) zaznaczyć **Enforce HTTPS**.

## DNS w nazwa.pl (britishvalley.pl, ręczna konfiguracja)
| Typ | Host | Wartość |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | bestadvice86.github.io. |

Usunąć domyślne rekordy A/CNAME nazwa.pl dla `@` i `www`. **Rekordów MX, SPF/TXT i DKIM (poczta) nie ruszać.**

britishvalley.com (jeśli kupiona): przekierowanie 301 w panelu nazwa.pl na `https://britishvalley.pl`. Jedno repozytorium Pages obsługuje tylko jedną domenę własną.

## Aktualizacja kociąt
W sekcji `#kocieta` każdy miot to blok `<div class="litter">`, a każde kocię to `<article class="kitten">`. Status zmienia się klasą:
`st-free` (Dostępne) · `st-res` (Zarezerwowane) · `st-home` (W nowym domu).
