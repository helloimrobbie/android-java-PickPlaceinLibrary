# android-java-PickPlaceinLibrary


##Library Place Pick Example


Hi, everyone.

Welcome my Git .

i'm Korean Student.

and Im not mobile Developer.

but im just made this example for Pratice.

i learn Java and Android Mobile :)


So Simple , and maybe bad Example.

just example :)

Thx, my Git.

Have a Nice Day.




## How to Pick my Place in the Library ?


Show this example.


## user language
java- Android Studio 3.2
Web Server and my Application communication by JSON.


## Before Using
Before Using, This Example First Setting php Server Environment.

need some PHP Page, and Request & Response API


## Server API Setting
* `ex) Show All Place State in my Virtual Library
in - `XXXXXX/ShowList.php`
Response JSON : 
```groovy
{"response":[
    {"No":"1","State":"X","UserID":""},
    {"No":"2","State":"O","UserID":""},
    ...
    {"No":"25","State":"X","UserID":""}
    ]}
```

* `ex) Login my Virtual Server for Pick Place in Virtual Library
in - XXXXXX/Login.php
Method POST.
ID=myID

Response JSON:
[Success]
    {"response":True,"userName":userName,"userID":userID}
    
[Failed]
    {"response":false}
    
    
* `ex) Pick Place Request.
in - XXXXXX/Pick.php
Method POST
ID=myID
Number= Want Pick Place Number. (ex) 2)

[Success]
	.. // Some Action Add userData in SQL Place Table
	{"response":True}
			
[Failed]
  {"response":false,"errorcode":1}
  
* `what is Errorcode ? 
 Errorcode 1 : The user who sent this request already has a reserved place
 Errorcode 2 : this request Place already has a reserved place by Another user's Request
 
 
* `ex) Pick Out Place Request
 in - XXXXXX/PickOut.php
 Method POST 
 ID = myID
 
 [Success]
     .. // Some Action Delete userData in SQL Place Table 
     {"response":True}
     
 [Failed]
     {"response":false,"errorcode":1}
     
 maybe errorcode 1 means , Dont Have reserved Place This user.
 
