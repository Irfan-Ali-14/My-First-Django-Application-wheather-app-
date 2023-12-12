To Deploy the app on Ec2 instance follow the below instructions.

Update the System

sudo apt-get update

To get this repository, run the following command inside your git enabled terminal
git clone https://github.com/yeshwanthlm/django-on-ec2.git

Download django usig pip

sudo apt install python3-pip -y
pip install django

Once you have downloaded django, go to the cloned repo directory and run the following command

python3 manage.py makemigrations
This will create all the migrations files required to run this App.

Now, to apply this migrations run the following command

python3 manage.py migrate
We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user

python3 manage.py createsuperuser
We just need to start the server now and then we can start using our simple App. Start the server by following command

python3 manage.py runserver

Note: DO not foget to allow port 8000 (default port of django) on security group of EC2 instance. Secondly, change the host to 0.0.0.0:8000 initially it will run the app on local(127.0.0.1:8000) of production environment.
