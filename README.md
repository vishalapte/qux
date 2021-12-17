# Qux: A Django Template

## Introduction

Qux is a django template with augmented models,
extra template tags, and useful utilities.

- [Core](auth/README.md)
- Auth
- SEO
- Templates
- TemplateTags
- Utils
  - `mysql`
  - `date`
  - `phone`

## Core [_qux_core_]

### Models

- `CoreModel`
  - `dtm_created`
  - `dtm_updated`
  - `to_dict(self)`
  - `get_dict(cls, pk)`
- CoreModelPlus - where all deleted rows are soft-deleted only


- `AbstractCompany`
- `AbstractContact`
- `AbstractContactPhone`
- `AbstractContactEmail`


- `Company`
- `Profile` - `OneToOne(User)`


- `DownloadLog`
- `UploadLog`
- `CoreURLLog`
- `CommLog`

## Auth [_qux_auth_]

### URLS

- _login/_
- _logout/_
- _change-password/_
- _password-reset/_

## SEO [_qux_seo_]

### Models

- `SEOSite` - `OneToOne(Site)`
- `SEOPage`

### Mixin

- SEOMixin

## Templates

- `_blank.html`

## Template Tags

### Library: qux

- `multiply`
- `divide`
- `atleast`
- `qux_min`
- `qux_max`
- `date_before`
- `addstr`
- `url_replace`
- `{% lineless %}{% endlineless %}`

### Library: quxform

- `is_checkbox` &rightarrow; `Boolean`

Add these configuration in `project/project/settings.py` file after adding `qux` app in your project
```sh
LOGIN_URL = '/login/'
LOGOUT_URL = '/logout/'
LOGIN_REDIRECT_URL = '/'
LOGOUT_REDIRECT_URL = '/'
SHOW_USERNAME_SIGNUP = False

ROOT_TEMPLATE = "_app.html"
```
