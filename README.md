# Odoo 11.0 Windows Installation
Install odoo-11.0 from source on Windows

Download and install [Git for Windows](https://git-scm.com/download/win).<br />
Download and install [Node.js LTS](https://nodejs.org/en/download/).<br />
<br />
Launch `Git Bash` as Administrator.
 * Install `Less.js` by `$ npm install -g less less-plugin-clean-css`

Download and install [PostgreSQL](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads).<br />
add PostgreSQL's `bin` directory (default: `C:\Program Files\PostgreSQL\x.x\bin`) to your `PATH`.<br />
<br />
create a `postgres` user with a password using the `PgAdmin` GUI:<br />
 * open `PgAdmin4`,
 * expand `server` node to create a connection,
 * expand `PostgreSQL` node,
 * select **Object-> Create -> Login/Group Role**,
    * enter the username in the `Role Name` field (e.g. odoo),
    * open the `Definition` tab and enter the password (e.g. odoo),
    * open the `Privileges` tab and give `login` and `create database` rights,
 * click `save`.

Download and install <a href="https://www.python.org/downloads/" target="_blank">Python3</a>.<br />
 * goto `C:\Users\rangw\AppData\Local\Programs\Python\PythonXX`.<br />
 * rename `python.exe` to `python3.exe` and `pythonw.exe` to `pythonw3.exe`.<br />
 * add `C:\Users\rangw\AppData\Local\Programs\Python\PythonXX` to your `PATH`.<br />

Launch `Git Bash` as Administrator (for all `pip` installation).<br />
 * Install `pypiwin32` by `$  python3 -m pip install pypiwin32`
 * Install `psycopg2` by `$  python3 -m pip install psycopg2-2.7.3-cp36-cp36m-win_amd64.whl`
 * Install `python-ldap` by `$ python3 -m pip install pyldap-2.4.37-cp36-cp36m-win_amd64.whl`
 * Install `gevent` by `$ python3 -m pip install gevent-1.2.2-cp36-cp36m-win_amd64.whl`
 * Install `psutil` by `$ python3 -m pip install psutil-5.3.1-cp36-cp36m-win_amd64.whl`
 * Install `lxml` by `$ python3 -m pip install lxml-3.8.0-cp36-cp36m-win_amd64.whl`
 * Install `Pillow` by `$ python3 -m pip install Pillow-3.4.2-cp36-cp36m-win_amd64.whl`
 * Install `reportlab` by `$ python3 -m pip install reportlab-3.4.0-cp36-cp36m-win_amd64.whl`

Install remaining requirements using
 * `$ python3 -m  pip install -r requirements.txt`
 * `$ python3 -m pip install -U werkzeug`

Download and install [wkhtmltox](https://wkhtmltopdf.org/downloads.html).<br />
Add `C:\Program Files\wkhtmltopdf\bin` to `PATH`<br />
<br />
Launch `Git Bash`.<br />
Goto `odoo` installation directory and run `odoo` using<br />
`$ python3 odoo-bin -w odoo -r odoo --addons-path=addons --log-level=debug_rpc`<br />
