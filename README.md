# Ramen-Chef-Uni-Game-Dev-Project
Project for the extracurricular Game Dev, part of the masters degree Computer graphics by FMI in SU.  

# Student info
Ralitsa Kostadinova
Faculty number: 5MI3400297

# Game overview
Ramen Chef is a single-player cooking game controlled by a custom Arduino hardware controller. The player runs a small ramen stall during dinner rush, physically interacting with the game props and receiving information and instructions through the game's desktop visualisation.
The game is built in Unity 2D and communicates with an Arduino Uno via USB serial. The Arduino reads sensors, transmits a CSV string each frame and receives display commands back from Unity. 

# Core design pillars
- Physical part — every sensor maps to a real kitchen action.
- Parallel attention — the different actions demand focus simultaneously.
- One new mechanic per level — clean and explainable difficulty curve.

# Game Mechanics
- Pouring mechanism - the player pours broth soup into a bowl using a prop laddle. They have to do it in a certain way, if not - the soup will overflow or the bowl may end up half empty.
- Heat managment - the player controls the heat of the stove. They have to warm the broth in time for serving, but be careful to not burn it in the rush.
- Topping system - the player needs to do the ramen exactly as the client ordered it. One wrong topping and the soup gets returned to the chef - the topings cannot be removed once added to the food and will always affect the score.
- Queue logic - as the levels go up, the game gets harder. At certain part of the game there are two customers waiting for their orders simultaneously.

# Hardware and sensors 
- Laptop - runs the game itself, used for communication with the arduino and the other hardware
- Arduino - communicates with Unity the data from the sensors
- MPU6050 axelerometer - maps the tilting of the laddle, therefore the pouring of broth soup
- Potentiometer - stove dial for the temperature
- OLED display - shows the temperature of the stove
- Push buttons - each button symbolises a topping, when pressed the topping goes into the ramen 

# Level Design
- Level 1 - One customer at a time. No burn consequence. The focus is on the ladle tilt.
- Level 2 - Heat consequences get active. Up to 3 toppings per order.
- Level 3 - Two simultaneous customers. Prioritisation required.
- For future development - Adding more cutomers and second OLED screen to scroll the orders. Adding a VIP cutomer, whose order shows only for a few seconds and then it dissapears.

# Inspiration and credits
- Overcooked (Team17) — split-attention cooking under time pressure
- Cook, Serve, Delicious (Vertigo Gaming) — memorising and executing orders
- Keep Talking and Nobody Explodes — physical prop as primary interface

- Overcooked using arduino and sensors - https://www.instagram.com/p/DSrVVMnDlcN/
