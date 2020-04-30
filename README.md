'''
#Tinkercad-Projects

Circuit of Light Row:

  Link: https://www.tinkercad.com/things/l3PPbVqE0S8-copy-of-light-row/editel?sharecode=km11Dwv22Xz37xPKimUEgKdv9WWOdHnVjNqJUSpsDSE
    
  '''
  
  int leds[]={5,6,7,8,9,10,11};
int n=0;
int time=30;

void setup() { 
  for (n=0;n<7;n++) {
  pinMode(leds[n],OUTPUT);
 }
}

void loop() {
  for (n=0;n<7;n++) {
    digitalWrite (leds[n],HIGH);
    delay(time);
    digitalWrite(leds[n+1],HIGH);
    delay(time);
    digitalWrite (leds[n],LOW);
    delay(time*2);
 }
  
  for (n=6;n>=0;n--) {
    digitalWrite (leds[n],HIGH);
    delay(time);
    digitalWrite(leds[n-1],HIGH);
    delay(time);
    digitalWrite (leds[n],LOW);
    delay(time*2);
 }
}
