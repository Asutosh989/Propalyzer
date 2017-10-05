# Propinator

Web app that helps investors evaluate investment property opportunities. The user inputs a US residential property address and the app uses Zillow's API to pull property details. The app presents the property details to the user for inspection and the ability to edit. With the details finalized, the app will crunch the data and return various financial metrics about the property including:
- Operating Income
- Operating Expenses
- Cash on Cash Return
- Debt Coverage Ratio
- Monthly Cash Flow

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

- Install Python 3.6.2
```
https://www.python.org/downloads/
```
- Obtain a Zillow account and Zillow API Key (ZWS-ID)
```
https://www.zillow.com/webservice/Registration.htm
```

- Create and configure virtualenv 
```
$ mkdir [directory name]
$ pip install virtualenv
$ virtualenv -p /Library/Frameworks/Python.framework/Versions/3.6/bin/python3.6 [directory name]
```
- Git dialed in! 
```
$ cd [directory name]
$ git init
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
$ git clone https://github.com/toms3t/Propinator.git
```
- Install packages from requirements.txt file

```
$ source bin/activate (run this from the directory you created to activate the virtual environment)
$ pip install -r requirements.txt
```
- Enter secret key in your /Users/[your username]/[directory name]/propinator_site/propinator_site/settings.py file
```
secret_key = '[enter new key here without the brackets - keep your key private]'
[save settings.py file]
```
- Enter your ZWSID into the '/Users/[username]/[directory name]/propinator_site/propinator_app/views.py' file
```
ZWSID = '[enter your key here without brackets]'
```

- Run local webserver and test the home page
```
$ cd /Users/[your username]/[directory name]/Propinator/propinator_site
$ python manage.py runserver
```
Test that the site homepage appears when you browse to http://127.0.0.1:8000/propinator

## Deployment

This web app uses a SQLite database which is installed by Django by default.

## Built With

* [Django](http://www.djangoproject.com) - The web framework used

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Authors

* **Tom Setliffe** - *Initial work* - [toms3t](https://github.com/toms3t)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thanks [PurpleTooth](https://github.com/PurpleTooth) for the readme template!
* Zillow for their outstanding API