# Inchworm Robot
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails! 

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Austin L | Lynbrook High School | Mechanical Engineering | Incoming Freshman |

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

The robot is completed. I replaced the motors to fit the horns, and adjusted the code to make it work. My biggest challenges involve motors. The motors had a defect, like not fitting the horns, being too weak, or functioning differently. I altered the motors, as well as the code. I learned about Arduino microcontrollers and Servo motors, and I hope to learn more about remote control or remote sensing.

# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/x-Nej1nZgww?si=CaFHTCXpC0QC5G-u" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I have put together the parts in the  project. Many of my parts were different from the usaul parts. The motors, in particlar, were incompatable with the horns that attach them to the body. I had to use hot glue and other techniques to fix this. This is troubleshooting. I will need to make the robot able to close.

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/3o0YcmSlRyE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

The inchworm robot is made up of the motors, the parts that move, the Arduino and breadboard, where the code and circutry is, and the chassis, the body of the Inchworm.  I have made the motors move in the way the motor would move later. The motors were moving in a weird order, but with an arrangement of delay, I got it to work. Next, I would use 3D-printing to make the body or chassis of the inchworm, before putting it all together.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
#include <Servo.h>

Servo motor;
Servo motor1;
Servo motor2;

void setup() {
  delay(1000);
  motor.attach(8);
  motor.write(90);
  motor1.attach(7);
  motor1.write(55);
  motor2.attach(6);
  motor2.write(70);
  delay(1000);
}

void loop() {
  front();
  delay(50);
  open();
  delay(50);
  back();
  delay(50);
  close();
  delay(50);
}

void close() {
  delay(50);
  motor.write(0);
  delay(500);
  motor.write(90);
  delay(50);
}

void open() {
  delay(50);
  motor.write(100);
  delay(200);
  motor.write(90);
  delay(50);
}

void front() {
  delay(50);
  motor1.write(90); 
  motor2.write(45);
  delay(50);
}

void back() {
  delay(50);
  motor1.write(45); 
  motor2.write(135);
  delay(50);
}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Amount** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|:--:|
| Arduino Nano | 1 | The microcontroller, computer, or brain of the project  | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Small Breadboard | 1 | Connecting the Arduino's signals and power to the rest of the project | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| 9v Battery w/ Pigtail Connector | 1 | The power supply for removal of cable | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Micro Servo | 2 | Motors for rotating feet | $Price | <a href="https://www.amazon.com/Micro-Servos-Helicopter-Airplane-Controls/dp/B07MLR1498/ref=sr_1_5?crid=A4RT2ZMU6FIT&dib=eyJ2IjoiMSJ9.Z8zXoZs9nMkNwqQN2AI2Fkurdvj8MGFHhgFJWhnJQ_MKcq1cE-QbEgLJpLhrkaAgV5iBYW3qy7iEVTIzuk_FddavLfInfs0oUscB0OkT79B3X7LaUeGszw-nf6d1CAGl1Oy7H9eoiJHbU3tTY4RroycEiFcBt7FEa3cQeO0xD0TTjo7LMe9b5CMNrRIjCtMQHVoXp6z7I-RCJU0x4zle4gwIYFN1u7jwrtb6xKSDs6zd0iCkmNl0uoG8rE8h61Wpvcpn8cpIfol8hKY2Uyz7v0Ws67e6RE8_Rg62ARnyoDY.Dc5gIi99dM8VJAYrsnMkLVVD9o-cJBK57sIrwV5rdS8&dib_tag=se&keywords=sg90%2Bmicro%2Bservo&qid=1785167080&sprefix=%2Caps%2C139&sr=8-5&th=1"> Link </a> |
| Micro Servo | 1 | Different motor for main inchworm motion | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| 3D Printed Parts |  | The body the componets move and sit on | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Weatherseal | 1 | A grip for the feet | $10.27 | <a href="https://www.homedepot.com/p/Frost-King-5-16-in-x-1-4-in-x-17-ft-White-D-Center-EPDM-Medium-Gap-Weatherseal-Tape-V25WA/100017014"> Link </a> |
| Zipties | 3 | Securing the servos to the body | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Wires | 11 | Connecting power and signals between parts | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
