# D-Livr
Programming and Electronics Final Project

There are two people, one of them is called Bob and other is called Joe. They are best buddies who get along very well because they are both very lazy. They also happen to work at the same place. Unfortunately for them, their tables in the office are placed at opposite ends of the room. Sometimes they would like to send office papers, share a snack, or borrow each other’s stationary. But then that means one of them will have to walk all the way to other side of the room and back to their table! That is a lot of walking to both Bob and Joe. But what if they had a car that would deliver their items for them? If Joe wanted a lollipop from Bob, Joe can easily text Bob for a piece of lollipop. Then Bob will put a lollipop D-Livr and all Joe has to do now is clap his hands. By the sound of Joe’s clap, D-Livr will start racing towards the direction of Joe’s clapping sound while blinking lights to caution others it is coming through.

D-Livr would be an automated car that will start driving towards the direction of a clapping sound. It will start going towards the direction until it senses there is something in front of it, then it will stop going forward in order to avoid bumping into it. It will be a fun and easy way for people to deliver things inside a small space. The input would be the sound of a clapping while the output will be the driving towards the clapping sound while blinking its lights.

The hardest part was trying to get the code to work. Getting the distance sensor to work with the motors wasn’t as hard compared to trying to get the sound sensors to work with the motors. It might have been because of how close both sound sensors were to each other, and definitely the code. It is hard to get it to try and figure out which sensor of the two is picking up a stronger sound. Also the code overall seems to have trouble looping the sound sensors commands and the distance sensors commands together. Overall, I don't think trying to get the robot to follow the sound of clapping was a very good idea in terms of physics. In a room, the sound detectors will pretty muh detect the same levels. Something more ideal would be something like a light sensor.

Photos:

[process photo](https://scontent.fsjc1-1.fna.fbcdn.net/hphotos-xfl1/v/t34.0-12/11998753_10154095950694026_1430846473_n.jpg?oh=82382794472e27ad868be674c6f3fb24&oe=566AB627)

[final product](https://scontent.fsjc1-1.fna.fbcdn.net/hphotos-xta1/v/t34.0-12/12351168_10154095950699026_1438553303_n.jpg?oh=1ae3e5554d7c3fa24d5f135f63f7a046&oe=566AB4E3)


References:

[workshopweekend](http://workshopweekend.net/arduino/projects/remote_control_cardboard)

[henrysbench](http://henrysbench.capnfatz.com/henrys-bench/arduino-sound-detection-sensor-tutorial-and-user-manual/)

[instructables](http://www.instructables.com/id/Simple-Arduino-and-HC-SR04-Example/?ALLSTEPS)

[letsmakerobots](http://letsmakerobots.com/node/40502)
