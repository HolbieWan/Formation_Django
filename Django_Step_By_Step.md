# Tuto Django

## 1-Creer venv:
in root repo create and activate venv

## 2-Demarer projet
```bash
django-admin startproject nom-du-projet
```

## 3-Renommer dossier avec le nom du projet en src (pour plus de clareté)

## 4-Choisir language pour le pannel Admin:
dans **settings.py** : 
```bash
LANGUAGE_CODE = 'en-us' ou 'fr'
```

## 5-Lancer server local:
depuis le dossier **src**:
```bash
python3 manage.py runserver
```
-> se lance sur localhost

## 6-Crééer fichier run_server.sh
dans le dossier nom-de-projet, créer un fichier run_server.sh pour automatiser le lancement du server, contenu: 
+ Aller dans venv/bin/ clique-droit sur python -> copy absolute path
+ puis copier chemin absolu pour manage.py

```python
chemin-complet-vers-python chemin-complet-manage.py runserver
```
en executant ce fichier run_server.sh un fichier config est créé et le server django démare

## 7-Edit configuration:
renommer config selon son choix

## 8-Resoudre erreur de lancemant server:
depuis /src: 
```bash
python3 manage.py migrate
```
-> applique les migration pour créer les tables de la Base de Donnée

## 9-Créer super user:
-> relancer server
-> aller dans localhost/admin (interface admin - login )

depuis src: 
```bash
python manage.py createsuperuser
```
entrer ses info puis:
-> relancer les serveur
-> se connecter à l'admin en superuser

## 10-Résumé: 
```bash
django-admin startproject
manage.py runserver
manage.oy migrate
manage.py crceatesuperuser
```

## 11-Créer une application:
```bash
python mnage.py startapp nom-de-app
```
cela crée:
-> /migrations
-> __init__.py
-> admin.py
-> apps.py
-> models.py
-> tests.py
-> views.py

