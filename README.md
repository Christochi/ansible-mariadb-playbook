# Ansible-MariaDB-Playbook

## Description
Ansible Playbook for installation and configuration of mariadb database in Amazon Linux. The Playbook consists of the following directories:
- `files`
- `templates`
- `defaults`
- `tasks`
- `handlers`

### files
Sample compressed bzip2 sql script. Script creates tables and loads data into the database. The sample sql script is from this website https://www.sqltutorial.org/sql-sample-database

### templates
`my.cnf.j2` is MariaDB configuration file. Sample MariaDB option files can be found in `usr/share/mysql` directory. You can copy one of the sample MariaDB option files and use it as the basis for building your server's primary MariaDB option file.

### defaults
All referenced variables are in the `main.yml` in the `defaults` directory. ***Boolean variables are used as a form of control to turn configuration or commands ON/OFF***

### tasks
The files are the tasks ansible will perform:
- **config.yml:** templates `my.cnf.j2` to the server
- **dependencies.yml:** installs other dependencies required by the OS or application
- **initialize.yml:** creates and configures the database
- **mariadb-install.yml:** installs MariaDB
- **main.yml:** calls the other tasks to perform when ansible plays the playbook

***More functionalities will be added to the playbook. Feel free to make any pull requests, report issues or offer some advice and feedback***
