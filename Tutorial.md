# Podiumschermen

## It's time to code! @showdialog

Het festival gaat beginnen, klaar om als podiumtechnieker aan de slag te gaan!?

## Verwelkom de festivalgangers
Sleep de ``||basic:toon tekens||`` blok in de ``||basic:de hele tijd||`` blok. En toon een leuke verwelkomingsboodschap.

```blocks
basic.forever(function () {
    basic.showString("Welkom")
})
```

## Laat de lichten aangaan

Als de knop aan de zijkant is ingedrukt, dan moet de lichten wisselen van rood, naar groen, naar blauw.
Sleep de ``||logic:Als dan||`` blok uit de ``||logic:Logisch||`` categorie in de ``||basic:de hele tijd||`` blok.

```blocks
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P1, 0)
basic.forever(function () {
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
        pins.digitalWritePin(DigitalPin.P2, 0)
        pins.digitalWritePin(DigitalPin.P8, 1)
        pins.digitalWritePin(DigitalPin.P12, 1)
        basic.pause(1000)
        pins.digitalWritePin(DigitalPin.P2, 1)
        pins.digitalWritePin(DigitalPin.P8, 1)
        pins.digitalWritePin(DigitalPin.P12, 0)
        basic.pause(1000)
        pins.digitalWritePin(DigitalPin.P2, 1)
        pins.digitalWritePin(DigitalPin.P8, 0)
        pins.digitalWritePin(DigitalPin.P12, 1)
        basic.pause(1000)
    } else {
        pins.digitalWritePin(DigitalPin.P2, 1)
        pins.digitalWritePin(DigitalPin.P8, 1)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
})
```
