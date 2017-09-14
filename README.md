# gpd-macos
Project Directory Generator for MacOS


## Prerequisites
- On Mac OS X, install [rails](https://gorails.com/setup/osx/10.12-sierra "Ruby on Rails").


## Syntax
    gpd [ domain [entity [project [application]]]]


## Parameters
    domain        Top level domain name abbreviation.

    entity        Company or organization name.

    project       Project or concept name.

    application   The name of the application or program.


By default, gpd with all parameters will create a rails application in the directory provided.  The project directory will contain the "trunk", "tags", & "branches" directories with the application being installed to the trunk directory.  Normall, only the first three (3) parameters are passed to create the structure, then navigating to the directory and running "rails new ..." to create the application in any of the directories under branches.


## Examples

Create a **website** directory structure for a company called **example.com**.
```
$ ./gpd.sh com example website
```

Create a **food blog** rails application in a directory structure for a company called **acme.org**.
```
$ ./gpd.sh org acme blog food
```

Create a **bootstrap tutorial** rails application based on a development branch of **W3Schools**.
```
$ ./gpd.sh com w3schools tutorial
$ cd GITRepositories/com/w3schools/tutorial/branches/develop
$ rails new learn-bootstrap
```


## Directory Structure
```
GITRepositories
└── domain
    └── entity
        └── project
            ├── branches
            │   ├── develop
            │   ├── feature
            │   ├── hotfix
            │   ├── release
            │   └── training
            ├── tags
            └── trunk
```
