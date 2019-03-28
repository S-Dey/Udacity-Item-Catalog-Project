# Item Catalog Project
An Udacity Full Stack Web Developer II Nanodegree project developed by Subhadeep Dey.

## About
This application provides a list of items within a variety of categories as well as provide a user registration and authentication system. Registered users will have the ability to post, edit, and delete their own items.

### Features
- Proper authentication and authorisation check.
- Full CRUD support using SQLAlchemy and Flask.
- JSON endpoints.
- Implements oAuth using Google Sign-in API.

### Project Structure
```
.
├── app.py
├── client_secrets.json
├── database_setup.py
├── fake_db_populator.py
├── itemcatalog.db
├── LICENSE
├── README.md
├── static
│   └── style.css
└── templates
    ├── delete_category.html
    ├── delete.html
    ├── edit_category.html
    ├── index.html
    ├── items.html
    ├── layout.html
    ├── login.html
    ├── new-category.html
    ├── new-item-2.html
    ├── new-item.html
    ├── update-item.html
    └── view-item.html
```

## Steps to run this project

1. Download and install [Vagrant](https://www.vagrantup.com/downloads.html).

2. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

3. Clone or download the Vagrant VM configuration file from [here](https://github.com/udacity/fullstack-nanodegree-vm).

4. Open the above directory and navigate to the `vagrant/` sub-directory.

5. Open terminal, and type

   ```bash
   vagrant up
   ```

   This will cause Vagrant to download the Ubuntu operating system and install it. This may take quite a while depending on how fast your Internet connection is.

6. After the above command succeeds, connect to the newly created VM:

   ```bash
   vagrant ssh
   ```

8. Type `cd /vagrant/` to navigate to the shared repository.

9. Download or clone this repository, and navigate to it.

11. Install or upgrade Flask:
    ```bash
    sudo python3 -m pip install --upgrade flask
    ```
12. Set up the database:
    ```bash
    python3 database_setup.py
    ```
13. Insert dummy values. **If you don't run this, the application might not run.**
    ```bash
    python3 fake_db_populator.py
    ```
14. Run this application:
    ```bash
    python3 app.py
    ```
15. Open `http://localhost:5000/` in your favourite Web browser, and enjoy.

## Debugging
In case the app doesn't run, make sure to confirm the following points:
- You have run `python3 fake_db_populator.py` before running the application. This is an essential step.
- The latest version of Flask is installed.
- Python 3.6 is installed. In the vagrant machine, you may find Python 3.5 installed by default. To install Python 3.6, follow [this answer](https://askubuntu.com/a/865569/571299). To invoke Python 3.6, type `python3.6` instead of `python3`.

## Known Issue
This app might show an empty username if you sign in with a custom-domain-based Google account (Corporate accounts). For instance, if you use a Google account `johndoe@company.com`, this app might show an empty username.

## Help and Support
In case you run into any trouble, create an issue on GitHub. I will make sure to look into it as soon as possible.
