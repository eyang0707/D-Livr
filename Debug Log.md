1.	I wanted to control the direction the car goes.
2.	The motors were going at the opposite directions.
3.	It was probably because of how I had my wires wired that was causing it to read different from one motor to the other. By changing the wires, it would be easier then changing the code.
4.	I can test it just by simply plugging in my code for it go forward, then I observe how it is. 
5.	It is now wired correctly so both motors go the way I want it to.
//----------------------------------------------------------------

1.	I wanted the car to keep going forward until it detects something in front of it within x distance. Then it will turn and then go towards another direction. 
2.	The car wouldn’t move.
3.	I will need to get the code to print, therefore I can test and set its distance limit for different commands. 
4.	I can test by seeing how my motors move based on where the placement my hand is from the distance sensor. 
5.	It now goes forward when it doesn’t detect anything within 40cm of the distance sensor, but it will still end up hitting the wall if it goes at it at a certain undetectable angle. 
6.	I will need a servo so it can turn repeatedly and detect a wider range of area. 
7.	I can test it by placing it on the floor and letting it run around the room.
8.	I couldn’t set up a servo at this point.
//----------------------------------------------------------------

1.	I want the motors to do a set of commands based on which sound detector picks up the clapping sound.
2.	The sound detectors was receiving the loud sound, but the code wasn’t doing any actions from my back sound detector.
3.	I will try to change my if statement in the loop to a “if x > y, else.” 
4.	I will clap and see how it responds.
5.	It does not work, in fact it is now even worse because it doesn’t move at all.
6.	I will now try to map the code, so it won’t detect the sounds from the motor.
7.	I will clap and see how it responds.
8.	It doesn’t seem to work with a digitalRead code.
9.	I will now try to change it so it reads through analog, through wiring and coding. 
10.	I will clap and see how it responds.
11.	It has trouble reading the different sound levels.
12.	I will now try to physically change the potentiometer, so it will be more sensitive.  
13.	I will clap and see how it responds.
14.	The level of sounds change, but it still can’t detect my clapping sounds. 
15.	I will now try to change everything back to as it first was and try to add delays to the code.
16.	I will clap and see how it responds.
17.	It will react, like the beginning, to the front sound detector, but not do the commands linked to the back sound detector. 
18.	Still can’t resolve this bug.
