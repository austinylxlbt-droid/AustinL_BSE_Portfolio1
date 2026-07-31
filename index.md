# Inchworm Robot
An inchworm moves differently from any other object, moving by opening and closing with Servo motors. I made the inchworm robot, but not without many roadblocks and challenges along the way.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Austin L | Lynbrook High School | Mechanical Engineering | Incoming Freshman |

<img width="575" height="384" alt="Screenshot 2026-07-31 at 10 03 19 AM" src="https://github.com/user-attachments/assets/06d97280-07a5-429b-9f63-91c4108d8214" />
<img width="146" height="146" alt="Screenshot 2026-07-31 101654" src="https://github.com/user-attachments/assets/8d9f7f35-547f-4dc5-a200-d66fb857b1dd" />


# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/8AVximU8iAQ?si=WktEF0cOeeXZzi6N" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

The robot is completed. I replaced the motors to fit the horns, and adjusted the code to make it work. My biggest challenges involve motors. The motors had a defect, like not fitting the horns, being too weak, or functioning differently. I altered the motors, as well as the code. I learned about Arduino microcontrollers and Servo motors, and I hope to learn more about remote control or remote sensing.

# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/x-Nej1nZgww?si=CaFHTCXpC0QC5G-u" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I have put together the parts in the  project. Many of my parts were different from the usual parts. The motors, in particlar, were incompatable with the horns that attach them to the body. I had to use hot glue and other techniques to fix this. This is troubleshooting. I will need to make the robot able to close.

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/3o0YcmSlRyE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

The inchworm robot is made up of the motors, the parts that move, the Arduino and breadboard, where the code and circutry is, and the chassis, the body of the Inchworm.  I have made the motors move in the way the motor would move later. The motors were moving in a weird order, but with an arrangement of delay, I got it to work. Next, I would use 3D-printing to make the body or chassis of the inchworm, before putting it all together.

# Schematics 
<img width="497" height="254" alt="Screenshot 2026-07-30 114548" src="https://github.com/user-attachments/assets/f9c63965-bb70-4af7-8b1a-4fba63c6f186" />
<img width="368" height="490" alt="Screenshot 2026-07-30 120212" src="https://github.com/user-attachments/assets/57a70c45-5afc-4379-9f31-832878a53727" />

# Code

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

| **Part** | **Amount** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|:--:|
| Arduino Nano | 1 | The microcontroller, computer, or brain of the project  | $15.99 | <a href="https://www.amazon.com/LAFVIN-Board-ATmega328P-Micro-Controller-Arduino/dp/B07G99NNXL/ref=sr_1_4?crid=3JR9NZIRE6EX9&dib=eyJ2IjoiMSJ9.QmNYvO8VeEYJRoPLV8e0zctqT2oRtwroDCO2-jHie3PO0hkxBx_7VlrxfkkjsxSwf11b4ngFUT1DQZmeEJm6-HVFXr5KMyHJuWxNWg2ZxCOIdAwluEXCkqkwFhjx6hJr8lt9E3St_WDqeL7VLqjO4C-DcrIiSD-sVaVhtQiW23_vy9j-UnmJrjXlqns1JM3GmuWm95YMoZC21r1NmPD02k7Ncn4t1B2-oTSt4BynKlY.lyvShFcj-smjllHVP26siVFLFsw-Tf_wE1Glh9J9-hs&dib_tag=se&keywords=arduino+nano&qid=1785340262&sprefix=arduino+nano%2Caps%2C165&sr=8-4"> Link </a> |
| Small Breadboard | 1 | Connecting the Arduino's signals and power to the rest of the project | $9.99 | <a href="https://www.amazon.com/BOJACK-Values-Solderless-Breadboard-Flexible/dp/B08Y59P6D1/ref=sr_1_7_sspa?crid=34T7ND7XL7E5G&dib=eyJ2IjoiMSJ9.EQvCK09g_r0CejNbKABqFcXKydXK1tmlZ6l7WbJ6SayOBgx6k72RgbTq8ALmsR8fuKqWTcDHIONZTFwHWQTSXqFZKRWeFiMr0ZWgxwKeqF4KLTkd0Wi--bj5_eaTL04mU7c54GYE9rKIKlK8IXUK_iElWSE3xZ3CSCog_Hsxg8XrTrp0Im9U0OghvKkRWx7pwmL7zR1lOzH2VTnJVpXXGlIiQVQUrRdLmRr-QWQAJoc.JeXO8lM-MSfWieY4YRAqKp7R5yruiddh5wigP8ECTl0&dib_tag=se&keywords=small%2Bbreadboard&qid=1785341065&sprefix=small%2Bbread%2Caps%2C171&sr=8-7-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9tdGY&th=1"> Link </a> |
| 9v Battery | 1 | The power supply for removal of cable | $9.79 | <a href="https://www.amazon.com/Amazon-Basics-Performance-All-Purpose-Batteries/dp/B0774D64LT/ref=sr_1_7?crid=3CBKQDV4L7R6I&dib=eyJ2IjoiMSJ9.by69tUnxi0q6-YnaJD-4K7nTJGbLULtKhQmcMN_e-eWSWX_LFhSb8EmZCcEGEnmAMcne3sZc3qQtDKCHRV2fFDuzxJTYGKDvMfeBdIKd9-PwSiDpklGGzr8IjrezflbErsZmRtudnkuWE_csKIYD33jddeFS98ikd7HEvR54uDEYGfWHHqesw3QVxAAc0Ybdc7wmPbPre-teFFOVZTOcpJIjA0FcIXoIw1RBkWyqa6ki1Xm3QWbos-ogCuzsQz7hWDDWrmKMsmxCc5FKFa9N3NWEQqR9-cA8O3FYOx3icEY.OcLAmknB_YyvRgA2ktc1E6b6Yh42iVkrQzUa1ZfhKZw&dib_tag=se&keywords=9v%2Bbattery&qid=1785255759&rdc=1&sprefix=9v%2Bbattery%2Caps%2C233&sr=8-7&th=1"> Link </a> |
| Pigtail Connector | 1 | Connecting the battery to the Arduino and breadboard | $3.59 | <a href="https://www.amazon.com/California-JOS-Battery-PCS-Experiment/dp/B0CR8RKQ5Q/ref=sr_1_1_sspa?crid=1L723AKMRNVWO&dib=eyJ2IjoiMSJ9.5Yx6TBGcuOZfvmyHBW8xP2cSseI3_YQdz9rD_LFdp3_Dw3ImlTAHgl_rKULY-yhl4kMz_JhdFNA4xpWDEkTYwF2WI5XRw6axw9uShHUHuRzJ6dHAga3ATGQfGkJeYne6kzXsOGviqwCXPZnPQsWDYZlV2KyqZ19hRHP-7AEUX7w4xcCuZiqqP15mwo78I0Ofvr8FK-_vRcr4MoFxqb5V3j7uNJzDW5HqtEW7dE89PJ0.GlTR79Z-q0hLThx6Kp9mFvj4dCuvUltYn-wOwDieOQo&dib_tag=se&keywords=9v%2Bbattery%2Bpigtail%2Bconnector&qid=1785256123&sprefix=9v%2Bbattery%2Bpigtail%2Caps%2C260&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1"> Link </a> |
| Micro Servo | 2 | Motors for rotating feet | $7.98 | <a href="https://www.amazon.com/Micro-Servos-Helicopter-Airplane-Controls/dp/B07MLR1498/ref=sr_1_5?crid=A4RT2ZMU6FIT&dib=eyJ2IjoiMSJ9.Z8zXoZs9nMkNwqQN2AI2Fkurdvj8MGFHhgFJWhnJQ_MKcq1cE-QbEgLJpLhrkaAgV5iBYW3qy7iEVTIzuk_FddavLfInfs0oUscB0OkT79B3X7LaUeGszw-nf6d1CAGl1Oy7H9eoiJHbU3tTY4RroycEiFcBt7FEa3cQeO0xD0TTjo7LMe9b5CMNrRIjCtMQHVoXp6z7I-RCJU0x4zle4gwIYFN1u7jwrtb6xKSDs6zd0iCkmNl0uoG8rE8h61Wpvcpn8cpIfol8hKY2Uyz7v0Ws67e6RE8_Rg62ARnyoDY.Dc5gIi99dM8VJAYrsnMkLVVD9o-cJBK57sIrwV5rdS8&dib_tag=se&keywords=sg90%2Bmicro%2Bservo&qid=1785167080&sprefix=%2Caps%2C139&sr=8-5&th=1"> Link </a> |
| Micro Servo | 1 | Different motor for main inchworm motion | $9.99 | <a href="https://www.amazon.com/AILUOMI-MG90S-Compatible-Arduino-Raspberry/dp/B0G4W72Z3V/ref=sr_1_2_sspa?crid=2GW3M9HSC2CGY&dib=eyJ2IjoiMSJ9.EdycfDxnDtcyy4IWKKo05MB-738x75AKe4V5UYnoE9T7rv2qsMxgNECJ0QHNvlp7eFw3VkhmwsFuGQzTCl35F6FW6r5VyfRb_UtWjn9XQg8-qG_qYvszhW1vFEaGritMwl9Mvgv87f9ERWLHYxMlQsF7ZmcIPKtwguUUZOhj8CcmV0S6g_NT5o9e1csuvZMrU14CsgkWMfNFNX9LCmxNTUnvw9hIwd5I_LPtYRD7CKFSjJGnphuc_YzrkmmzwWjc2TUtI9cnmpHtDik0bJTQZfxxoZkK-uNCqN0hvq7gQp4.3dqj6kyvmx9Y5ZOELWSn0n3AoqyZTjPjJIXuJYeMMkU&dib_tag=se&keywords=mg90s&qid=1785255516&sprefix=mg90s%2Caps%2C223&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1"> Link </a> |
| 3D Printed Parts | 4 | The body the components move and sit on | $Price | <a href="Screenshot 2026-06-26 102806.png"> Link </a> |
| Weatherseal | 1 | A grip for the feet | $10.27 | <a href="https://www.homedepot.com/p/Frost-King-5-16-in-x-1-4-in-x-17-ft-White-D-Center-EPDM-Medium-Gap-Weatherseal-Tape-V25WA/100017014"> Link </a> |
| Wax Paper | 1 | Aid for sliding motion | $2.66 | <a href="https://www.amazon.com/Reynolds-Cut-Rite-Paper-Square-Foot/dp/B0036QO8M6/ref=sr_1_3?crid=AQML1FGXOO97&dib=eyJ2IjoiMSJ9.Pxkl6jq2eSgwsMmKCpxwWbfxJXZ_JHxXqmSrfMdtDVQALXJWb3olXmXXNXgM48fvxg0bdZ8Azhxhbqxmdfi-pv0o5ALJpNnBfSGyJPA0ZmNZF82Owg0lwxRD9MGwC9SW7q_X2odykFoLwn0aYwigQQJi4Z5h2n07Isq89b0itkTC3iJWu0rszsgBIezJw2D4-qkocjojc3fnIiGlVqnKJGwkDlK5ubg0a3rj9AtyBShz0TU--gi6lTLCpBf-o1J87WVOnLpQvVcKnOuZEljyQGBAeXXsoBhHRcjmr2LpEjQ.PEqaD0Zx7s9PbZFNYp8wcOPj27XlDzG0WlbR_Lb3sek&dib_tag=se&keywords=kitchen%2Bwax%2Bpaper&qid=1785256631&sprefix=kitchen%2Bwax%2Bpaper%2Caps%2C181&sr=8-3&th=1"> Link </a> |
| Zipties | 3 | Securing the servos to the body | $3.44 | <a href="https://www.homedepot.com/p/HDX-8-in-UV-Resist-Zip-Ties-Black-20-Pack-FT-200STUV-20/307799394"> Link </a> |
| Wires | 11 | Connecting power and signals between parts | $9.99 | <a href="https://www.amazon.com/BOJACK-Values-Solderless-Breadboard-Flexible/dp/B08Y59P6D1/ref=sr_1_7_sspa?crid=34T7ND7XL7E5G&dib=eyJ2IjoiMSJ9.EQvCK09g_r0CejNbKABqFcXKydXK1tmlZ6l7WbJ6SayOBgx6k72RgbTq8ALmsR8fuKqWTcDHIONZTFwHWQTSXqFZKRWeFiMr0ZWgxwKeqF4KLTkd0Wi--bj5_eaTL04mU7c54GYE9rKIKlK8IXUK_iElWSE3xZ3CSCog_Hsxg8XrTrp0Im9U0OghvKkRWx7pwmL7zR1lOzH2VTnJVpXXGlIiQVQUrRdLmRr-QWQAJoc.JeXO8lM-MSfWieY4YRAqKp7R5yruiddh5wigP8ECTl0&dib_tag=se&keywords=small%2Bbreadboard&qid=1785341065&sprefix=small%2Bbread%2Caps%2C171&sr=8-7-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9tdGY&th=1"> Link </a> |

# Other Resources/Examples
[Tutorial](https://www.instructables.com/Inchworm-Robot/)
