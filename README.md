# Djream app

This template provides a minimal set up to get a React and Django project running.

## Running it

The React code is built and served by Vite, so you need to run this alongside Django.

To run Django, run the following commands:

```
cd server
poetry install
poetry run python manage.py migrate
poetry run python manage.py runserver
```

To run the Vite server, run the following commands:

```
cd client
npm install
npm run dev
```

Django is configured (using the `DJREAM_VITE_DEVSERVER_URL` setting) to make Djream fetch frontend code from the Vite devserver.

In production, you should build the frontend code with `npm run build` and set the `DJREAM_VITE_BUNDLE_DIR` to the location of the folder that contains the `manifest.json` file.
