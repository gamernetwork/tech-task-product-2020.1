# Gamer Network Technical Task - Developer, Product

Hi!

In this task you will set up a working copy of a very, very simple news/reviews website, using some code provided.

The site is built using the Django framework (v1.11) and Python.

You will be asked to:

  - extend the basic `Post` model and render some new data
  - modify how the `Post` is rendered to include a new automatically inserted element
  - improve the aesthetics and accessibility of the site

The task is designed to allow you to demonstrate your ability to use new technology, to interpret specifications, to solve programming problems and to present information.

The task is intended to consume an evening - please do not spend more than 3 hours on it. If you do start to overrun significantly then please get in touch to discuss - we may have misjudged the timing!

If anything is unclear, please do no hesitate to get in touch. (The mind-reading test comes later...)

## Getting set up

Install **Python 3** if you don't already have it (should be fine on OSX and Linux).

Then, in a shell, run the following to set up the project:

```bash
git clone https://github.com/gamernetwork/tech-task-product-2020.1.git
cd tech-task-product-2020.1

# set up a python virtual environment
virtualenv .env
python -m venv .env

# install Django into this environment
.env/bin/pip install -r requirements.txt

# set up the database
.env/bin/python manage.py migrate
```

You will now have a `db.sqlite3` file in your project directory. This is your database.

```
# import 3 starting articles
.env/bin/python manage.py loaddata youreagamer_starting_articles

# set yourself up as a user for the backend of this site
.env/bin/python manage.py createsuperuser
```

You can now start a local development server (errors and access logs will show here) and get hacking

```
.env/bin/python manage.py runserver
```

Point your browser at http://127.0.0.1:8000 and you should see a list of 3 posts, which can be clicked.

The data for the site can be modified using the backend available here: http://127.0.0.1:8000/admin/ (log in using the superuser account you created.)

### Note regarding database

If you get into a mess with migrations, etc, you can just move/delete the `db.sqlite3` file and re-run the `migrate`, `loaddata` and `createsuperuser` steps again to get back to a fresh install.

## Tasks

Please do the following:

  1. Add the following fields to the `Post` model:
     1. datetime (mandatory, default to now)
     2. a subheading (not mandatory, max 200 characters)
  2. Refer to https://docs.djangoproject.com/en/1.11/topics/migrations/#workflow for steps to get your model changes into the database.
  3. Populate the new fields using the admin site.
  4. Render these new fields on each post page and on the index page
  5. Using either client-side (js) or server-side (python) code, insert a blue 300x250 advert placeholder in the main text flow on a post page (i.e. to interrupt reading), according to these constraints:
     1. An ad must not occur immediately before or after an image
     2. An ad must not occur at the start, not the end of the article
  6. Improve the design of the page to your taste, while achieving optimal readability on desktop and mobile devices

## Submitting your completed task

You should submit your work by email either as a zip/tar of code, or as a patch against the original repo.

Please do not file a pull request against the original repo - other candidates will see your work.

## Candidate's notes

Candidates should include explanatory notes here.

