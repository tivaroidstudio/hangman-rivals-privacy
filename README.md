# Hangman: Rivals — publiczne strony prawne

Ten katalog jest samodzielną, statyczną stroną bez cookies, analityki i zewnętrznego JavaScriptu.

Docelowe adresy wpisane w aplikacji:

- polityka: `https://hangman-rivals-privacy.pages.dev/`
- usuwanie konta: `https://hangman-rivals-privacy.pages.dev/delete-account.html`

## Darmowe wdrożenie przez Cloudflare Pages

1. Zaloguj się na `https://dash.cloudflare.com/`.
2. Otwórz **Workers & Pages → Create → Pages → Upload assets**.
3. Jako nazwę projektu wpisz dokładnie `hangman-rivals-privacy`.
4. Przeciągnij cały katalog `PrivacySite` albo archiwum ZIP zawierające jego pliki.
5. Kliknij **Deploy site**.
6. Sprawdź w trybie incognito oba adresy podane powyżej.
7. Jeśli nazwa jest zajęta i Cloudflare nada inny adres, zmień oba adresy w `Assets/Hangman/Scripts/LegalLinks.cs` przed kolejnym buildem.
8. Po każdej zmianie użyj w projekcie Pages opcji **Create deployment / Upload assets**, wgraj ponownie zawartość katalogu i sprawdź datę wdrożenia.

W Google Play Console wpisz:

- **Polityka prywatności:** adres strony głównej;
- **Usuwanie konta / Data deletion URL:** adres `delete-account.html`.

Publiczna strona nie ma dostępu do Unity i nie usuwa danych automatycznie. Bezpieczne zgłoszenie tworzy zalogowana gra przez Cloud Code. Dla osoby bez aplikacji pozostaje ręczna ścieżka e-mail z weryfikacją zgodnie z `Docs/ACCOUNT_DELETION_RUNBOOK.md`.

Plik `_headers` dodaje CSP, HSTS i blokady niepotrzebnych funkcji przeglądarki. Po wdrożeniu zweryfikuj nagłówki np. przez `https://securityheaders.com/`.
