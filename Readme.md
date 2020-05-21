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

### Social networks

[![alt text][1.1]][1] [![alt text][2.1]][2] [![alt text][3.1]][3] [![alt text][4.1]][4]

[1.1]: http://i.imgur.com/tXSoThF.png 'twitter icon with padding'
[2.1]: https://i.imgur.com/A21PSOX.png 'linkedin icon with padding'
[3.1]: https://i.imgur.com/FTfZyuk.png 'Instagram  icon with padding'
[4.1]: http://i.imgur.com/0o48UoR.png 'github icon with padding'
[1]: https://twitter.com/Jdlinux97
[2]: https://www.linkedin.com/in/dimas-gonzalez/
[3]: https://www.instagram.com/jdlinux/?hl=en
[4]: https://github.com/Jdlinux97

## License

MIT

**Free Software, Hell Yeah!**
