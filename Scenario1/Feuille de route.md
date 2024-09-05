1. cd Scenario1
2. docker build -t phpcegep .
3. docker run -it -p 8000:8000 --rm -v CHEMIN/SUR/TA/MACHINE/HÔTE:/app phpcegep bash
4. composer create-project laravel/laravel UnProjet
5. cd UnProjet
6. php artisan serve --host 0.0.0.0 --port 8000