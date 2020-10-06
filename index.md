## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Saviourise/new-project/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Saviourise/new-project/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
<!DOCTYPE html>

<html>

    <head>

        <meta charset="utf-8">

        <!-- Responsive -->

       <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- CSS -->

        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">

        <!-- jQuery -->

        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>

        <!-- JavaScript -->

        <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

        <link href="https://fonts.googleapis.com/css?family=Oswald|Raleway&display=swap" rel="stylesheet">

        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

        <link rel='stylesheet' href='https://use.fontawesome.com/releases/v5.5.0/css/all.css' integrity='sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU' crossorigin='anonymous'>

        

        <style>

            body {

                font-family:Raleway;

            }

            

            .container [class^=col-] {

                padding-top: 10px;

                padding-bottom: 10px;

                background-color: #eee;

                background-color: rgba(86,61,124,.15);

                border: 1px solid #ddd;

                border: 1px solid rgba(86,61,124,.2);

            }

            

            .row {

                margin:5px;

            }

            

            input {

                outline:none;

            		font-weight:bolder;

            }

            

            .but {

                outline:none;

                box-shadow: inset 0px 0px 5px rgba(86,61,124,.2), inset -1px -1px 5px rgba(86,61,124,.2);

            				

            }

            .but:hover {

            		background-color:green;

            }

            

            form {

            		

            }

            

            #mmm {

            		height:685px;

            		overflow:scroll;

            		background-color: #eee;

                background-color: rgba(86,61,124,.15);

                border: 1px solid #ddd;

                border: 1px solid rgba(86,61,124,.2);

                margin-left:20px;

                width:370px;

                margin-top:10px;

            }

            

            #head {

            		height:40px;

            		overflow:scroll;

            		background-color: #eee;

                background-color: rgba(86,61,124,.15);

                border: 1px solid #ddd;

                border: 1px solid rgba(86,61,124,.2);

                margin-left:20px;

                width:370px;

                margin-top:10px;

                padding-left: 7px;

                color:red;

                padding-top: 7px;

                font-size:20px;

                font-weight: bolder;

            }

            p {

            		list-style-type:none;

            		padding-top: 7px;

                padding-bottom: 7px;

                margin-top:0px;

            }

        </style>

        

        

        

        

       <script src="https://www.gstatic.com/firebasejs/6.2.4/firebase-app.js"></script>

        <script src="https://www.gstatic.com/firebasejs/6.2.4/firebase-database.js"></script>

<script>

  // Your web app's Firebase configuration

  var firebaseConfig = {

    apiKey: "AIzaSyBEVY6VUuKOB96KwUmhtB7QgZCHTbBHui8",

    authDomain: "chatapp-c401d.firebaseapp.com",

    databaseURL: "https://chatapp-c401d.firebaseio.com",

    projectId: "chatapp-c401d",

    storageBucket: "chatapp-c401d.appspot.com",

    messagingSenderId: "38639924929",

    appId: "1:38639924929:web:429f633582e0bd45adc640"

  };

  // Initialize Firebase

  firebase.initializeApp(firebaseConfig);

  

  var myName = prompt("Choose Username")

  

  function sendMessage() {

  		var message = document.getElementById("mess").value;

  		

  		firebase.database().ref("messages").push().set({

  				"sender": myName,

  				"message": message

  		});

  		

  		

  		return false;

      

  }

  firebase.database().ref("messages").on("child_added", function(snapshot){

  		var html = "";

  		html += "<p id='message-" + snapshot.key + "'>";

  		

  		    html += snapshot.val().sender + ": " + snapshot.val().message + "  ";

  		    

  		

  		html += "</p>"

  		

  		document.getElementById("messages").innerHTML += html;

  

  });

 

  

</script>

        

        

        

        

        

        

    </head>

    <body>

    <div id="head">

        ChatRoom

    </div>

    <div class="container" id="mmm">

        <div id="messages"></div>

        

    </div>

    <div class="container">

        

        <div class="row">

            

            <form onsubmit="return sendMessage()">

                <input class="col-xs-10" type="text" id="mess" placeholder="Enter Message" id="">

                <button type="submit" class="col-xs-2 but"><i class="fa fa-send"></i></button>

            </form>

            

        </div>

    </div>

    

    </body>

</html>
