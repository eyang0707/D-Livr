int motorRightForward   = 10; //for motors
int motorRightReverse   = 11;
int motorLeftForward    = 12;
int motorLeftReverse    = 13;

float soundDetectedPinback = 5; //for sound
float soundDetectedPinfront = 6;
int soundDetectedVal1 = HIGH; // This is where we record our Sound Measurement
int soundDetectedVal2 = HIGH;
boolean bAlarm = false;
unsigned long lastSoundDetectTime; // Record the time that we measured a sound
int soundAlarmTime = 200; // Number of milli seconds to keep the sound alarm high

#include <NewPing.h> //for distance
#define TRIGGER_PIN  1  // Arduino pin tied to trigger pin on the ultrasonic sensor.
#define ECHO_PIN     2  // Arduino pin tied to echo pin on the ultrasonic sensor.
#define MAX_DISTANCE 200 // Maximum distance we want to ping for (in centimeters). Maximum sensor distance is rated at 400-500cm.
NewPing sonar(TRIGGER_PIN, ECHO_PIN, MAX_DISTANCE); // NewPing setup of pins and maximum distance.

//------------------------------------------------------------

void setup() { //setup for motors
  Serial.begin(9600);

  pinMode (soundDetectedPinfront, INPUT) ; // input from the Sound Detection Module
  pinMode (soundDetectedPinback, INPUT) ; // input from the Sound Detection Module


  pinMode(motorRightForward, OUTPUT);
  pinMode(motorRightReverse, OUTPUT);
  pinMode(motorLeftForward, OUTPUT);
  pinMode(motorLeftReverse, OUTPUT);
}

void forward() {
  digitalWrite(motorRightForward, HIGH);
  digitalWrite(motorRightReverse, LOW);
  digitalWrite(motorLeftForward, HIGH);
  digitalWrite(motorLeftReverse, LOW);
}

void halt() {
  digitalWrite(motorRightForward, LOW);
  digitalWrite(motorRightReverse, LOW);
  digitalWrite(motorLeftForward, LOW);
  digitalWrite(motorLeftReverse, LOW);
}

void forwardleft() {
  digitalWrite(motorRightForward, HIGH);
  digitalWrite(motorRightReverse, LOW);
  digitalWrite(motorLeftForward, LOW);
  digitalWrite(motorLeftReverse, LOW);
}

void forwardright() {
  digitalWrite(motorRightForward, LOW);
  digitalWrite(motorRightReverse, LOW);
  digitalWrite(motorLeftForward, HIGH);
  digitalWrite(motorLeftReverse, LOW);
}

void backleft() {
  digitalWrite(motorRightForward, LOW);
  digitalWrite(motorRightReverse, HIGH);
  digitalWrite(motorLeftForward, LOW);
  digitalWrite(motorLeftReverse, LOW);
}

void backright() {
  digitalWrite(motorRightForward, LOW);
  digitalWrite(motorRightReverse, LOW);
  digitalWrite(motorLeftForward, LOW);
  digitalWrite(motorLeftReverse, HIGH);
}

//------------------------------------------------------------

unsigned long lastPing = 0;


void loop ()//for sound

{
  soundDetectedVal1 = digitalRead (soundDetectedPinfront) ; // read the sound alarm time
  if (soundDetectedVal1 == LOW) // If we hear a sound

    soundDetectedVal2 = digitalRead (soundDetectedPinback) ; // read the sound alarm time
  if (soundDetectedVal2 == LOW) // If we hear a sound

    if (soundDetectedPinback < soundDetectedPinfront) {
      delay (15);
      forward();
    }

    else {
      delay (15);
      halt();
      delay(15);
      forwardleft();
      delay(15);
      forward();
    }



  {
    lastSoundDetectTime = millis(); // record the time of the sound alarm
    // The following is so you don't scroll on the output screen
    if (!bAlarm) {
      Serial.println("LOUD, LOUD");
      bAlarm = true;
    }

    else
    {
      if ( (millis() - lastSoundDetectTime) > soundAlarmTime  &&  bAlarm) {
        Serial.println("quiet");
        bAlarm = false;
      }
    }


    // delay(50);                     // Wait 50ms between pings (about 20 pings/sec). 29ms should be the shortest delay between pings.
    if (millis() - lastPing > 20) {
      Serial.print("Ping: ");
      Serial.print(sonar.ping_cm());
      Serial.println("cm");
      lastPing = millis();
    }


    long duration, distance;
    digitalWrite(TRIGGER_PIN, LOW);
    delayMicroseconds(2); //
    digitalWrite(TRIGGER_PIN, HIGH);

    delayMicroseconds(10); //
    digitalWrite(TRIGGER_PIN, LOW);
    duration = pulseIn(ECHO_PIN, HIGH);
    distance = (duration / 2) / 29.1; // convert the distance to centimeters.
    if (distance < 40) {
      Serial.println ("Close Obstacle detected!" );
      Serial.println ("Obstacle Details:");
      Serial.print ("Distance From Robot is " );
      Serial.print ( distance);
      Serial.print ( " CM!");// print out the distance in centimeters.

      Serial.println (" The obstacle is declared a threat due to close distance. ");
      Serial.println (" Turning !");
      delay (15);
      forwardleft();
    }
    else {
      Serial.println ("No obstacle detected. going forward");
      delay (15);
      forward();
    }
  }
}

