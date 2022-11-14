Info:
 - Domain: israelmiller.tech
 - A Record:
    - Name: www.israelmiller.tech
    - Value: 35.225.138.255
    - TTL: 28800
 - Cloud Vendor: GCP


Instructions to set up VM to host site:
 - Create VM instance in GCP or Azure that allows http and https traffic
 - Next, Install the following packages and update VM: 
    - To update VM: `sudo apt-get update`
    - To install pip3: `sudo apt-get install python3-pip`
    - To install Flask `pip3 install Flask`
    - To install flask-mysqlalchemy `pip3 install flask_sqlalchemy`
    - To install dotenv `pip3 install python-dotenv`
    - To install MySQL Client: `sudo apt-get install mysql-client`
 - Next, clone the Github repo that contains the flask application: `git clone (Repo URL)`
    - Next, create a .env file in the root directory of the repo and add the following variables:
        - `MYSQL_USER=(username)`
        - `MYSQL_PASSWORD=(password)`
        - `MYSQL_HOST=(host)`
        - `MYSQL_DATABASE=(database)`
 - Next, run the flask application: `sudo python3 app.py`
    - or as a background process with logging: `sudo nohup python3 app.py > /dev/null 2>&1 &`

