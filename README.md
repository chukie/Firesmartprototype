# Firesmartprototype
Fire smart is a system compromised of an app,  fire sensing device and a server that work hand in hand to solve a problem . The goal is to sense fire and it alerts the user when fire is sensed . The user has the ability to stop the alarm through the app(if it’s a false fire , for example smoke from cooking ) . The user has ability to instruct the app to call 911 to the house (incase the user isn’t home ) . If the user does not respond after a time limit set by the user . The alarm system automatically calls 911 .

The prototype of the server can be found at : https://github.com/chukie/firesmartdemo

The prototype of the microcontroller code can be found at : https://github.com/chukie/firesmartarduinocode

The prototype of the App (android platform ) can be found at : https://github.com/chukie/firesmartandroidapp


## Brief architecture explanation :
Microcontroller (Think speak) runs a loop that senses fire when sensed it triggers the central server and an alarm object is created in a json File storage base (stored on aws buckets) . The android app repeatedly looks for a change in database to see if any alarm object has been created when created , the app notifies user and if after a certain time there is no change in alarm status the microcontroller calls the central server again to call 911 . 


## This is an incomplete but functioning prototype of the system 
 Features implemented
* call 911
* Text notification
* microcontroller sense fire 
* Interaction between server , app and Microcontroller
* Alarm status displaying on app

 Features to add
* Boot android app service when phone is turned on
* Detect varying level and angles of smoke (might require advanced designed sensors).
* Use App notification instead of text notification 


