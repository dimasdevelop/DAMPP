<!-- @format -->

# DAMPP

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

DAMP is the union of the [PHP](https://www.php.net/), [MYSQL](https://www.mysql.com/) and
[APACHE](https://www.apache.org/) [Docker](https://www.docker.com/) images connected and ready to
work as [XAMMP](https://www.apachefriends.org/es/index.html) or LAMPP.

-  Reading PHP files.
-  Mysql database.
-  PHPMyadmin environment.

### Installation

DAMPP requires [Docker](https://www.docker.com/) v19.03+ and
[Docker-Compose](https://docs.docker.com/compose/) v1.25+ to run.

Clone the repository on a pc.

```sh
$ git clone https://github.com/Jdlinux97/DAMPP.git
```

Position yourself in the containing folder.

```sh
$ cd DAMPP
```

Initialize DAMPP.

```sh
$ docker-compose up
```

### Setting

DAMPP settings are in the .env file.

| Variable         | Value        |
| ---------------- | ------------ |
| MYSQL_VERSION    | 5.7          |
| DB_NAME          | dbtest       |
| DB_USERNAME      | otherUser    |
| DB_ROOT_PASSWORD | rootpassword |
| DB_PASSWORD      | password     |

### Mysql connection

| Variable | Value        |
| -------- | ------------ |
| \$host   | mysql        |
| \$user   | root         |
| \$pass   | rootpassword |

```sh
    <?php
        $host = 'mysql';
        $user = 'root';
        $pass = 'rootpassword';
        $conn = new mysqli($host, $user, $pass);
        if ($conn->connect_error) {
            die("Connection failed: " . $conn->connect_error);
        } else {
            echo "Connected to MySQL successfully!";
        }
    ?>
```

### PHPMyadmin

To use **phpmyadmin** from **DAMPP** you must go to [localhost:8183](localhost:8183) once it is
initialized.

| Variable | Value        |
| -------- | ------------ |
| Server   | mysql        |
| User     | root         |
| Password | rootpassword |

### How to use

**Copy your folder with the PHP files and paste it in the html folder go to your browser and put
localhost / your_folder and enjoy the magic**

## License

MIT

**Free Software, Hell Yeah!**
