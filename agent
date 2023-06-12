




const int a = 8;  //For displaying segment "a"
const int b = 9;  //For displaying segment "b"
const int c = 4;  //For displaying segment "c"
const int d = 5;  //For displaying segment "d"
const int e = 6;  //For displaying segment "e"
const int f = 2;  //For displaying segment "f"
const int g = 3;  //For displaying segment "g"

//for unit2 7segment

const int a1 = A2;  //For displaying segment "a"
const int b1 = A3;  //For displaying segment "b"
const int c1 = 12;  //For displaying segment "c"
const int d1 = 13;  //For displaying segment "d"
const int e1 = 7;  //For displaying segment "e"
const int f1 = A0;  //For displaying segment "f"
const int g1 = A1;  //For displaying segment "g"

bool bPress = false;
const int Unit1buttonPin = 10;
const int Unit2buttonPin = 11;

// Variables will change:
int buttonPushUnit1Counter = 0;   // counter for the number of button presses
int buttonPushUnit2Counter = 0;

int Unit1buttonState = 0;         // current state of the button
int lastUnit1buttonState = 0;     // previous state of the button

int Unit2buttonState = 0;         // current state of the button
int lastUnit2buttonState = 0;     // previous state of the button

int an=0 ;

void setup() {

  
  // put your setup code here, to run once:
  pinMode(a, OUTPUT);  //A
  pinMode(b, OUTPUT);  //B
  pinMode(c, OUTPUT);  //C
  pinMode(d, OUTPUT);  //D
  pinMode(e, OUTPUT);  //E
  pinMode(f, OUTPUT);  //F
  pinMode(g, OUTPUT);  //G

  pinMode(a1, OUTPUT);  //A
  pinMode(b1, OUTPUT);  //B
  pinMode(c1, OUTPUT);  //C
  pinMode(d1, OUTPUT);  //D
  pinMode(e1, OUTPUT);  //E
  pinMode(f1, OUTPUT);  //F
  pinMode(g1, OUTPUT);  //G

  pinMode( Unit1buttonPin , INPUT_PULLUP );
  pinMode( Unit2buttonPin , INPUT_PULLUP );
  Serial.begin(9600);

  displayDigit1(buttonPushUnit1Counter);
  displayDigit2(buttonPushUnit2Counter);

}




void loop() {

   Unit1buttonState = digitalRead(Unit1buttonPin);
   Unit2buttonState = digitalRead(Unit2buttonPin);

   checkUnit1ButtonPress();
   checkUnit2ButtonPress();

  
   
 if( bPress ){
    bPress = false;
     turnOff();
     displayDigit1(buttonPushUnit1Counter);
     displayDigit2(buttonPushUnit2Counter);

     delay(50);
  }
 

   /*
  for(int i=0;i<10;i++)
 {
   displayDigit(i);
   delay(1000);
   turnOff();
 }
 */
}
// ----------------------------------------------------------------------------------------





void checkUnit1ButtonPress()
{
   // compare the IncbuttonState to its previous state
  if (Unit1buttonState != lastUnit1buttonState) {
    // if the state has changed, increment the counter
    if (Unit1buttonState == LOW) {
      // if the current state is HIGH then the button went from off to on:
      bPress = true;
      an++;
      if( an > 9) an =0 ;
       buttonPushUnit1Counter=an;
      Serial.println("on");

    } else {
      // if the current state is LOW then the button went from on to off:
      Serial.println("off");
    }
    // Delay a little bit to avoid bouncing
    delay(50);
  }
  // save the current state as the last state, for next time through the loop
  lastUnit1buttonState = Unit1buttonState;
 

}
// -----------------------------------------------------------------------------------------





void checkUnit2ButtonPress()
{
   // compare the IncbuttonState to its previous state
  if (Unit2buttonState != lastUnit2buttonState) {
    // if the state has changed, increment the counter
    if (Unit2buttonState == LOW) {
      // if the current state is HIGH then the button went from off to on:
      bPress = true;
     an++;
     buttonPushUnit2Counter=an;
      if( an > 9) an =0 ;
      Serial.println("on");

    } else {
      // if the current state is LOW then the button went from on to off:
      Serial.println("off");
    }
    // Delay a little bit to avoid bouncing
    delay(50);
  }
  // save the current state as the last state, for next time through the loop
  lastUnit2buttonState = Unit2buttonState;

}  

// ----------------------------------------------------------------------------------------------

void displayDigit1(int digit)
{
 //Conditions for displaying segment a
 if(digit!=1 && digit != 4)
 digitalWrite(a,LOW);


 //Conditions for displaying segment b
 if(digit != 5 && digit != 6)
 digitalWrite(b,LOW);

 //Conditions for displaying segment c
 if(digit !=2)
 digitalWrite(c,LOW);
 
 //Conditions for displaying segment d
 if(digit != 1 && digit !=4 && digit !=7)
 digitalWrite(d,LOW);
 
 //Conditions for displaying segment e 
 if(digit == 2 || digit ==6 || digit == 8 || digit==0)
 digitalWrite(e,LOW);

 //Conditions for displaying segment f
 if(digit != 1 && digit !=2 && digit!=3 && digit !=7)
 digitalWrite(f,LOW);
 
 if (digit!=0 && digit!=1 && digit !=7)
 digitalWrite(g,LOW);

}







void displayDigit2(int digit)
{
 //Conditions for displaying segment a
 if(digit!=1 && digit != 4)
 digitalWrite(a1,LOW);


 //Conditions for displaying segment b
 if(digit != 5 && digit != 6)
 digitalWrite(b1,LOW);

 //Conditions for displaying segment c
 if(digit !=2)
 digitalWrite(c1,LOW);
 
 //Conditions for displaying segment d
 if(digit != 1 && digit !=4 && digit !=7)
 digitalWrite(d1,LOW);
 
 //Conditions for displaying segment e 
 if(digit == 2 || digit ==6 || digit == 8 || digit==0)
 digitalWrite(e1,LOW);

 //Conditions for displaying segment f
 if(digit != 1 && digit !=2 && digit!=3 && digit !=7)
 digitalWrite(f1,LOW);
 
 if (digit!=0 && digit!=1 && digit !=7)
 digitalWrite(g1,LOW);

}






void turnOff()
{
  digitalWrite(a,HIGH);
  digitalWrite(b,HIGH);
  digitalWrite(c,HIGH);
  digitalWrite(d,HIGH);
  digitalWrite(e,HIGH);
  digitalWrite(f,HIGH);
  digitalWrite(g,HIGH);

  digitalWrite(a1,HIGH);
  digitalWrite(b1,HIGH);
  digitalWrite(c1,HIGH);
  digitalWrite(d1,HIGH);
  digitalWrite(e1,HIGH);
  digitalWrite(f1,HIGH);
  digitalWrite(g1,HIGH);
}
