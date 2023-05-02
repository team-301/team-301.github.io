## **Bill of Materials** 

| **Bill of Materials Team 301**  |                   |                         |                          |                          |                           |                                   |                         |                                                                                                                                                                                                                                                                                                                                       |                                                                                                                       |              |                      |             |                                     |
|---------------------------------|-------------------|-------------------------|--------------------------|--------------------------|---------------------------|-----------------------------------|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|--------------|----------------------|-------------|-------------------------------------|
| **Part Name/Description**       | **Unit Quantity** | **Unit Prototype Cost** | **Total Prototype Cost** | **Unit Production Cost** | **Total Production Cost** | **Manufacturer**                  | **Manufacturer Part #** | **Vendor Link**                                                                                                                                                                                                                                                                                                                       | **Datasheet Link**                                                                                                    | **Supplier** | **Supplier Part #**  | **Surplus** | **Schematic Reference Designators** |
| FAN8100N/Motor driver           | 8                 | $0.00                   | $0.00                    | $0.73                    | $5.84                     | Fairchild Semiconductor           | FAN8100N                | [<u>Link</u>](https://www.digikey.com/en/products/detail/rochester-electronics-llc/FAN8100N/11558200)                                                                                                                                                                                                                                 | [<u>Link</u>](https://rocelec.widen.net/view/pdf/1pizbjqffm/FAIRS23777-1.pdf?t.download=true&u=5oefqw)                | Digikey      | 2156-FAN8100N-FS-ND  | 0           | U6                                  |
| Motor                           | 4                 | $0.00                   | $0.00                    | $6.89                    | $27.56                    | JYC International Trade Co., Ltd. | DC3-12V 00933           | [<u>Link</u>](https://www.amazon.com/AUTOTOOLHOME-Torque-Traxxas-Wheels-Electric/dp/B01M58POHF/ref=asc_df_B01M58POHF/?tag=hyprod-20&linkCode=df0&hvadid=309768150198&hvpos=&hvnetw=g&hvrand=9707710327954434611&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9030039&hvtargid=pla-526501699343&psc=1&region_id=972485) | No datasheet                                                                                                          | Amazon       | B01M58POHF           | 0           | TP24-25                             |
| Temp Sensor TC74                | 6                 |                         | $0.00                    | $1.90                    | $11.40                    | Microchip                         | SOT-23                  | [<u>Link</u>](https://www.microchip.com/en-us/product/TC74)                                                                                                                                                                                                                                                                           | [<u>Link</u>](https://ww1.microchip.com/downloads/aemDocuments/documents/APID/ProductDocuments/DataSheets/21462D.pdf) | Microchip    | TC74                 | 0           | U5                                  |
| Micro Controller                | 3                 |                         | $0.00                    | $1.85                    | $5.55                     | Microchip Technology              | PIC16LF15376            | [<u>Link</u>](https://www.digikey.com/en/products/detail/microchip-technology/PIC16LF15376-I-PT/7164824)                                                                                                                                                                                                                              | [<u>Link</u>](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC16_L_F15313_23_Data_Sheet_40001897C.pdf)            | Digikey      | PIC16LF15376-I/PT-ND | 0           | U11                                 |
| Switching regulator AP63203WU-7 | 5                 | $0.00                   | $0.00                    | $1.16                    | $5.80                     | Diodes Incorporated               | AP63203WU-7             | [<u>link</u>](http://digikey.com/en/products/detail/diodes-incorporated/AP63203WU-7/9858426)                                                                                                                                                                                                                                          | [<u>link</u>](https://www.diodes.com/assets/Datasheets/AP63200-AP63201-AP63203-AP63205.pdf)                           | Digikey      | AP63203WU-7DICT-ND   | 0           | U2                                  |

## **MQTT table** 

| EGR314/Team301/Temperature sensor |                                           |     |     |     |     |     |
|-----------------------------------|-------------------------------------------|-----|-----|-----|-----|-----|
| Entities Publishing               | MQTT                                      |     |     |     |     |     |
| Entities Subscribing              | Microcontroller                           |     |     |     |     |     |
| Topic Value Separator             | NA/only sending one value                 |     |     |     |     |     |
| Value 1                           |                                           |     |     |     |     |     |
| Value Name:                       | Temperature                               |     |     |     |     |     |
| Value Description:                | Temperature reading value                 |     |     |     |     |     |
| Unit System:                      | Celsius                                   |     |     |     |     |     |
| Value Minimum:                    | Zero - 0                                  |     |     |     |     |     |
| Value Maximum:                    | 1024                                      |     |     |     |     |     |
| Value Type:                       | Float                                     |     |     |     |     |     |
| Value Format String:              | printf ("temp = %uF \\n", readtemp,temp); |     |     |     |     |     |
| Value Unique Identifier:          | C                                         |     |     |     |     |     |
| Full Topic Example:               | printf ("temp = %uF \\n", readtemp,temp); |     |     |     |     |     |

## 

## **MPLAB Project Code**

/\*\*

Generated Main Source File

Company:

Microchip Technology Inc.

File Name:

main.c

Summary:

This is the main file generated using PIC10 / PIC12 / PIC16 / PIC18 MCUs

Description:

This header file provides implementations for driver APIs for all
modules selected in the GUI.

Generation Information :

Product Revision : PIC10 / PIC12 / PIC16 / PIC18 MCUs - 1.81.8

Device : PIC16LF15376

Driver Version : 2.00

\*/

/\*

\(c\) 2018 Microchip Technology Inc. and its subsidiaries.

Subject to your compliance with these terms, you may use Microchip
software and any

derivatives exclusively with Microchip products. It is your
responsibility to comply with third party

license terms applicable to your use of third party software (including
open source software) that

may accompany Microchip software.

THIS SOFTWARE IS SUPPLIED BY MICROCHIP "AS IS". NO WARRANTIES, WHETHER

EXPRESS, IMPLIED OR STATUTORY, APPLY TO THIS SOFTWARE, INCLUDING ANY

IMPLIED WARRANTIES OF NON-INFRINGEMENT, MERCHANTABILITY, AND FITNESS

FOR A PARTICULAR PURPOSE.

IN NO EVENT WILL MICROCHIP BE LIABLE FOR ANY INDIRECT, SPECIAL,
PUNITIVE,

INCIDENTAL OR CONSEQUENTIAL LOSS, DAMAGE, COST OR EXPENSE OF ANY KIND

WHATSOEVER RELATED TO THE SOFTWARE, HOWEVER CAUSED, EVEN IF MICROCHIP

HAS BEEN ADVISED OF THE POSSIBILITY OR THE DAMAGES ARE FORESEEABLE. TO

THE FULLEST EXTENT ALLOWED BY LAW, MICROCHIP'S TOTAL LIABILITY ON ALL

CLAIMS IN ANY WAY RELATED TO THIS SOFTWARE WILL NOT EXCEED THE AMOUNT

OF FEES, IF ANY, THAT YOU HAVE PAID DIRECTLY TO MICROCHIP FOR THIS

SOFTWARE.

\*/

#include "mcc_generated_files/mcc.h"

#include "mcc_generated_files/examples/i2c2_master_example.h"

#include \<xc.h>

#include \<stdint.h>

#define address 0b1001100

#define tempreg 0x00

volatile uint8_t rx1;

volatile uint8_t rx2;

//process messages eusart communication between the pic and the sp32

void EUSART2_ISR(void)

{

    EUSART2_Receive_ISR();

    

    if(EUSART2_is_rx_ready()){

        

        rx1 = EUSART2_Read(); // read data from eusart 2 and place in
rx1

    

        while (!EUSART1_is_tx_ready());

        EUSART1_Write(rx1); // print rx1 data in eusart 1

        while (!EUSART1_is_tx_done()){};

    }

}

void EUSART1_ISR(void)

{

    EUSART1_Receive_ISR();

    

    if(EUSART1_is_rx_ready()){

        

        rx2 = EUSART1_Read(); // read data from eusart 1 and place in
rx2

    

        while (!EUSART2_is_tx_ready());

        EUSART2_Write(rx2); // print rx2 data in eusart 2

        while (!EUSART2_is_tx_done()){};

 

        LED_0\_Toggle();

    

    }

}

/\*

Main application

\*/

void main(void)

{

// initialize the device

SYSTEM_Initialize();

// When using interrupts, you need to set the Global and Peripheral
Interrupt Enable bits

// Use the following macros to:

// Enable the Global Interrupts

INTERRUPT_GlobalInterruptEnable();

// Enable the Peripheral Interrupts

INTERRUPT_PeripheralInterruptEnable();

// Disable the Global Interrupts

//INTERRUPT_GlobalInterruptDisable();

// Disable the Peripheral Interrupts

//INTERRUPT_PeripheralInterruptDisable();

SYSTEM_Initialize();

I2C2_Initialize();

EUSART1_Initialize();

uint8_t readtemp;

uint8_t temp;

while (1)

{

readtemp = I2C2_Read1ByteRegister(address, tempreg); //reading the temp
data from the sensor

temp = (readtemp\*1.8)+32; // calculating temp in degree C

if(-10\<=temp\<=100) { //check if the value make sense/PID

if(EUSART1_is_tx_ready())

{

readtemp = I2C2_Read1ByteRegister(address, tempreg);

temp = (readtemp\*1.8)+32;

printf ("temp = %uF \\n", readtemp,temp);

\_\_delay_ms(1000);

}

if (temp \<= 25){ // check if the temp is less than or equal to 25
degree C

RA2_SetHigh(); //turn the motor1 CW on

\_\_delay_ms(10000); //wait for 10 sec

RA2_SetLow(); // turn the motor1 off

\_\_delay_ms(10000); //wait for 10 sec

RA3_SetHigh(); //turn the motor2 CCW on

\_\_delay_ms(10000); //wait for 10 sec

RA3_SetLow(); // turn the motor2 off

if(EUSART1_is_tx_ready())

{

printf ("Cleaning is Done for Today"); // displaying "Cleaning is Done
for Today"

\_\_delay_ms(43200000); //wait for 12 hours

}

}

}

}

}

/\*\*

End of File

\*/

## **MCC Configuration**
