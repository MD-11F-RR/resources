# <span style="color:#EA5823;font-weight:800">Example Name</span>


## <span style="color:#EA5823;font-weight:700">What you need</span>


## <span style="color:#EA5823;font-weight:700">Circuit</span>


## <span style="color:#EA5823;font-weight:700">Tips</span>


## <span style="color:#EA5823;font-weight:700">Code</span>


```swift
/*
  Mission5 Buzzer

  The buzz will play different tones when you rotate the potentiometer.

  The circuit:
  - Use Potentiometer Module or Light Sensor, and connect it to an Analog Jack.
  - Use Buzzer Module, and connect it to a Digital Jack.

  created 2019
  by Orange J

  Play a wonderful piece of music Happy Birthday!
  Numbered musical notation: 55 65 17 55 65 21 55 53 176 44 31 21.
  This example code is in the public domain.
  Visit madmachine.io for more info.
*/

import SwiftIO

let a0 = AnalogIn(Id.A0)

// PWM, also known as Pulse Width Modulation is a type of digital signal.
// The PWM signal can be used to configure a servo, or to control the dimming of a LED light.
// Initialize a PWM output pin.
let buzzer = PWMOut(Id.PWM2B)

while true {
    // Read the input voltage.
	value = a0.readPercent()
    
    //let value = a0.readPercent()
    let frequency = Int(1000 + 2000 * value) // calculate the float value into Int type to serve as frequency.
    buzzer.set(period: frequency, pulse: frequency/2) // Set PWM parameters.

    sleep(ms: 50) // Set the duration of the notes.
}

```


## <span style="color:#EA5823;font-weight:700">Video</span>


## <span style="color:#EA5823;font-weight:700">See Also</span>


## <span style="color:#EA5823;font-weight:700">References</span>

---
Last revision 2020/09/10 by Johnson