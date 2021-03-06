## Welcome to Our Computer Vision Project

# Introduction
## What is Color Blindness?
Well in simple words, its the inability of ones eyes to truly see the color the way it should.
Our eyes perceive everything around us by receiving the lights being reflected by the objects on the retina of the eye. The retina itself is covered with special nerve cells that contain pigments that react to light: 
- Cones: These are active at higher light levels (photopic vision), are capable of color vision and are responsible for high spatial acuity.
- Rods: These are responsible for vision at low light levels (scotopic vision). They do not mediate color vision, and have a low spatial acuity.

![eye](https://user-images.githubusercontent.com/36117814/94383554-6f18d380-010e-11eb-8477-bf2d344dfd48.gif)

Normal color vision requires the use of specialized receptor cells called cones, which are located in the retina of the eye. 
There are three types of cones, termed red, blue, and green, which enable people to see a wide spectrum of colors. An abnormality, or deficiency, of any of the types of cones will result in abnormal color vision.
Dichromats and anomalous trichromats exist again in three different types according to the missing cone or in the latter case of its malfunctioning.

1. Tritanopia/Tritanomaly: Missing/malfunctioning S-cone (blue).
2. Deuteranopia/Deuteranomaly: Missing/malfunctioning M-cone (green).
3. Protanopia/Protanomaly: Missing/malfunctioning L-cone (red).

![what-color-blind-people-see-different-types-blindness-9](https://user-images.githubusercontent.com/36117814/94381889-c9af3100-0108-11eb-8c31-ec10b10ca6d4.jpg)

# Problem Statement
## Goal
The main goal of our project is to create a program that will convert a colored image to a version that will allow people with colorblindness to see. The three types of color blindness that we are focusing on are Deuteranopia(where green looks more red), Protanopia(where red looks more green), and Tritanopia(for blue/yellow colorblindness). The current plan to do this is to modify the input pictures that come in with the appropriate filter. If there is time at the end, we would like to implement real time output and to be able to modify videos as well. 

## Expected Input
The only inputs that the user needs to provide is the media they want to be modified and the type of colorblindness they are looking to address. 

## Desired Output
The desired output is to compensate for the color blindness, aka allowing those with the red-green color blindness to see red and green in images

# Approach
## Technical Approach
1. Do research on what causes the different types of color blindness and different technologies addressing the issue such as Enchroma.
Modify the RGB and HSV color spaces of the images to determine the best result
From our current research, it seems that the main reason behind color blindness is due to the fact that certain color wavelengths aren’t recognized that well by the eye. (Damaged or lacking con) 
Test our images 
This is the hardest part of our design. Most of the results will be qualitative, so we need to interpret that in some way. 
2. Ideally, we want to be able to test our program on actual colorblind people. Most of the results will be qualitative and will depend on how much “change” they see. 
3. However, if we do not find colorblind people for all of the different types of colorblindness, we are also going to test our resulting images against other color blindness programs and see how similar the results are. 
4. Repeat steps 2 and 3 until the results are satisfying

# Experiments and Results
## Experimental Setup
- Experiment with the color space parameters
- Currently with each type of colorblindness certain colors are weaker to the eye so we will experiment with increasing intensity of that specific color and decreasing the intensity of the weaker color. 

## Datasets Used
- No external datasets will be used in terms of finding images and applying filters
- Alok Tripathy

## Any existing code

## What we will implement ourselves
- The entire solution. We are not aware of any code existing regarding this solution. 
- Thus, we are coming up with a game plan to be able to tackle this by understanding in detail about how different colors interact with each other(wavelength) to produce the effect of color.

## Our definition of success for the project
When our test subject is able to see the specific color that is related to their color blindness

## Will we collect our own data
Yes, the images/videos will be found online, and we will use our own test subject to determine if our implementation works

## Uncertainty Areas
- Because we are dealing with qualitative verbal feedback from our test subjects and none of the members in the team are colorblind, it will become more difficult to determine when we have “finished” our design. 
- To help to reduce this risk, we need to look for more test subjects, possibly providing some kind of incentive to get people to volunteer themselves.
- We can also use a numerical scaling/ grading that the test subjects can use as feedback on the images. For example, we can have a google sheet asking our test subjects to review our solution and its effectiveness on a scale of -5-5 where -5 means that the image was worse than before and 5 means this is the best they’ve seen. This way we can avoid deciphering relative terms like “better” and “best” but have absolute numerical data. 
