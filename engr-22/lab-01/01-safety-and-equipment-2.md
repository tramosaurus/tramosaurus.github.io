---
title: "ENGR 22 Lab 1: Safety and Equipment - Part 2"
date: "2026-11-20"
author: "T. Dang"
---

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
   src="/engr-22/lab-01/img/resistor-band.png"
   alt="The image shows a close-up of a four-band resistor. The resistor is oriented so that the right-most band is gold, which is the tolerance band. The first band is orange, the second band is blue, and the third band is brown. The color bands tell us that it's a 360 ohm resistor."
   caption="Figure 1. How to orient a resistor to read resistor band colors." %}

<figure>
  <img src="/engr-22/lab-01/img/resistor-band.png" alt="The image shows a close-up of a four-band resistor. The resistor is oriented so that the right-most band is gold, which is the tolerance band. The first band is orange, the second band is blue, and the third band is brown. The color bands tell us that it's a 360 ohm resistor.">
  <figcaption>Figure 1. How to orient a resistor to read resistor band colors.</figcaption>
</figure>

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

You can use the following image to help you determine the nominal value of your resistor



<div class="e22-lab-activity" markdown="1">

#### Complete Activity 2: Identifying Resistor and Resistor Color Codes

The full directions for the activity can be found on your Data and Answer Sheet.

</div>

<div style="float: right" markdown="1">

Ready to move on? [Go to Part 3.](/engr-22/lab-01/01-safety-and-equipment-3)

</div>

<div style="float: left" markdown="1">

Need to go back? [Go to Part 1.](/engr-22/lab-01/01-safety-and-equipment-1)

</div>
 
