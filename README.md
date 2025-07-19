# Photo Album Website 

Group Project CSCI 435: Database Management
Feb 2019

### Features
- lets user make photo albums
- User needs provide username, password, email.
- Can upload photos and put them into photo album.
- Database to store user information, photo albums and photos

### Tech Stack (XAMP:  X-operating system, Apache, Mysql, Php)
- Apache HTTP Server
- Database: MariaDB MySQL
- PHP Interpreters for scripts

#### Queries in PHP
```php
Signup.php: $sql="INSERT INTO account (username, email, password) VALUES ('$username', '$email', '$password’)”;

Login.php: $result = mysqli_query($connect, "select username,password from account where username='$username' and password='$password’”);

Index.php: $result = mysqli_query($connect, "select username,password from account where username='$username' and password='$password'");
```

##### ALBUMS PHP Functions 
```php
- createAlbum(): $sql = "INSERT INTO album (username, name) VALUES ('" . $_SESSION['user_id'] . "', '" . $_GET['name'] . "')";
- addPhoto(): $sql = "INSERT INTO photo (album_key, path2photo) VALUES ('" . $_GET['album_key'] . "', '" . $_POST['data'] . "')";
- deletePhoto(): $sql = "DELETE FROM photos WHERE id = " . $_GET['id’];
- getPhoto(): $sql = "SELECT id, path2photo FROM photo WHERE album_key = '" . $_GET['album_key'] . ”’”;
- getAlbums(): $sql = "SELECT * FROM album where username = '" . $_SESSION['user_id'] . "'";


```


Contributors:
- Riyadh
- Deion
- Topgyal
- Wei

