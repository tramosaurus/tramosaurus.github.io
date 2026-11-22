---
title: "ENGR 22 Lab 1: Safety and Equipment"
date: "2026-11-20"
author: "T. Dang"
---

Site URL: {{ site.url}}

Base URL: {{site.baseurl }}

Page URL: {{ page.url }}

Fixme: {{ site.fixme }}  ![Fix Me!](/assets/img/fixme.svg)

## Equipment Needed for This Lab
From your kit:
- Resistors: 100, 220, 470, 1k 

From the lab:
- Power Supply (5V)
- Breadboard
- Digital Multimeter

## Laboratory Safety and Hazards

Watch the following video on laboratory safety: Lab Safety Video 

### Why Does Safety Matter?

While the circuits we’re going to be building in this class are all designed to be safe to handle, it’s still important to understand that the electrically powered equipment can pose a serious risk if you’re not careful. Many pieces of equipment in a typical research lab have high voltage or high-power requirements, which make them even more dangerous to operate. Certain components, like capacitors, can store a lot of energy even after its been disconnected from its power source.

### What Can Happen?

Electricity can cause fatal burns or cause vital organs to malfunction. It all depends on how much, how long, and where. In general, a current of 5 mA or less will cause a sensation of shock, but rarely any damage. Larger currents can cause hand muscles to contract. Currents on the order of 100 mA are often fatal if they pass through the body for even a few seconds. The chart below shows the general relationship between the degree of injury and amount of current for a 60-cycle hand-to-foot path of one second's duration of shock.

*Table 1: Effects of a range of electrical current passing through the human body.*
{: .table-caption}

| Current (mA) | Reaction |
| :---: | --- |
| 1	| Perception level |
| 5	| Slight shock felt; not painful but disturbing |
| 6-30 | Painful shock; “let-go” range |
| 50-150 | Extreme pain, respiratory arrest, sever muscular contraction |
| 1,000-4,300 | Ventricular fibrillation |
| 10,000+ | Cardiac arrest, severe burns, and probable death |

### Is it Safe to Touch?

Is it okay to touch a wire on our breadboard if it has a voltage potential of 12 V?  It's all dependent on the resistance of the human body. Our skin typically has pretty high resistance, making us pretty resilient towards voltages, but that depends on moisture levels and the integrity of your skin. Generally speaking, 50 V or lower are safe handling levels (some would argue more and some less) for AC and DC voltages.

### Lab Rules

During your work on these labs you should follow safe electronics practices and always turn off power to your circuit before building it or modifying the wiring. This will prevent you from “frying” circuit components as well – many components are less tolerant of moderate voltage levels than humans are.

- **Never work on a circuit while power is applied.** Be sure to disconnect or turn off your power source while you are moving your circuit components around.
- **Do not connect power to a circuit until the circuit is finished.** Check your work carefully before you connect or turn on your power source.
Disconnect the power source if you smell anything burning. The smell of burning electronics components is very distinct and hard to miss! Turn off your power source the minute you smell it, and inspect your circuit for errors. Be careful! Some of the components may be very hot.
- **Keep your work area dry.** Electricity will happily conduct through water, and will also lower your skin's resistivity. No food or drink in the lab!
- **Always use common sense and pay attention to the task you are working on.**
- **If at any time you are not sure how to handle a particular situation, ask the instructor for advice.**

<div class="e22-lab-activity" markdown="1">

### Complete Activity 1: Safety Hazards Related to Electricity and Electronics Equipment

The full directions for the activity can be found on your Activity Data Record Sheet.

</div>

## Reading Resistor Codes

You probably realized that it’s hard to identify the different resistor values, but that the colors somehow indicate the resistance. Watch the following video on identifying resistor color bands:
Identifying Resistor Color Bands

### What Are Resistor Codes?

If you’ve worked with electronics before, you’ve probably seen the color bands painted on most resistors. These bands help us identify the value of resistance without resorting to using an ohmmeter. There are a lot of websites that will help you identify the resistance such as this one, but we're going to learn how to read them anyway.

### Four or Five Bands?

Resistors marked with color bands come in two types: one with four color bands, and one with five color bands. Resistors with five color bands have a smaller tolerance of 1% and use the extra band to specify the value more precisely. We'll be using resistors with four color bands in our lab.

### Reading Resistor Values

To figure out the resistance value of a four-band resistor, start by finding the gold or silver band, known as the tolerance band. Rotating the resistor so that the tolerance band is on the right side.

{% include figure.html
   src="../img/resistor-band.png"
   alt="The image shows a close-up of a four-band resistor. The resistor is oriented so that the right-most band is gold, which is the tolerance band. The first band is orange, the second band is blue, and the third band is brown. The color bands tell us that it's a 360 ohm resistor."
   caption="Figure 1. How to orient a resistor to read resistor band colors." %}

The first three color bands are arranged as follows: the first band, the second band, and the multiplier band. For these three bands, each color represents a different value, which can be found in the chart below. (The final column represents a mnemonic device to help you remember.)

_Table 2. Resistor color and the corresponding value._
{: .table-caption}

| Value | Color | Word |
| :---: | :---: | :---: |
| 0 | Black | Black |
| 1 | Brown | Birds |
| 2 | Red | Run |
| 3 | Orange | Over |
| 4 | Yellow | Your |
| 5 | Green | Garden |
| 6 | Blue | But |
| 7 | Violet | Vegetables |
| 8 | Gray | Grow |
| 9 | White | Wonderfully |

You can use the mnemonic device to help you remember: 

> Black birds run over your garden but vegetables grow wonderfully.

The most significant digit of our resistor value is represented by first band, while the least significant is represented by the second band. We then multiply this value by ten raised to the power of the multiplier band. That means that for a resistor colored orange - blue - brown, the nominal resistance is 

$$
36 \times 10^1=360 \text{ }\Omega
$$

Five-band resistors are similar, except that the first three bands represent the three significant digits of the resistor value. The fourth band represents the multiplier. In addition to the values from the above table, the multiplier band can also be gold or silver, which represent $0.1$ and $0.01$, respectively.

_Table 3. Extra multiplier color bands and their corresponding values._
{: .table-caption}

| Value | Color |
| :---: | :---: |
| 0.1 | Gold |
| 0.01 | Silver |

### Resistance Tolerances

Resistors are never manufactured to exact values—it would be too expensive. Instead, the manufacturer guarantees that a resistor value will fall within the tolerance range specified by the last band, called the tolerance band. A resistor with a gold band for the tolerance will be guaranteed to fall within 5% of the nominal value. The table of tolerance colors is given below.

_Table 4. Resistor color bands and their corresponding tolerance values._
{: .table-caption}

| Tolerance | Color |
| :---:| :---: |
| 1% | Brown |
| 2% | Red |
| 5% | Gold |
| 10% | Silver |

The formula to calculate the minimum and maximum values for a given resistor color code is given below. The true resistance value should fall within this range.


$$
\text{minimumum value} = \text{nominal value} \times (1-\frac{\text{tolerance, in }\%}{100})
$$

$$
\text{minimumum value} = \text{nominal value} \times (1+\frac{\text{tolerance, in }\%}{100})
$$

### Summary

You can use the following image to help you determine the nominal value of your resistor.

{% include figure.html
   src="./img/resistor-chart.png"
   alt="An instructional diagram showing how to read a resistor’s color bands to determine its resistance. Five color bands on a resistor are connected by lines to a color-coded chart showing the digit values (0–9), the multiplier values (powers of ten), and tolerance values. The top example shows a resistor with orange, blue, red, and gold bands, corresponding to 36 × 10 = 360 ohms. The bottom example shows a resistor with green, blue, black, gold, and brown bands, corresponding to 460 × 0.1 = 46 ohms, with 1% tolerance. The chart identifies gold as a 5% tolerance band and silver as a 10% tolerance band."
   caption="Figure 2. Resistor chart to help you determine the resistance." %}
 
<div class="e22-lab-activity" markdown="1">

### Complete Activity 2: Identifying Resistor and Resistor Color Codes

The full directions for the activity can be found on your Data and Answer Sheet.

</div>

## At Home Use: Installing Software

If you would like to work on your laboratory assignments at home, you may wish to install the following software on your personal laptop or desktop. The listed software is compatible with Linux, Mac, and Windows.

### Waveforms for Digilent Analog Discovery 3

To operate the Digilent Analog Discovery 3, you will need to install WaveForms, which is compatible with Linux, Mac, Windows, and ARM. 

Get the software here: [WaveForms ](https://digilent.com/shop/waveforms/)

### Fritzing

Fritzing is a great way to help you convert bread board prototypes into circuit diagram schematics. You can even use it to create vias for printed circuit boards! Fritzing is compatible with Linux, Mac, and Windows.

Get the software here: [Fritzing](https://fritzing.org/)

### LTspice

LTspice is an open-source circuit simulator that is based on SPICE. It's a bit clunky to use, but hey-- free is free! It is available for Windows and MacOS.

Get the software here: [LTspice](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html)

<div class="e22-lab-activity" markdown="1">

### No activities to complete, however you may consider installing the above software.

</div>

## Breadboard Basics

Watch the video on breadboarding basics:

<iframe
	class="responsive-frame"
    src="https://www.youtube.com/embed/6WReFkfrUIk" 
	allowfullscreen>
</iframe>

### How a Breadboard is Constructed

Breadboards are a great tool for prototyping electronics projects, and is a necessary tool for electronics design. The original breadboards were originally just that – wooden boards used for cutting bread, and date all the way back to the beginning of electrical experimentation. (If you’re curious to see them in action, this You-tuber wires up a circuit on a wooden breadboard in this video.) Modern breadboards are plastic tablets that have rows of holes connected underneath with metal clips.

These boards are great for prototyping and testing new circuits. Components can be placed into the breadboard and pulled out easily, and requires no soldering or other more permanent connections. The figure below shows a picture of the breadboard (left) and a diagram showing how the individual holes are connected with the metal clips.

{% include figure.html
   src="./img/breadboard-routing.png"
   alt="A side-by-side comparison of a solderless breadboard (left) and its internal electrical connection layout (right). The breadboard has two outer power rails marked with red and blue lines, two terminal strips separated by a center channel, and columns of holes labeled A–E and F–J with row numbers 45, 50, 55, and 60. The routing diagram shows the outer power rails connected vertically, while the terminal-strip holes are connected horizontally in groups of five on either side of the center gap. Red lines indicate positive power rails, and blue lines indicate negative power rails."
   caption="Figure 3. Physical (left) and electrical (right) view of a section of a breadboard." %}

To connect two components together, you just need to make sure that the two ends being connected share the same 5-pin row. The metal clips below act as a wire connecting the two ends together. An example is shown below.
 
{% include figure.html
   src="./img/wire-to-resistor.png"
   alt="Diagram showing how to connect a wire to a resistor on a breadboard. On the left, a circuit schematic highlights the junction where a wire connects to one lead of resistor R1 (33 Ω), marked with a black connection dot inside a red circle. On the right, a breadboard view shows the equivalent physical connection: a blue jumper wire and one lead of a resistor are inserted into holes in the same horizontal row, highlighted by a red circle. Green highlights indicate the electrically connected holes, demonstrating that components sharing the same breadboard row are connected together."
   caption="Figure 4. Connecting a wire to a resistor in schematic view (left) and breadboard view (right)." %}

### How to Wire Parts in Series

In order to wire two parts in series, you’ll want the parts share one node. This means that the two ends you are trying to connect need to share the same 5-pin row. You can also use a wire to bridge between rows to connect the two parts at one end. The following images are there to show you a few different ways you can wire components in series.

{% include figure.html
   src="./img/breadboard-in-series.png"
   alt="Three vertically stacked breadboard diagrams illustrating different ways to connect two resistors in series. The top diagram shows one resistor positioned horizontally across the breadboard's center gap and a second resistor positioned vertically on the left side, with both sharing an electrically connected row. The middle diagram shows two resistors positioned vertically on the left side, with one lead of each resistor inserted into the same connected row. The bottom diagram shows two resistors positioned horizontally across the center gap, with a blue jumper wire connecting their left-side rows. Green-highlighted holes indicate electrically connected rows, demonstrating three different arrangements for connecting resistors in series on a breadboard."
   caption="Figure 5. Different ways to wire two elements in series." %}

### How to Wire Parts in Parallel

In order to wire two parts in parallel, you’ll want the parts to share two nodes, one on either side. The following images are there to show you a few different ways you can wire components in series.

{% include figure.html
   src="./img/breadboard-in-parallel.png"
   alt="Three vertically stacked breadboard diagrams illustrating different ways to connect two resistors in parallel. The top diagram shows two resistors positioned vertically side by side, with their upper leads sharing one electrically connected row and their lower leads sharing another. The middle diagram shows two vertically positioned resistors in different rows, with a blue jumper wire connecting their upper leads and a shared row connecting their other leads. The bottom diagram shows two resistors positioned horizontally across the breadboard's center gap, with blue jumper wires connecting their corresponding ends on both sides. Green-highlighted holes indicate electrically connected rows, demonstrating three arrangements in which both resistors share the same two electrical connection points."
   caption="Figure 6. Different ways to wire two elements in parallel." %}

### How to Add Integrated Circuits, Buttons, and Other Elements

Integrated circuits, or ICs for short, are complex circuits built into a tiny, black “chip.” To learn more about the makeup of ICs, you can watch this optional video.

{{ fixme }}

ICs can come in all different shapes and sizes, depending on the application. Those designed to be used with breadboards come as a Dual In-line Package, or DIP. To use DIP ICs on your breadboard, you’ll have to use that ravine that runs down the middle of your board, called the mounting channel. The following image shows the correct placement of an IC, as well as a potentiometer, onto a breadboard.

{% include figure.html
   src="./img/breadboard-ic.png"
   alt="Breadboard diagram illustrating how to position an integrated circuit (IC) and a multi-terminal component across the center gap of a solderless breadboard. At the top, an eight-pin IC straddles the center channel, with four pins inserted into separate rows on each side. Below it, a three-terminal adjustable component is positioned with its terminals inserted into separate electrically connected rows. Green-highlighted holes indicate the electrical connections within each row. The arrangement demonstrates how placing components across the breadboard's center gap keeps their terminals electrically isolated from one another, allowing independent circuit connection."
   caption="Figure 7. Wiring a dual in-line package (DIP) style chip and a 3-terminal potentiomenter." %}

## How to Power the Breadboard

### How to Effectively Use the Power Strips

The two vertical columns of pins on either side of the main area are reserved for source voltages and ground connections. These columns are available along the entire length of the board, since power and ground often need to be accessed at many points in a circuit. 

The figure below shows a typical breadboard with +12 and -12V power supplies connected and two ground lines. The source voltages could come from a battery, an AC-DC adapter, or a bench supply.

{% include figure.html
   src="./img/breadboard-ic.png"
   alt="Diagram illustrating how to connect positive and negative 12-volt power supplies and ground to a solderless breadboard. On the left, a red wire labeled +12V connects to the positive power rail, while a black wire labeled GND connects to the adjacent ground rail. On the right, a red wire labeled −12V connects to the red-marked power rail, while a black wire labeled GND connects to the adjacent blue-marked ground rail. Green-highlighted holes indicate electrically connected positions along each vertical rail. Red and black ovals and arrows emphasize that all holes within the corresponding power and ground rails share the same electrical connection."
   caption="Figure 8. Breadboard with power strips connected to +12, -12 and Ground." %}

### How to Use the Bench-top Power Supply

Watch the following video on powering your protoboard using the benchtop power supply:

{{ fixme }}

### How to Use the Digilent Analog Discovery 3

The following video shows you how to use the previously released device, the Analog Discovery 3, to power your protoboard:

{{ fixme }}

### How to use the Power-to-Breadboard Adapter

In the off-chance that you’ll be borrowing components from us to work on labs at home, the take-home kits comes with two special DC barrel jack to screw terminal adapters that will allow you to connect the 12V wall adapters. You can then attach wires to the screw terminals, which also connect to the breadboard. When properly set up with grey and white wires, they look like this:

{% include figure.html
   src="./img/power-terminal.png"
   alt="Close-up photograph of a black DC barrel jack power adapter with a green two-position screw terminal block. Two wires, one dark and one light-colored, extend from the terminal block, with each wire inserted into a separate terminal. Two silver screws on top of the green block secure the wires in place, allowing the adapter to connect a DC power supply to a circuit or breadboard."
   caption="Figure 9. DC barrel jack to screw terminal adapter." %}

Note that the black wire should be wired to the (-) post and the white wire to the (+) post. Once configured, plug in a wall adapter and confirm you are getting about 12V at the wire leads (actually, it should  be a little larger than 12V) with the voltmeter switched to DCV. 

When you plug a power supply into the barrel jack, a voltage potential of +12V will extend along the red horizontal line marking the top “power strip” of the breadboard.  Ground (0V potential) will run along the row marked with a blue line. 

The breadboard also has four short jumper wires bridging the gaps on the power strip lines in the center, where there is a break in the connection. This ensures that power and ground extend all the way across the board. Make sure your breadboard looks like the following, making sure to add the short jumper wires in the middle of the board. Leave the wall adapter unplugged while you construct the rest of the circuit. 

<div class="e22-lab-activity" markdown="1">

### Complete Activity 3: Build the Circuits

You will be building some circuits to show that you understand how to properly use a breadboard. 

- **For all breadboarded circuits**, you may either build a physical circuit and take a picture of it, or you may prototype the entire board on [Tinkercad Circuits](https://www.tinkercad.com/circuits). (The latter is easier if you're working from home.)
- **For all circuit diagrams**, you can neatly hand-draw them and take a picture of it. You can also use an online circuit diagram maker (search for it - there are may to choose from) such as [Circuit Canvas](https://circuitcanvas.com/).
- **You can check your answers** using [Circuit Canvas](https://circuitcanvas.com/), which will automatically convert breadboard circuits into a circuit diagram. Note that regardless of whether you do this, you are still responsible for understanding how to build circuits for the rest of the semester.

</div>

## Digital Multimeters (DMMs)

A DMM is a very important tool for electricians and electrical engineers. Depending on the model and the specifications, a DMM can be used to measure multiple parameters, including voltage, resistance, current, continuity, capacitance, and temperature. 

 
Figure 4. Two different digital multimeters, the Keysight multimeter (left) and the Tacklife multimeter (right).
The Keysight DMM (show on the left) measures voltage, resistance, continuity, capacitance, and temperature (note that this does NOT measure current!). This unit also is auto-ranging; you do not need to “find” the correct sensitivity in order to take a reading. To take measurements, you will need to attach the cables to the correct port:
	COM: Short for “common,” the black probe should be plugged into this port. This probe should be placed on the side of the circuit that is closest to 0 V when making voltage measurements.
	VΩ: The red probe should be placed into this side. The various symbols correspond to the different measurements that can be taken by using this port. This probe should be placed on the side of the circuit that is farthest from 0 V when making voltage measurements.

The Tacklife DMM (shown on the right) measures voltage, resistance, current, and continuity (note that this does NOT measure capacitance or temperature!). This unit is not autoranging; 
	10A: The red probe should be plugged into this port when making current measurements only. 
	COM: Short for “common,” the black probe should be plugged into this port. This probe should be placed on the side of the circuit that is closest to 0 V when making voltage measurements.
	VΩ: The red probe should be placed into this side when making any measurements other than current. The various symbols correspond to the different measurements that can be taken by using this port. This probe should be placed on the side of the circuit that is farthest from 0 V when making voltage measurements.[TD5.1]

Each meter has measurement limits in voltage and current beyond which the meter will be damaged. For the DMMs supplied in this lab, the maximum voltage input is 600 V, while for the Tacklife, the maximum current input is 10 A.

 	Be careful to connect the red probe to the correct jack for the measurement you are performing, or you could damage the meter.
How to Measure Resistance

Watch the following videos on digital multimeters and measuring resistance: 
Measure Resistance - Video 1
Measure Resistance - Video 2 [TD6.1]

As you make your measurements, keep in mind that if your fingers are touching the leads you may distort the resistance measurement. You may find it easier to plug the resistor across two rows in your breadboard so you can connect the leads without touching them.

TIP!	In order to accurately measure the value of the resistor, be sure that it is not powered and it is disconnected from any circuitry.

Complete Activity 4: Measuring Resistance

How to Measure Voltage

Watch the following video on using your DMM to measure voltage:
Measure voltage using your digital multimeter

Your Analog Discovery 2 (old model) can also measure voltage (but not current). Watch this video to learn how to measure voltage: Measure voltage using Analog Discovery  

When you want to measure voltage, be sure to switch the device of your choosing to measure DC (direct current) voltage, as indicated by the symbol  . You can measure the voltage any element making up the circuit by touching the V probe to an exposed wire on the “+” side and the COM probe to an exposed wire on the “–” side of each one. An example of a measurement of the voltage across R2 is shown below.

 

Circuit Diagram 1
The alligator clip probes can help in attaching the probes to your circuit. It can also be helpful to connect a small wire to the end of an alligator clip to probe into the breadboard at the desired points.


TIP!	Note that we place the DMM in parallel to the element when we wish to measure the voltage.

Complete Activity 5: Measure Voltage

How to Measure Current

Watch the following video on measuring current using your DMM:
Measure current using your digital multimeter

In order to measure the current, you will need to reconfigure your DMM to measure current. For current measurements, the circuit must be temporarily broken in order for the current to go through the DMM. Keep in mind that in current measurement mode, the DMM has little-to-no resistance, so plugging your DMM in parallel with a component can cause damage to it. An example of a circuit to measure current I2 that passes through R2 is shown below.

 

Circuit Diagram 2
TIP!	Note that we place the DMM in series to the element when we wish to measure the current.

Complete Activity 6: Measure Current


Digital Multimeter Tips

Here are some extra guidelines to help you with using your DMM:
	Always power down the circuit before measuring resistance with a DMM.
	To measure the resistance of a single component embedded in a larger circuit, disconnect at least one side of the component from the rest of the circuit; otherwise, parallel current paths may provide incorrect readings.
	Voltage measurements are made parallel to the components being measured.
	Current measurements are made in series and always require temporarily breaking the circuit to insert the DMM into the current path. Be sure to check that the probes are connected to the correct ports.

   Warning   

Never connect a DMM in ammeter mode across a resistor or voltage source.
Since the ammeter acts like a short circuit, this connection would damage 
the meter or possibly blow a fuse that would need to be replaced.

AVOID THIS CONNECTION in AMMETER MODE:

 



Workstation Cleanup 
Turn off the DMM, turn off power to your circuit, put all wires and components back in their bins, return circuit kits to the cart and upload your completed datasheet to the submission site.
