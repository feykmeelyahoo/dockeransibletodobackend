Do the instructions given below link

https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-ubuntu-16-04

sudo apt-get update
sudo apt-get -y upgrade

python3 -V

sudo apt-get install -y python3-pip
sudo apt-get install build-essential libssl-dev libffi-dev python-dev
sudo apt-get install -y python3-venv

pip3 install django
django-admin startproject todobackend

# pyvenv depreciated 3.6dan itibaren o yüzden aşağıdaki gibi yap
# Ikinci venv virtual envin ismi
python3 -m venv venv

. venv/bin/activate

# Activationdan sonra artık Python3 pip çalışıyor defaulttan

pip install --upgrade pip
pip install django
pip install django-cors-headers
pip install djangorestframework

python manage.py startapp todo

# update settings.py file 
# create models under todo

# create schema
python manage.py makemigrations todo

