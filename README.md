# Rift DPS HPS Leaderboards

Python scripts, MySQL Database and templates with which the leaderboards are created. The script scrapes data from https://prancingturtle.com/, enters it into a database and generates html files in the public folder. It is also possible to automate the upload of html files to a web server via a crontab.

Example Website: https://top.prancingturtle.com/index.html

## Installation Instructions:
1. Import the `database.sql` from the database folder into a database named `rift_leaderboards`.
2. Configure the `mysql_connect_config.py` in the scripts folder to connect to your database (host, username, pass, db).
3. Start the `main.py` in the scripts folder. 

## Prerequisites...
1. nginx or apache server if not using AWS to upload.
2. python3.x series to run `python3 main.py`
3. MariaDB or mySQL.

## Database / File storage notes

* Database storage: ~5 to 10MB.
* First run duration: Ranges from 15 to 45 minutes (rate limited).
* Flat file usage: 
  * ./public: ~8MB (these are your rendered files)
  * ./scripts: ~200KB (these are static files)
  * ./template: ~512KB (edit these files
