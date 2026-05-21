# Welkomstbericht met drukknop

## Introduction
In deze tutorial leer je hoe je een welkomstbericht toont op de micro:bit wanneer je op een externe drukknop drukt die verbonden is met pin P1.

## Step 1
### Sluit de drukknop aan
Gebruik de kabels op tafel en verbind je drukknop:

- Verbind één kant van de knop met **P1**
- Verbind de andere kant met **GND**

👉 Zo kan de micro:bit detecteren wanneer de knop wordt ingedrukt


## Step 3
### Gebruik pinnen
Ga naar de categorie **Pinnen**.  
We gaan controleren of er op pin P1 wordt gedrukt.

```blockconfig
pins.digitalReadPin(DigitalPin.P1)
```

## Step 4
### Voeg een als-dan blok toe
Ga naar **Logica** en voeg een **als ... dan** blok toe.

```blocks
if (pins.digitalReadPin(DigitalPin.P1) == 1) {
    
}
```

## Step 5
### Toon tekst bij indrukken
Voeg een **toon tekst** blok toe binnen het **als ... dan** blok.

```blocks
basic.forever(function () {
    if (pins.digitalReadPin(DigitalPin.P1) == 1) {
        basic.showString("Hallo!")
    }
})
```

👉 De tekst verschijnt nu wanneer je op de knop drukt


## Step 6
### Test je programma
Druk op de knop en kijk wat er gebeurt:

- De boodschap verschijnt op de LED display
- Laat je los, dan stopt het bericht

## Step 7
### Download naar de micro:bit
Sluit je micro:bit aan en klik op **Download**.  
Test nu met de echte knop.

## Conclusion
Goed gedaan! Je hebt een drukknop aangesloten en gebruikt om een bericht te tonen op de micro:bit 🎉
