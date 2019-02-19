# InfraRed Communication :tv:

 This sketch/program uses the Arduino Board and IDE to run the code, and a PNA4602 (IR receiver) to
decode IR received. This can be used to make a IR receiver (by looking for a particular code)
 or transmitter (by pulsing an IR LED at ~38KHz for the durations detected).

## IR Receiver :inbox_tray:

- Wire up the circuit board to the Arduino,
- connect Arduino via USB to Arduino IDE,
- open *IR-Receiver.ino* on Arduino IDE,
- Open Serial Monitor,
- point the remote control to the IR receiver (PNA4602) and press once the button to be copied,
- Check monitor for values,
- Copy the list of values.

## IR Transmitter :outbox_tray:

- Wire up the circuit board to the Arduino with IR emitter and the trigger button,
- connect Arduino via USB to Arduino IDE,
- open *IR-tv-Send.ino* on Arduino IDE,
- Go to end of code and replace the *ON* and *OFF* times:
```
delayMicroseconds(51908);      //Time off (LEFT column)
pulseIR(9360);                //Time on (RIGHT column)
```
You have to do it manually :sweat_smile:
I'll come up with some automated way to do it.
Make sure you replace them all with the values collected from the IR Receiver process,
sometimes you need to add or delete some lines of code depending on the brand/model of what
you are trying to control (TV, radio, Air cond...)
