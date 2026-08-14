# ECP

To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in

AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in
keil.

APPARATUS REQUIRED

Keil.
Personal Computer
Keil μVision Software
Serial Transfer of Single Byte / Character using 8051 (Keil)


PROGRAM
(i) Serial Port Transfer a Single Character

#include<reg51.h>
void main(void)
{
TMOD=0X20;
TH1=0XFA;
SCON=0X50;
TR1=1;
SBUF='A';
while (T1==0);
T1=0;
while(1);
}

(ii) Serial Port to Transfer a Message

#include <reg51.h>
void main(void)
{
unsigned char msg[] = "RAVEENDRANATH";
unsigned char i;
TMOD = 0x20; // Timer1 Mode2
TH1 = 0xFD; // 9600 baud rate
SCON = 0x50; // Serial mode1
TR1 = 1; // Start Timer1
for(i = 0; msg[i] != '\0'; i++)
{
SBUF = msg[i];
while(TI == 0);
TI = 0;
}
while(1);
}

OUTPUT
(i) Serial Port Transfer a Single Character
<img width="1919" height="1023" alt="image" src="https://github.com/user-attachments/assets/078e1906-42a2-40d6-9a30-ebda5c0b979e" />







(ii) Serial Port to Transfer a Message

<img width="1919" height="1015" alt="image" src="https://github.com/user-attachments/assets/da6523ac-b3da-4c9f-b01f-2a62d3a5089d" />







RESULT

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
