## Text-to-Speech-Module

### Pre-requisites

- pyttsx3 is a text-to-speech conversion library in Python.
  Unlike alternative libraries, it works offline, and is compatible
  with both Python 2 and 3.
- The OS module in python provides functions for interacting
  with the operating system. OS, comes under Python's standard utility modules.
  
### Install Libraries

- pip install pyttsx3 

PS: OS library should be available before hand with python distribution.

### Import Libraries

         import pyttsx3
         import os

### Lets dive into the code

           engine = pyttsx3.init('sapi5')

sapi5 is a referance to male voice for windows. Init() is a function to create an object<br> 
of pyttsx3 type.<br>

         voices = engine.getProperty('voices')
        
Gets the current value of an engine property.<br>

        engine.setProperty('voice',voices[0].id)
        
Queues a command to set an engine property. The new property value affects all utterances<br>
queued after this command.<br>

         def speak(audio):
               engine.say(audio)
               engine.runAndWait()

<br>It is an user defined function. The pyttsx3 function say() pronounces the actual audio.<br>
The runAndWait() function blocks while processing all currently queued commands. <br>
Invokes callbacks for engine notifications appropriately. <br>
Returns when all commands queued before this call are emptied from the queue.<br>
  
         remember = open('input.txt','r')

<br>Here our text file is opened and stored in 'remember'<br>

         speak(remember.read())

 <br>Now finally we call our function.


