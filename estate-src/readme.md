## Requirements
### django=3.2.7

### djangorestframework=3.12.4
Django REST framework is a powerful and flexible toolkit for building Web APIs.

### django-environ=0.7.0
Python package that allows you to use [Twelve-factor methodology](https://www.12factor.net/) to configure your Django application with environment variables.

### django-filter=21.1
Provides filtering supp for django rest Framework
Django-filter is a generic, reusable application to alleviate writing some of the more mundane bits of view code. Specifically, it allows users to filter down a queryset based on a model’s fields, displaying the form to let them do this.

### django-autoslug=1.9.8
Django-autoslug is a reusable Django library that provides an improved slug field which can automatically:

1.Populate itself from another field.
2.Preserve uniqueness of the value.
3. Use custom slugify() functions for better i18n.

The field is highly configurable.

### django-countries=7.2.1
A Django application that provides country choices for use with forms, flag icons static files, and a country field for models.

### Pillow=8.3.2
The Python Imaging Library adds image processing capabilities to your Python interpreter.

This library provides extensive file format support, an efficient internal representation, and fairly powerful image processing capabilities.

The core image library is designed for fast access to data stored in a few basic pixel formats. It should provide a solid foundation for a general image processing tool.

### django-phonenumber-field=5.2.0
A Django library which interfaces with python-phonenumbers to validate, pretty print and convert phone numbers. python-phonenumbers is a port of Google’s libphonenumber library, which powers Android’s phone number handling.

### phonenumbers=8.12.33
Python version of Google's common library for parsing, formatting, storing and validating international phone numbers.

### psycopg2-binary=2.9.9
Psycopg is the most popular PostgreSQL database adapter for the Python programming language. Its main features are the complete implementation of the Python DB API 2.0 specification and the thread safety (several threads can share the same connection). It was designed for heavily multi-threaded applications that create and destroy lots of cursors and make a large number of concurrent “INSERT”s or “UPDATE”s.

### flake8=3.9.2
Flake8 is a Python linting tool that checks your Python codebase for errors, styling issues and complexity. 

Flake8 is a wrapper around these tools:

PyFlakes

pycodestyle

Ned Batchelder’s McCabe script

Flake8 runs all the tools by launching the single flake8 command. It displays the warnings in a per-file, merged output.

### black=21.6b0
Black is the uncompromising Python code formatter. By using it, you agree to cede control over minutiae of hand-formatting. In return, Black gives you speed, determinism, and freedom from pycodestyle nagging about formatting. You will save time and mental energy for more important matters.

### isort=5.9.3
isort is a Python utility / library to sort imports alphabetically and automatically separate into sections and by type.

### setup setup.cfg, gitignore and .env file and update settings.py accordingly

### create apps folder
### create by users,profiles,common,ratings apps ```python manage.py startapp users```

### add ```django.contrib.sites``` , SITE_ID, THIRD_PARTY_APPS, LOCAL_APPS and INSTALLED_APPS

## Configure PostreSQL server and create databse

# Django Login
## Good logging is critical to debugging 
### Python logging module is resposible for system loging in Django
### Python Logging Components are - Loggers , Handlers , Filters and Formaters

## Logger Level - 
### Debug - Low level system infomation
### INFO - General system information
### Warning - Minor problem occured
### Error - Major problem occured
### Critical - Critical problem occured

## Handlers -
- Determines what happens to each message in a logger
### FileHandler
### StreamHandler
### SMTPHandler

## Filters
- Determines which log records pass from loggers to handler
- Filter log messages based on e.g. - log levels etc.
- Can be applied to both loggers and handlers

## Formatters
- Describe exact format of text
- Format and convert log records

# Custom User
## Abstract User - have existing user model and just want to remove user name field
## Abstract BaseUser - Use this to start from scratch by creating completely new user model

# UUIDs - Universally Unique IDentifier

- Obscure ID's, making it virtually impossible for attackers to guess ID's
- Obscure Foreign Keys references
- Allow for horizontal partioning without key collision or rekeying concerns

## Disadvantages
- At scale, they cause massive insert performance issues
- no quick "sort by id" chronology available
- disadvantage can be avoided using pseudo primary key

## Serializers
- Serializers allow complex data such as querysets and model instances to be converted to native Python datatypes that can then be easily rendered into JSON, XML or other content types. Serializers also provide deserialization, allowing parsed data to be converted back into complex types, after first validating the incoming data.

- The serializers in REST framework work very similarly to Django's Form and ModelForm classes. We provide a Serializer class which gives you a powerful, generic way to control the output of your responses, as well as a ModelSerializer class which provides a useful shortcut for creating serializers that deal with model instances and querysets.

## Token Based Authentification

### Djoser 
- provides API endpoints for registration, login/logout, password change/reset, social auth etc.


## mailtrap.io
- SMTP server design to run in dev or test environment
- Design to champ an email the app is sending and displays it in web interface instead of sending it to user.
- It helps to prevents any test email sending to real people no matter what address is provided.

## send grid
- SendGrid provides an SMTP service that allows you to deliver your email via their servers instead of your own client or server. This means we can count on SendGrid's delivery at scale for our SMTP needs.

## API Testing

### Postman


## Exception handlers and renderers
- exception  handlers allows errors to be handling cleanly
- renderers allow us to return reponses with various media types.


# Configure Djagno Application with Docker
## Install Docker Desktop
### Containers - Containers are an isolated environment to run any code.
### Containerisation - Containerization is a process of packaging your application together with its dependencies into one package (a container). Such a package can then be run pretty much anywhere, no matter if it's an on-premises server, a virtual machine in the cloud, or a developer's laptop.
### Docker file - It is a text file that contains instructions, at times called commands or directives, which dictate how to create a Docker image.

## makefile 
- make is a traditional Unix utility which reads a Makefile to decide what programs to run to reach a particular goal. Typically, that goal is to build a piece of software from a set of source files and libraries; but make is general enough to be used for various other tasks, too, like assembling a PDF from a collection of TeX source files, or retrieving the newest versions of each of a list of web pages.
 cmd eg - ```MinGW32-make build```

## PEP 518
- defines pyproject.toml as a configuration file to store build system requirements for python projects

## black - 
### Black is a tool that can reformat Python code. It's remarkable for it's lack of configuration
## ishort -
### isort is a Python utility / library to sort imports alphabetically, and automatically separated into sections and by type. It provides a command line utility, Python library and plugins for various editors to quickly sort all our imports.

## flake8 - 
### Flake8 will output any errors or violations it detects, along with a line number and a description of the issue. By default, Flake8 checks for errors and violations of PEP 8 style guidelines.