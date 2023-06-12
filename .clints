#include <LiquidCrystal.h>



LiquidCrystal lcd(7,8,9,10,11,12); 





// this constant won't change:

const int  Unit1_buttonPin   = 2;    // the pin that the pushbutton is attached to

const int  Unit2_buttonPin = 3;



// Variables will change:

int buttonUnit1Counter = 0;   // counter for the number of button presses

int buttonUnit2Counter = 0;

int Unit1_buttonState = 0;         // current state of the up button

int Unit1_lastButtonState = 0;     // previous state of the up button



int Unit2_buttonState = 0;         // current state of the up button

int Unit2_lastButtonState = 0;     // previous state of the up button

bool bPress = false;



void setup()

{


  Serial.begin(9600);

  pinMode( Unit1_buttonPin , INPUT_PULLUP);

  pinMode( Unit2_buttonPin , INPUT_PULLUP);



  lcd.begin(16,2);                     
 

  // Print a message to the LCD.

  lcd.clear();
  lcd.setCursor(0,0);
  lcd.print("Please Select");
  lcd.setCursor(0,1);
  lcd.print("your Unit:");
    

 

}





void loop()

{
   checkUp();

   checkDown();

}



void checkUp()//*************************************************************

{

 Unit1_buttonState = digitalRead(Unit1_buttonPin);



  // compare the buttonState to its previous state

  if (Unit1_buttonState != Unit1_lastButtonState) {

    // if the state has changed, increment the counter

    if (Unit1_buttonState == LOW) {

        bPress = true;

      // if the current state is HIGH then the button went from off to on:

      buttonUnit1Counter++;

      Serial.println("on");

      Serial.print("The turn number in Unit1 is: ");

      Serial.println(buttonUnit1Counter);

      //-------------------
      
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("You select unit1");
      lcd.setCursor(0,1);
      lcd.print("Your turn:");
      lcd.setCursor(10,1);
      lcd.print(buttonUnit1Counter);

      delay(3000);

    
      
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("Thanks for your");
      lcd.setCursor(4,1);
      lcd.print("PATIENCE");

      delay(1500);

      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("Please Select");
      lcd.setCursor(0,1);
      lcd.print("your Unit:");
      
    } else {

      // if the current state is LOW then the button went from on to off:

      Serial.println("off");

    }

    // Delay a little bit to avoid bouncing

    delay(50);

  }

  // save the current state as the last state, for next time through the loop

  Unit1_lastButtonState = Unit1_buttonState;

}

void checkDown()//*******************************************************************

{

  Unit2_buttonState = digitalRead(Unit2_buttonPin);



  // compare the buttonState to its previous state

  if (Unit2_buttonState != Unit2_lastButtonState) {

    // if the state has changed, increment the counter

    if (Unit2_buttonState == LOW) {

        bPress = true;

      // if the current state is HIGH then the button went from off to on:

      buttonUnit2Counter++;

     

      Serial.println("on");

      Serial.print("The turn number in Unit2 is:");

      Serial.println(buttonUnit2Counter);

      //-------------------------------------------------
      
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("You select unit2");
      lcd.setCursor(0,1);
      lcd.print("Your turn:");
      lcd.setCursor(13,1);
      lcd.print(buttonUnit2Counter);
      
      delay(3000);
      
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("Thanks for your");
      lcd.setCursor(4,1);
      lcd.print("PATIENCE");

      delay(1500);

      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("Please Select");
      lcd.setCursor(0,1);
      lcd.print("your Unit:");
      

    } else {

      // if the current state is LOW then the button went from on to off:

      Serial.println("off");

    }

    // Delay a little bit to avoid bouncing

    delay(50);

  }

  // save the current state as the last state, for next time through the loop

 Unit2_lastButtonState = Unit2_buttonState;

}
