# upload.php
<!DOCTYPE html>
<html>
<head>
  <title>uploader</title>
</head>
<body style="background-color: yellow;">
<?php
$serverName = "localhost";
 $username = "root";
$password = "";
  $databaseName = "upload";
//connect to database
$con= new mysqli($serverName, $username, $password, $databaseName); 
//set the submit button 
if (isset($_POST['submit'])) {
$filecount = count($_FILES['file']['name']);
for ($i=0; $i<$filecount;$i++){
$filename = $_FILES['file']['name'][$i];
// insert details into 'img' table in database
$sql = "INSERT INTO img(title, img) VALUES ('$filename','$filename')";
$result   = mysqli_query($con, $sql);
if ($result) {
            echo "<div class='form'>
                  <h3>uploaded successfully.</h3><br/>
                  <p class='link'>Click here to continue <a href='login.php'>Login</a></p>
                  </div>";
        } else {
            echo "<div class='form'>
                  <h3>'ppRequired fields are missing.</h3><br/>
                  <p class='link'>Click here to <a href='registration.php'>registration</a> again.</p>
                  </div>";}


// move the uploaded files to a folder named img that was created
  move_uploaded_file($_FILES['file']['tmp_name'][$i], 'img/'.$filename);
    }

}

?>



  <form action="" method="POST" enctype="multipart/form-data">
    <input type="file" name="file[]" multiple><br>
    <input type="submit" name="submit" value="upload Images">

  </form>
</body>
</html>
