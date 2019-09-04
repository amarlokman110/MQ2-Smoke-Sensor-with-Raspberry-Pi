# MQ2 Smoke Sensor with Raspberry Pi

<img src="https://user-images.githubusercontent.com/54172575/64233343-8941ab80-cf26-11e9-8ccd-dd93ad6914f9.jpg" width="300" />

The smoke sensor we will use is the MQ-2. This is a sensor that is not only sensitive to smoke, but also to flammable gas.

The MQ-2 smoke sensor reports smoke by the voltage level that it outputs. The more smoke there is, the greater the voltage that it outputs. Conversely, the less smoke that it is exposed to, the less voltage it outputs.

The MQ-2 also has a built-in potentiometer to adjust the sensitivity to smoke. By adjusting the potentiometer, you can change how sensitive it is to smoke, so it's a form of calibrating it to adjust how much voltage it will put out in relation to the smoke it is exposed to.

We will wire the MQ-2 to a raspberry pi so that the raspberry pi can read the amount of voltage output by the sensor and output to us if smoke has been detected if sensor outputs a voltage above a certain threshold. This way, we will know that the sensor has, in fact, detected smoke.

## Components Needed

* Raspberry Pi board
* MQ2 smoke sensor
* MCP 3008 Analog to digital converter chip

## Source Code
```if SmokeTrigger > 1.5:
            print("Gas leakage")
            print"Current Gas AD vaule = " +str("%.2f"%((COlevel/1024.)*3.3))+" V"
            time.sleep(1)
            
        else:
            print("Gas not leak")
            time.sleep(0.5)```
