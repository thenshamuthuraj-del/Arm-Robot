#define BLYNK_TEMPLATE_ID "********"
#define BLYNK_DEVICE_NAME "********"
#define BLYNK_AUTH_TOKEN "********"
#define BLYNK_PRINT Serial

#include <ESP8266WiFi.h>
#include <BlynkSimpleEsp8266.h>
#include<Servo.h>

Servo servo1, servo2, servo3, servo4, servo5;

char auth[] = BLYNK_AUTH_TOKEN;
char ssid[] = "********";
char pass[] = "********";

BLYNK_WRITE(V0){     
    int value = param.asInt(); // Get value as integer  
    servo1.write(value);
}
BLYNK_WRITE(V1){     
    int value = param.asInt(); // Get value as integer  
    servo2.write(value);
}
BLYNK_WRITE(V2){     
    int value = param.asInt(); // Get value as integer  
    servo3.write(value);
}
BLYNK_WRITE(V3){     
    int value = param.asInt(); // Get value as integer  
    servo4.write(value);
}
BLYNK_WRITE(V4){     
    int value = param.asInt(); // Get value as integer  
    servo5.write(value);
}

void setup(){
    Serial.begin(9600);
    servo1.attach(D2);
    servo2.attach(D3);
    servo3.attach(D5);
    servo4.attach(D6);
    servo5.attach(D7);
    Blynk.begin(auth, ssid, pass);
    //Splash screen delay  
    delay(2000); 
}

void loop() {  
    Blynk.run();
}
