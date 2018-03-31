ResearchMatch
-------------

ResearchMatch is an open source Web application written in Rails 3 designed
to facilitate the matching of students (in particular, but not necessarily,
undergraduate students) to research positions offered by faculty at
university. ResearchMatch uses tags and user-specified parameters to
suggest research positions for students, manages the application to jobs
by students and allows for the submission of a resume and/or transcript
in the research application.


## How to run this Ruby on Rails application?
1. Download [Docker](https://docker.com)
2. Create a file called 'config/database.yml'
3. Boot the application
    - Terminal Command: `docker-compose up`
4. In another terminal, do the following rake commands:
    - `rake db:setup_yml`
    - `rake ldap:setup`
4. Create the database
    - In another terminal, run: `docker-compose run web rake db:create:all`
    - Afterwards, run: `docker-compose run web rake db:migrate`
5. Within a browser, open: `localhost:3000`
6. [Optional] Boot the application again
    - Same procedure as step 2
    - [Reminder](https://docs.docker.com/compose/rails/): Delete the file `tmp/pids/server.pid` if you stop the application with `Ctrl-C` in the same shell in which you executed the `docker-compose up`
7. To stop the application, run [docker-compose down](https://docs.docker.com/compose/reference/down/) in your project directory (preferably in a different shell than the one in which you executed the `docker-compose up`)

Having some trouble? Try consulting this [wiki](https://github.com/ucberkeley/Beehive/wiki/)!
