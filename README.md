# Grafik Orlen jako PWA

Ten folder to osobna wersja aplikacji jako PWA. Obecny plik `grafikgpt.html` nie został zmieniony.

## Co jest w folderze

- `index.html` - kopia aplikacji.
- `manifest.json` - nazwa, ikona i ustawienia instalowania aplikacji.
- `service-worker.js` - zapisuje aplikację do pamięci, żeby działała offline po pierwszym uruchomieniu.
- `icons/icon.svg` - ikona aplikacji.

## Jak najprościej przetestować na komputerze

PWA musi być otwarte przez adres `http://` albo `https://`. Samo kliknięcie `index.html` z dysku uruchomi aplikację, ale instalowanie/offline PWA może nie zadziałać.

Najprostszy test lokalny na Windows:

1. Otwórz PowerShell w tym folderze.
2. Uruchom:

```powershell
python -m http.server 8080
```

3. Wejdź w przeglądarce na:

```text
http://localhost:8080
```

4. W Edge/Chrome kliknij ikonę instalacji aplikacji na pasku adresu.

## Jak zrobić, żeby działało na Windows, Android i iPhone

Najwygodniej wrzucić cały folder na darmowy hosting statyczny, np. GitHub Pages, Netlify albo Cloudflare Pages.

Potem:

- Windows/Android: otwierasz link w Chrome/Edge i wybierasz instalację aplikacji.
- iPhone: otwierasz link w Safari, klikasz Udostępnij, potem `Do ekranu początkowego`.

Po pierwszym wejściu aplikacja powinna działać offline. Dane zapisują się osobno na każdym urządzeniu w pamięci przeglądarki.
