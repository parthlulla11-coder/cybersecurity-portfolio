Learning Objectives - 

* Representing 8 colors

* Representing 16 million colors

* Binary numbers

* Hexadecimal numbers

* (Optional) Octal numbers

Main objective of the topic - 
* how computers represent colors and understand numbers (specifically positive integers). Being familiar with binary and hexadecimal system representations is a must when you use various computer tools, especially in the domain of cyber security.

*Our First Eight Colors* - 

By combining different amounts of red, green, and blue lights, you can get any color you like. In computer colors, think of it like three knobs, and each knob controls one of the three colors.
Example

*Let’s say that each of the three colors can be either on or off, i.e., each has two states.*

* The red light can be either on or off
* The green light can be either on or off
* The blue light can be either on or off
* These states give us 2 × 2 × 2 = 8, that’s eight different colors.

<img width="956" height="636" alt="image" src="https://github.com/user-attachments/assets/0bee68e8-2fc9-49c0-9821-185a5b7634f5" />

If a computer were limited to 8 colors, it would only need to indicate which color is “switched on” and which is “switched off.” In fact, it can use three digits of 1 and 0 to represent the states of red, green, and blue. For example, 111 would be all 3 lights switched on, while 100 would be only the red switched on. This digit, which can be either 1 or 0, is called a bit.

Now, a computer can represent any of the 8 colors. If this is still unclear, a detailed list is shown in the table below.

<img width="996" height="475" alt="image" src="https://github.com/user-attachments/assets/930092e7-c267-42f8-b6b9-267555baf02a" />

*From 8 to 16,000,000*

* Being limited to eight colors is inconvenient, as we prefer millions of colors. It would be convenient if each of the 3 lights (red, green, and blue) had 256 levels instead of just 2 (on or off).
* repeat the same math as earlier: 256 × 256 × 256 = 16,777,216. That’s more than 16 million colors; that covers most of our needs.
* One bit is enough to represent 2 states: on and off. We need 8 bits to express 256 states. In most textbooks, a group of 8 bits is referred to as a byte; however, you can also use the term octet.

*Hexadecimal Representation*

<img width="823" height="726" alt="image" src="https://github.com/user-attachments/assets/7197b551-8a16-4dfe-a8ce-c6ae04545152" />

To summarise what we have covered so far:

* In real-life applications, a color is represented in 24 bits, i.e., 3 bytes
* Each byte can represent 256 different values
* Each of the three bytes specifies the intensity of the red, green, and blue lights
* Every 4 bits are represented by one hexadecimal digit
* Each byte is represented as two hexadecimal digits

**Numbers: from Decimal to Hexadecimal**

* Low and High in voltage range (example: transistor-transistor logic)
* North and South in magnetic polarity (example: hard disk drives)
* Light presence (example: fiber optics)

**Binary Numbers**

The binary (base-2) system can be expressed similarly to what we wrote earlier, discussing the decimal (base-10) system. The key differences are that the binary system is limited to two digits, 0 and 1, and that everything is a power of 2. Let’s consider a couple of examples.

The binary number 1001 can be expressed as follows: 1001 = 1 × 23 + 0 × 22 + 0 × 21 + 1 × 20 = 1 × 8 + 0 × 4 + 0 × 2 + 1 × 1 = 8 + 0 + 0 + 1 = 9. We just demonstrated how to write 9 in binary.

Following the same approach, it won’t be challenging to convert the binary numbers 0000, 0001, 0010, 0011 to the decimal system. Let’s go through these four conversions.

0000 = 0 × 23 + 0 × 22 + 0 × 21 + 0 × 20 = 0 × 8 + 0 × 4 + 0 × 2 + 0 × 1 = 0

0001 = 0 × 23 + 0 × 22 + 0 × 21 + 1 × 20 = 0 × 8 + 0 × 4 + 0 × 2 + 1 × 1 = 1

0010 = 0 × 23 + 0 × 22 + 1 × 21 + 0 × 20 = 0 × 8 + 0 × 4 + 1 × 2 + 0 × 1 = 2

0011 = 0 × 23 + 0 × 22 + 1 × 21 + 1 × 20 = 0 × 8 + 0 × 4 + 1 × 2 + 1 × 1 = 3

As an exercise, we will convert four more binary numbers, 1100, 1101, 1110, and 1111, to the decimal system. Try to do this on a piece of paper before comparing your answers with the solutions below.

**The numbers written as "10(2) = 10 has the power of 2 (10 x 10)"**

Example for making this calculation easier - 

**10(2) = 100, 10(1) = 10, and 10(0) = 1** 

found a way to crack this in a simpler way (for a non math guy)

suppose we need the conversion of Binary number - 1100 to Decimal system - 

* step 1 - write the Binary as it is - 

1100 

Let's break down the numbers - 

first number - 1
second number - 1
third number - 0
fourth number - 0 

* Step 2 - 

(Now follow this Formula in every conversion)

first number * 2(3) + second number 2(2) + third number * 2(1) + Fourth number * 2(0)

* step 3 - (Applying formula) - 

1100 - 1 x 2(3) + 1 x 2(2) + 0 * 2(1) + 0 * 2(0)

* Step 4 simplify stage 1 - 

1 x 8 + 1 x 4 + 0 x 2 + 0 x 1

* Step 5 simplify stage 2

8 + 4 + 0 + 0

= 12 

Please refer below for more clarification - 


* 1100 Sol -  1 x 2(3) + 1 x 2(2) + 0 * 2(1) + 0 * 2(0) = 1 x 8 + 1 x 4 + 0 x 2 + 0 x 1 =  8 + 4 + 0 + 0 = 12
* 1101 Sol - 1 x 2(3) + 1 x 2(2) + 0 x 2(1) + 1 x 2(0) = 1 x 8 + 1 x 4 + 0 x 2 + 1 x 1 = 8 + 4 + 0 + 1  =  13
* 1110 Sol - 1 x 2(3) + 1 x 2(2) + 1 x 2(1) + 0 x 2(0)  = 1 x 8 + 1 x 4 + 1 x 2 + 0 x 1 = 8 + 4 + 2 + 0 = 14
* 1111 Sol - 1 x 2(3) + 1 x 2(2) + 1 x 2(1) + 1 x 2(0)  = 1 x 8 + 1 x 4 + 1 x 2 + 1 x 1 = 8 + 4 + 2 + 1 = 15

Using a shorter form - **1100**  = 1 x 8 + 1 x 4 + 0 x 2 + 0 x 1 =  8 + 4 + 0 + 0 = **12** 

**Hexadecimal Numbers**

<img width="828" height="724" alt="image" src="https://github.com/user-attachments/assets/24cab333-ec04-44cd-b99a-e74e4faf4975" />

* Converting From Hexadecimal to Decimal System - 

* 9BDF = 9 × 163 + 11 × 162 + 13 × 161 + 15 × 160 = 9 × 4096 + 11 × 256 + 13 × 16 + 15 × 1 = **39,903**

**Formula for Hexadecimal to Decimal System is - 16(3), 16(2), 16(1), 16(0)** 
**Formula we had for the binary to decimal -  2(3), 2(2), 2(1), 2(0)**

(use the table above to figure out the Hexadecimal to Binary Representation.)

**Octal Numbers** 

The octal system refers to base 8. In other words, it uses the digits between 0 and 7. While the hexadecimal system uses base 16 and groups 4 bits, the octal system uses base 8 and groups 3 bits. The table below shows how the octal digits relate to their binary counterparts.

<img width="935" height="448" alt="image" src="https://github.com/user-attachments/assets/66320ae7-29b8-42ea-8765-b632eb4377f2" />

 Converting From Octal to Decimal System - 

 Converting an octal number to its decimal equivalent follows the steps of the previous conversions. Consider the octal number 357.

**357 = 3 × 82 + 5 × 81 + 7 × 80 = 3 × 64 + 5 × 8 + 7 × 1 = 239**

**Formula - first digit x 8(2), second digit x 8(1), third digit x 8(0)**


Conclusion - 

*Decimal (Base-10) system: This is the system we use in our everyday life.
*Binary (Base-2) system: Computers understand two states, which are encoded as 0 and 1.
*Hexadecimal (Base-16) system: Every 4 binary digits (bits) can be grouped as one hexadecimal digit. A hexadecimal digit ranges between 0 and F.
*Octal (Base-8) system: Every 3 binary digits (bits) can be grouped as one octal digit. An octal digit ranges between 0 and 7. This one is less commonly encountered on computer systems.


we learned how a color can be represented. We covered:

*Bit: It is short for binary digit, and it can be either 0 or 1.
*Byte: On modern systems, a byte is 8 bits. It is also referred to as an octet.
*Hex color: A color is represented as a combination of red, green, and blue on computer systems. If one byte is assigned for each of the primary colors (red, green, and blue), we can get more than 16 million color combinations.

