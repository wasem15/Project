
Python Developer Info & Vacancies Portal

Django site presenting informational pages about the Python developer profession (home, skills, geography, demand) and a live vacancies view that fetches recent Python job postings from HeadHunter.

Features
- Informational pages: home, info, geography, skills rendered from the main app models.
- Vacancies: live fetch from HeadHunter API via main/utils.py and displayed in vacanvies_template.html.
- Media & static: MEDIA_ROOT configured to media/; static files in static/.

Quick start (Windows PowerShell)
1. Create and activate a virtual environment

	python -m venv venv
	.\venv\Scripts\Activate.ps1

2. Install dependencies (one-off, or create a requirements.txt):

	pip install django==4.1.5 requests

3. Run migrations and start the development server:

	python manage.py migrate
	python manage.py runserver

4. (Optional) Create a superuser to manage content via Django admin:

	python manage.py createsuperuser

Important notes
- The project expects at least one record per model in the database. Many views use Model.objects.all()[0] and will raise an IndexError if the table is empty. Use the Django admin or load fixtures to add initial content for Home, Demand, Geography, and Skills.
- The vacancies view calls main/utils.py::get_vacancies() and requires network access and the requests package.
- djangoProject1/settings.py contains a development SECRET_KEY and DEBUG = True. Keep these values private and set appropriate production settings before deployment.
- If you plan to serve uploaded images in production, configure a proper media server or cloud storage and update MEDIA_ROOT/MEDIA_URL accordingly.

Project structure (high level)
- manage.py — Django entrypoint
- djangoProject1/ — project settings and WSGI/ASGI
- main/ — app code: models.py, views.py, admin.py, utils.py, templates/, migrations/
- static/ — CSS, JS, images
- media/ — uploaded images used by models

Suggested GitHub repo name & description
- Name: python-vacancies-portal
- Short description: "Django site showing Python developer info, skills graphs and live job vacancies from HeadHunter."

Suggested topics
- django, python, web, jobs, vacancies, hh.ru

License
Consider adding an MIT license (LICENSE file) when publishing the repository.

---
Created for development and educational purposes. See djangoProject1/settings.py for configuration details.
