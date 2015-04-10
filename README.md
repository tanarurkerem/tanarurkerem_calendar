Calendar Drupal Feature
=======================

This is a simple feature wich contains calendar installation with one simple event type.

HOWTO USE
---------

### Make a new Drupal installation with calendar feature:

* `drush make https://raw.github.com/tanarurkerem/tanarurkerem_calendar/master/build.make [WEBDIR]`
* Install Drupal (`drush si [YOUR OPTIONS]`)
* Enable Features module (`drush en -y features`)
* Enable Tanarurkerem calendar feature at admin/structure/features (`drush en -y tanarurkerem_calendar`)

### Install Tanarurkerem calendar feature to an existing site

* `drush make --no-core --tar https://github.com/tanarurkerem/tanarurkerem_calendar/raw/master/build.make tanarurkerem_calendar`
* Mac OSX - bsdtar 2.8.3 - libarchive 2.8.3

 `tar -x -s /tanarurkerem_calendar// -C [YOUR DRUPAL WEB DIR] < tanarurkerem_calendar.tar.gz`

* Ubuntu - (GNU tar) 1.25

 `tar -x -z --xform s/tanarurkerem_calendar// -C [YOUR DRUPAL WEB DIR] < ./tanarurkerem_calendar.tar.gz`

### Use it in a .make file

* add a following lines to your make file:

```
projects[tanarurkerem_calendar][type] = module
projects[tanarurkerem_calendar][subdir] = features
projects[tanarurkerem_calendar][download][type] = git
projects[tanarurkerem_calendar][download][url] = git://github.com/tanarurkerem/tanarurkerem_calendar.git
```
