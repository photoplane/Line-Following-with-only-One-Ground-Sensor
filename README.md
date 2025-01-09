# Line-Following-with-only-One-Ground-Sensor
In the book by Mordechai Ben-Ari and Francesco Mondada Elements of Robotics a section, page 48, is devoted to "Line Following with only One Ground Sensor" it is an approach to this application that will be carried out with Pygmy Forth. You should know that there is no analog-to-digital converter on the RaspberryPi, you must therefore use a specialized component (like the MCP3008) or make a small assembly with an LED, a photoresistor and a 1µF capacitor. This achievement is described here: https://pimylifeup.com/raspberry-pi-light-sensor/. We recover analog values ​​but very imprecise. However, the circuit being a grayscale track in the transverse direction, a measurement of the value in the center of the track allows to have a reference to guide the robot. For example, a value lower than the reference will shift the robot to the right and left for a reading higher than this reference. The rest is very simple, you only need three python primitives and the rest is in Pygmy Forth. 
The result may seem inefficient, but you have to remember, once again, that the RPi is not designed to process an analog signal.

![oneSensor](https://github.com/user-attachments/assets/e4f3efc4-bf57-46bf-ac88-c9469ab8f91c)




https://github.com/user-attachments/assets/a231db8e-4626-46e1-a97a-5bfeb815d766



https://github.com/user-attachments/assets/106e9857-0769-4db3-afde-1bca59317342

