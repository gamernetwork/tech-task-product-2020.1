## Getting started

Install Python if you don't already have it.

In a shall, run the following.

```bash
git clone git@github.com:gamernetwork/tech-task-frontend-2018.1
cd tech-task-frontend-2018.1

# set up a python virtual environment
virtualenv .env

# install Django into this environment
.env/bin/pip install django

# set up the database
.env/bin/python manage.py migrate

# set yourself up as a user for the backend of this site
.env/bin/python manage.py createsuperuser
```

## Tasks

  - Add the following fields to each post:
    - datetime
    - a subheading
  - Render these new fields on each post page and on the index page
  - Insert a blue 300x250 advert placeholder in the main text flow on a post page (i.e. to interrupt reading), according to these constraints:
    - An ad must not occur immediately before or after an image
    - Ad ad must not occur at the start, not the end of the article
  - Improve the design of the page to your taste, while achieving optimal readability on desktop and mobile devices
