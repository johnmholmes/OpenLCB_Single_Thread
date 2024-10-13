# Example Applications
The provided examples will give some ideas of how to accomplish sample projects.  They can form the basis of, or  be adapted to, a new Application, or just used for inspiration.  <br>

- **AVR-8Servo**<br>
    Implements an eight servo node. This example uses the Adafruit_PWMServoDriver.h and demonstrates how one might implement a node using an external library.      

- **OlcbBlankNode**<br>
    The example shows the minimal node code without any additional logic.  

- **OlcbBasicNode**<br>
    Implements a simple node which exercises most of the protocols.  It has **two inputs** and **two outputs**.  Each input has two Producer-eventIDs and each output has two Consumer-eventIDs, so **8 eventIDs in total**.  This Application makes use of the ButtonLed library to control **two buttons** and **two LEDs**.  In addition, it implements the BG (Blue-Gold) protocol to allow the **teaching** of eventIDs between this node and others.  
        The example connects the BUILTIN_LED to the first output, so triggering the two associated events will turn that LED on and off.  

- **Olcb328_8InputNode**<br>
    Implements an eight input node. Similarly to the above, example. 
        
- **Olcb328_8OutputNode**<br>
    Implements an eight output node. Similarly to the above, example. 

- **OlcbIoNode**<br>
    Implements the equivalent function to the base code in the Railstars Io and associated DevKit.  It uses this frame work and implements 8 inputs and 8 outputs, with two eventids per i/o.  

- **RailStarsIo-8Out-38InOut-16Servo**<br>
    Creates a node using the Railstars Io board (DevPack board) which implements 8 outputs (consumers), 8 inputs (producers), 24 BOD inputs (producers), and 16 servo outputs (consumers).  The latter uses a PCA8695 PWM chip (see: https://www.adafruit.com/product/815).  It shows how to write a different **pceCallback()**.  It also uses **userConfigWrite()** to allow real-time updating of a servo positions from a **UI Tool**, such as **JMRI** or **Model Railroad System**. 
    
- **Tiva123-8Out-8In-16BoD-16Servo**<br>
    Creates a node using the Tiva123 Launchpad board from TI (see: http://www.ti.com/tool/EK-TM4C123GXL) which implements 8 outputs (consumers), 8 inputs (producers), 16 BOD inputs (producers), and 16 servo outputs (consumers).  The latter uses a PCA8695 PWM chip (see: https://www.adafruit.com/product/815).  One will want to uncomment the INITIALIZE_TO_NODE_ADDRESS and RESET_TO_FACTORY_DEFAULTS the first time to initialize the EEPROM, and then they should be recommented to minimize EEPROM rewrites.  
    
- **OlcbBlankNode**<br>
    This is a blank node which can be used to develop a new node.

## Servo Examples

See the Servos directory
   