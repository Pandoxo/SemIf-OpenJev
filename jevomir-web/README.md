# jevomir-web

Prosta strona do API jevomir: 1–2 zdjęcia, pytanie i 2–16 opcji → wybrana opcja,
prawdopodobieństwa i skalibrowana szansa poprawności.

`server.py` (tylko stdlib) serwuje `index.html` i przekazuje `/api/info` i `/api/score`
do API, dodając klucz po stronie serwera — klucz nie trafia do przeglądarki,
a API nie musi obsługiwać CORS.

```bash
echo "jev_..." > .api-key                # albo: export JEVOMIR_API_KEY=jev_... (.api-key jest w .gitignore)
python server.py                        # http://127.0.0.1:8080
# opcjonalnie: --port 9000, --host 0.0.0.0, --api-url https://... (albo JEVOMIR_API_URL)
```

Uwaga: `--host 0.0.0.0` udostępnia stronę (a więc i GPU) każdemu w sieci.
