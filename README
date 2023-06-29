# image text to speech conversion-code
#This repository contains python code of my project "Image to Speech Extraction System".

#THE CODE STARTS FROM HERE

import time 
import numpy as np 
import cv2 from PIL 
import Image 
import sys
import espeak 
import picamera
import RPi.GPIO as GPIO 
sw = 18
sentences = splitParagraphIntoSentences("Welcome To The Project Portable camera for book reading system")

#Speak aloud each sentence in paragraph one by onefor s in sentences:
sound(s.strip()) def main():
GPIO.setmode(GPIO.BCM)	# Use BCM GPIO numbers 
GPIO.setup(sw, GPIO.IN) # LED
while True:

print GPIO.input(sw)

if not GPIO.input(sw):
open("out1.txt","w").close() 
text_file = open("out1.txt","w") 
time.sleep(0.1)

#Take an image from the RaspberryPi camera with sharpness 100(increases the readability of the text for OCR) 
call ("raspistill -o j2.jpg -t 1 -sh 100", shell=True)
print "Image taken"
#Start the Tesseract OCR and save the call 
("tesseract j2.jpg out1", text to out1.txt shell=True)
print "OCR complete"

#Open the text file and split the paragraph to Sentences
fname="out1.txt" f=open(fname) 
content=f.read() 
print content sentences = splitParagraphIntoSentences(content)
#Speak aloud each sentence in the paragraph one by one for s in sentences:
sound(s.strip())
 
time.sleep(0.2)
